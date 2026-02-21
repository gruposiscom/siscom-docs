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

| Atajo                   | Acción                        |
| ----------------------- | ----------------------------- |
| **Win + Tab**           | Vista de tareas               |
| **Alt + Tab**           | Cambiar ventanas              |
| **Win + D**             | Mostrar escritorio            |
| **Win + ↑ / ↓ / ← / →** | Ajustar ventana               |
| **Win + Shift + ← / →** | Mover ventana entre monitores |

---

# 🛡️ Seguridad --- Defender / Firewall / UAC

## Windows Defender

| Comando                       | Descripción breve                    |
| ----------------------------- | ------------------------------------ |
| `windowsdefender:`            | Abre Seguridad de Windows            |
| `ms-settings:windowsdefender` | Abre ajustes de Seguridad de Windows |

### Secciones Defender

| Comando                                 | Descripción breve                       |
| --------------------------------------- | --------------------------------------- |
| `ms-settings:windowsdefender-firewall`  | Abre Firewall y protección de red       |
| `ms-settings:windowsdefender-antivirus` | Abre Protección contra virus y amenazas |

---

## Firewall

| Comando        | Descripción breve                 |
| -------------- | --------------------------------- |
| `firewall.cpl` | Abre el panel clásico de Firewall |
| `wf.msc`       | Abre el Firewall avanzado         |

---

## UAC

| Comando                          | Descripción breve         |
| -------------------------------- | ------------------------- |
| `UserAccountControlSettings.exe` | Abre configuración de UAC |

### Alternativas gestión cuentas

| Comando                  | Descripción breve                     |
| ------------------------ | ------------------------------------- |
| `netplwiz`               | Gestión avanzada de cuentas           |
| `control userpasswords2` | Gestión avanzada de cuentas (clásico) |

### UAC avanzado (Policies)

| Comando      | Descripción breve                  |
| ------------ | ---------------------------------- |
| `secpol.msc` | Abre directivas de seguridad local |

Ruta: Local Policies → Security Options

---

# 🔁 Windows Update

## Panel principal

| Comando                     | Descripción breve                    |
| --------------------------- | ------------------------------------ |
| `ms-settings:windowsupdate` | Abre Windows Update en Configuración |

## Legacy

| Comando          | Descripción breve                       |
| ---------------- | --------------------------------------- |
| `control update` | Abre el panel clásico de Windows Update |

## Secciones

| Comando                             | Descripción breve                 |
| ----------------------------------- | --------------------------------- |
| `ms-settings:windowsupdate-action`  | Abre acciones de Windows Update   |
| `ms-settings:windowsupdate-history` | Abre historial de actualizaciones |
| `ms-settings:windowsupdate-options` | Abre opciones avanzadas           |

---

# 🧨 ADMIN GOD --- Run Commands Arsenal

## 🧠 Núcleo Sistema

| Comando     | Descripción breve       |
| ----------- | ----------------------- |
| `msinfo32`  | Información del sistema |
| `sysdm.cpl` | Propiedades del sistema |
| `winver`    | Versión de Windows      |
| `dxdiag`    | Diagnóstico de DirectX  |

---

## 👤 Usuarios

| Comando                  | Descripción breve                     |
| ------------------------ | ------------------------------------- |
| `lusrmgr.msc`            | Usuarios y grupos locales             |
| `netplwiz`               | Gestión avanzada de cuentas           |
| `control userpasswords2` | Gestión avanzada de cuentas (clásico) |

---

## ⚙️ Hardware / Drivers

| Comando       | Descripción breve                   |
| ------------- | ----------------------------------- |
| `devmgmt.msc` | Administrador de dispositivos       |
| `hdwwiz.cpl`  | Asistente para agregar hardware     |
| `joy.cpl`     | Configuración de controles/joystick |
| `mmsys.cpl`   | Sonido y dispositivos de audio      |

---

## 💾 Discos / Storage

| Comando        | Descripción breve                  |
| -------------- | ---------------------------------- |
| `diskmgmt.msc` | Administración de discos           |
| `cleanmgr`     | Limpieza de disco                  |
| `dfrgui`       | Optimizar y desfragmentar unidades |

---

## 🌐 Red

| Comando       | Descripción breve    |
| ------------- | -------------------- |
| `ncpa.cpl`    | Conexiones de red    |
| `inetcpl.cpl` | Opciones de Internet |

---

## 🧬 Servicios / Procesos / Monitoreo

| Comando        | Descripción breve       |
| -------------- | ----------------------- |
| `services.msc` | Servicios de Windows    |
| `taskmgr`      | Administrador de tareas |
| `resmon`       | Monitor de recursos     |
| `perfmon`      | Monitor de rendimiento  |
| `eventvwr.msc` | Visor de eventos        |

---

## 🏢 Consolas Enterprise

| Comando        | Descripción breve              |
| -------------- | ------------------------------ |
| `compmgmt.msc` | Administración de equipos      |
| `gpedit.msc`   | Directivas de grupo local      |
| `rsop.msc`     | Resultant Set of Policy (RSoP) |

---

## 🧪 Recovery / Diagnóstico

| Comando    | Descripción breve                  |
| ---------- | ---------------------------------- |
| `msconfig` | Configuración del sistema/arranque |
| `mdsched`  | Diagnóstico de memoria             |
| `rstrui`   | Restaurar sistema                  |

---

## 📦 Software / Features

| Comando            | Descripción breve           |
| ------------------ | --------------------------- |
| `appwiz.cpl`       | Programas y características |
| `optionalfeatures` | Características de Windows  |
| `control folders`  | Opciones de carpetas        |

---

# 🕶️ Nivel Avanzado (Poco Conocidos pero Útiles)

| Comando      | Descripción breve                      |
| ------------ | -------------------------------------- |
| `shrpubw`    | Asistente de carpetas compartidas      |
| `fsmgmt.msc` | Administración de recursos compartidos |
| `credwiz`    | Asistente de credenciales              |
| `azman.msc`  | Authorization Manager                  |

---

# 🧩 Flujos Reales de Soporte

## PC Lenta

| Comando              | Descripción breve            |
| -------------------- | ---------------------------- |
| `Ctrl + Shift + Esc` | Abre Administrador de tareas |
| `resmon`             | Monitor de recursos          |
| `perfmon`            | Monitor de rendimiento       |
| `eventvwr.msc`       | Visor de eventos             |

---

## Sospecha Malware

| Comando            | Descripción breve         |
| ------------------ | ------------------------- |
| `windowsdefender:` | Abre Seguridad de Windows |
| `msconfig`         | Configuración de arranque |
| `taskmgr`          | Procesos y rendimiento    |

---

## Problemas de Red

| Comando        | Descripción breve             |
| -------------- | ----------------------------- |
| `ncpa.cpl`     | Conexiones de red             |
| `devmgmt.msc`  | Administrador de dispositivos |
| `eventvwr.msc` | Visor de eventos              |

---

# 🧬 Tip Admin Real

Muchos .msc existen en: C:`\Windows\System32`

Si sabes el nombre → probablemente funciona en Win + R.

---

# 🧨 Bonus Mental Model

Tipo Ejemplo

---

| Tipo           | Ejemplo               |
| -------------- | --------------------- |
| `.msc`         | Consolas MMC          |
| `.cpl`         | Panel control clásico |
| `ms-settings:` | Config moderna        |
| `.exe`         | Ejecutables directos  |

---
