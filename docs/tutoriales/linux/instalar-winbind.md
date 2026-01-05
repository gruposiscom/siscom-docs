---
sidebar_position: 5
---

# Instalar winbind

## ¿Qué es winbind?

Winbind es el “traductor” entre Linux y un dominio de Windows.
Permite que una máquina Linux use cuentas de Active Directory (usuarios y grupos) para autenticarse, como si fuera parte del mismo reino corporativo. Maneja el login, resuelve identidades y sincroniza info sin que tengas que estar creando usuarios locales a mano.

## Instalación

```bash
sudo apt update
sudo apt install winbind libnss-winbind
```

Edita el nsswitch:

```bash
sudo nano /etc/nsswitch.conf
```

Busca la línea `hosts:` y modifícala así:

```bash
hosts: files dns wins
Reinicia el servicio:
bashsudo systemctl restart winbind
```
