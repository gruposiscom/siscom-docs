---
sidebar_position: 6
---

# Migrar boot de Windows a Linux con systemd-boot

Este tutorial muestra como migrar el boot de Windows 11 a la ESP (EFI System Partition) nueva de Pop!\_OS y limpiar dual-boot

Escenario típico:

- Windows en ESP de ~100 MB
- Pop!\_OS crea otra ESP de ~1 GB
- systemd-boot solo lee la ESP activa (/boot/efi)

Resultado: Windows no aparece en el menú.

La solucion es migrar el bootloader de Windows a la ESP nueva y limpiar las entradas EFI viejas.

## 1. Identificar las particiones de las ESP

```bash
lsblk -f
```

Busca algo como:

```text
├─nvme0n1p1
│ vfat FAT32 92C3-1BD1
├─nvme0n1p5
│     vfat   FAT32             BF15-702D                             701.1M    31% /boot/efi
```

Verás la ESP activa montada en /boot/efi (en el ejemplo es nvme0n1p5) y la ESP de Windows (nvme0n1p1).

## 2. Montar la ESP de Windows antigua

Crea un directorio para montar la ESP de Windows en `/mnt`

```bash
sudo mkdir /mnt/old-esp
```

Monta la partición:

```bash
sudo mount /dev/nvme0n1p1 /mnt/old-esp
```

verifica el contenido:

```bash
ls /mnt/old-esp/EFI
```

Normalmente verás una carpeta "Microsoft" con los archivos de boot de Windows.

```text
Microsoft
Boot
```

## 3. Copiar el bootloader de Windows a la nueva ESP

Copia la carpeta "Microsoft" a la nueva ESP activa:

```bash
sudo cp -r /mnt/old-esp/EFI/Microsoft /boot/efi/EFI/
```

Esto copia:

```text
EFI/Microsoft/Boot/bootmgfw.efi
```

a la ESP nueva.

## 4. Eliminar bootloaders antiguos (Opcional)

Si hay restos de instalaciones anteriores (ej. Ubuntu/kubuntu):

```bash
sudo rm -rf /boot/efi/EFI/ubuntu
sudo rm -rf /boot/efi/EFI/kubuntu
```

Esto evita que aparezcan entradas fantasmas en el firmware UEFI.

## 5. Respaldar el bootloader antiguo de Windows

En lugar de eliminarlo directamente, respalda comprimiendo la carpeta:

```bash
cd /mnt/old-esp/EFI/
sudo tar -czvf windows-boot-backup.tar.gz Microsoft
```

Luego elimina el directorio original:

```bash
sudo rm -rf /mnt/old-esp/EFI/Microsoft
```

Esto evita que el firmware vuelva a crear la entrada antigua nuevamente.

## 6. Elimina entradas EFI antiguas

Lista entradas actuales:

```bash
efibootmgr
```

Ejemplo típico:

```text
Boot0003 Windows Boot Manager
Boot0004 Windows Boot Manager
Boot0007 Pop!_OS
Boot0008 ubuntu
```

Elimina las entradas viejas:

```bash
sudo efibootmgr -b 0003 -B
sudo efibootmgr -b 0008 -B
```

## 7. Activar el menú de systemd-boot

Edita la configuración:

```bash
sudo nano /boot/efi/loader/loader.conf
```

Contenido recomendado:

```text
default Pop_OS-current.conf
timeout 10
console-mode max
editor no
```

## 8. Reiniciar el sistema

```bash
sudo reboot now
```

### Resultado esperado

Al arrancar aparecerá el menú de **systemd-boot** con algo así:

```text
Pop!_OS
Pop!_OS (previous kernel)
Windows Boot Manager
```

La entrada de Windows se detecta automáticamente gracias al soporte de **auto-entries** de systemd-boot, por lo que **no es necesario crear un `windows.conf` manual**

### Estructura final del EFI

```text
/boot/efi
 ├─ EFI
 │  ├─ systemd
 │  ├─ Pop_OS-UUID
 │  └─ Microsoft
 │     └─ Boot
 │        └─ bootmgfw.efi
 └─ loader
    └─ entries
```

Todo el arranque queda centralizado en una sola ESP

### Ventajas de esta configuración

- Dual-boot límpio
- Un solo EFI
- systemd-boot detecta Windows automáticamente
- Menos riesgo de romper boot al actualizar kernels
