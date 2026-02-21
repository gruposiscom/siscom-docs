---
sidebar_position: 3
---

# Reparación de Imagen de Sistema y Reparación de sistema mediante imagen

Para reparar la imagen de sistema de archivos de windows utilizamos el comando de Servicio y Gestión de Despliege de imagen `dism`, _"Deployment Image Servicing and Management"_, por sus siglas en inglés.

```batch
dism /online /cleanup-image /restorehealth
```

Una vez que la imagen de sistema esta restaurada ejecutamos el comando de verificación de archivos de sistema `sfc`, _"System File Checker"_, por sus siglas en inglés.

```batch
sfc /scannow
```
