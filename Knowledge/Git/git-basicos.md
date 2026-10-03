# Git Básico: Flujo de Trabajo Inicial 🛠️
#git #bash #versionado

Este documento resume los comandos fundamentales para iniciar un proyecto, gestionar los cambios localmente y sincronizarlos con un servidor remoto (como GitHub).

## 🚀 1. Configuración e Inicio

### `git init`
Inicializa un nuevo repositorio de Git en la carpeta actual. Crea la carpeta oculta `.git` donde se almacena todo el historial.
- **Uso**: `git init`

### `git clone <url>`
Copia un repositorio existente desde un servidor remoto a tu máquina local.
- **Uso**: `git clone https://github.com/usuario/repo.git`

---

## 📦 2. Gestión de Cambios Locales

### `git status`
Muestra el estado actual del repositorio: archivos modificados, en staging o no rastreados. Es el "diagnóstico" esencial antes de cualquier acción.
- **Uso**: `git status`

### `git add <archivo>`
Añade archivos al **Área de Preparación (Staging Area)**.
- **Uso**: `git add README.md` (uno) o `git add .` (todos).

### `git commit -m "mensaje"`
Crea una "foto" permanente (snapshot) de los archivos en el Staging Area.
- **Uso**: `git commit -m "Mensaje descriptivo"`

> [!TIP] Tip Profesional
> Usa `git commit -am "mensaje"` para hacer `add` y `commit` en un solo paso (solo para archivos ya rastreados).

---

## ☁️ 3. Sincronización Remota (GitHub/GitLab)

### `git remote add origin <url>`
Vincula tu repositorio local con un servidor remoto por primera vez.
- **Uso**: `git remote add origin https://github.com/usuario/repo.git`

### `git push`
Sube tus commits locales al servidor remoto.
- **Uso**: `git push -u origin main` (la primera vez) o simplemente `git push`.

### `git pull`
Trae los cambios más recientes del servidor y los fusiona con tu copia local. Fundamental para evitar conflictos antes de hacer un push.
- **Uso**: `git pull origin main`

---

## 🔄 El Flujo de Trabajo Completo
El ciclo profesional de trabajo es:
1. **Modificar** $\rightarrow$ 2. `git add` $\rightarrow$ 3. `git commit` $\rightarrow$ 4. `git pull` (por seguridad) $\rightarrow$ 5. `git push`

## 💡 Analogía del Paquete (Completa)
- **Working Directory**: Tu mesa de trabajo (donde escribes).
- **Staging Area**: La caja del paquete (donde seleccionas qué enviar).
- **Commit**: El sello del paquete (le das una identidad y fecha).
- **Remote (GitHub)**: La oficina central (donde el paquete se guarda para siempre y otros pueden verlo).
- **Push**: El servicio de mensajería (lleva el paquete de tu mesa a la oficina central).
- **Pull**: Pedir la última versión del paquete que está en la oficina central.

---
[[Git-MOC]] $\leftarrow$ Volver al Mapa de Git
