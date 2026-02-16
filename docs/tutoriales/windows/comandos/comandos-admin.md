---
sidebar_position: 1
---

# 🧾 Comandos y Atajos de teclado para el Administrador de Sistemas Windows

## ⌨️ Atajos de Teclado Clave para Admin Windows

---

### 🧠 Control del sistema / seguridad

| Atajo                      | Qué hace                | Cuándo lo usas                                          |
| -------------------------- | ----------------------- | ------------------------------------------------------- |
| **Ctrl + Alt + Supr**      | Menú de seguridad       | Cuando todo está congelado pero aún responde el sistema |
| **Ctrl + Shift + Esc**     | Task Manager directo    | Cuando quieres matar procesos rápido                    |
| **Win + L**                | Bloquear sesión         | Cuando te paras del equipo                              |
| **Win + Ctrl + Shift + B** | Reinicia driver gráfico | Cuando la pantalla se congela o se pone negra           |

---

### ⚡ Consolas rápidas

| Atajo                 | Qué abre                            |
| --------------------- | ----------------------------------- |
| **Win + X**           | Menú admin rápido (Power User Menu) |
| **Win + R**           | Ejecutar (RUN)                      |
| **Win + E**           | Explorador de archivos              |
| **Win + Pause/Break** | Info del sistema                    |
| **Win + I**           | Configuración                       |

### Tips Win + X

- **A** → Terminal / PowerShell admin
- **U → R** → Reiniciar
- **U → S** → Apagar

---

### 🧬 Diagnóstico rápido

| Atajo                      | Comando típico que lanzarías |
| -------------------------- | ---------------------------- |
| **Win + R → eventvwr.msc** | Event Viewer                 |
| **Win + R → devmgmt.msc**  | Device Manager               |
| **Win + R → services.msc** | Servicios                    |
| **Win + R → compmgmt.msc** | Computer Management          |
| **Win + R → diskmgmt.msc** | Administración de discos     |
| **Win + R → msconfig**     | Configuración de arranque    |
| **Win + R → sysdm.cpl**    | Propiedades del sistema      |

---

### 🗂️ Manejo de ventanas

| A                       | Atajo                         | Acción |
| ----------------------- | ----------------------------- | ------ |
| **Win + Tab**           | Vista de tareas               |
| **Alt + Tab**           | Cambiar ventanas              |
| **Win + D**             | Mostrar escritorio            |
| **Win + ↑ / ↓ / ← / →** | Ajustar ventana               |
| **Win + Shift + ← / →** | Mover ventana entre monitores |

---

# 🛡️ Seguridad --- Defender / Firewall / UAC

## Windows Defender

    windowsdefender:
    ms-settings:windowsdefender

### Secciones Defender

    ms-settings:windowsdefender-firewall
    ms-settings:windowsdefender-antivirus

---

## Firewall

    firewall.cpl
    wf.msc

---

## UAC

    UserAccountControlSettings.exe

### Alternativas gestión cuentas

    netplwiz
    control userpasswords2

### UAC avanzado (Policies)

    secpol.msc

Ruta: Local Policies → Security Options

---

# 🔄 Windows Update

## Panel principal

    ms-settings:windowsupdate

## Legacy

    control update

## Secciones

    ms-settings:windowsupdate-action
    ms-settings:windowsupdate-history
    ms-settings:windowsupdate-options

---

# 🧨 ADMIN GOD --- Run Commands Arsenal

## 🧠 Núcleo Sistema

    msinfo32
    sysdm.cpl
    winver
    dxdiag

---

## 👤 Usuarios

    lusrmgr.msc
    netplwiz
    control userpasswords2

---

## ⚙️ Hardware / Drivers

    devmgmt.msc
    hdwwiz.cpl
    joy.cpl
    mmsys.cpl

---

## 💾 Discos / Storage

    diskmgmt.msc
    cleanmgr
    dfrgui

---

## 🌐 Red

    ncpa.cpl
    inetcpl.cpl

---

## 🧬 Servicios / Procesos / Monitoreo

    services.msc
    taskmgr
    resmon
    perfmon
    eventvwr.msc

---

## 🏢 Consolas Enterprise

    compmgmt.msc
    gpedit.msc
    rsop.msc

---

## 🧪 Recovery / Diagnóstico

    msconfig
    mdsched
    rstrui

---

## 📦 Software / Features

    appwiz.cpl
    optionalfeatures
    control folders

---

# 🕶️ Nivel Avanzado (Poco Conocidos pero Útiles)

    shrpubw
    fsmgmt.msc
    credwiz
    azman.msc

---

# 🧩 Flujos Reales de Soporte

## PC Lenta

    Ctrl + Shift + Esc
    resmon
    perfmon
    eventvwr.msc

---

## Sospecha Malware

    windowsdefender:
    msconfig
    taskmgr

---

## Problemas de Red

    ncpa.cpl
    devmgmt.msc
    eventvwr.msc

---

# 🧬 Tip Admin Real

Muchos .msc existen en: C:`\Windows\System32`

Si sabes el nombre → probablemente funciona en Win + R.

---

# 🧨 Bonus Mental Model

Tipo Ejemplo

---

.msc Consolas MMC
.cpl Panel control clásico
ms-settings: Config moderna
.exe Ejecutables directos

---
