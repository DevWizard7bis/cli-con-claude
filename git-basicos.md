# Git Básico: Flujo de Trabajo Inicial 🛠️

Este documento resume los comandos fundamentales para iniciar un proyecto y gestionar los cambios en Git.

## 🚀 Comandos Principales

### `git init`
Inicializa un nuevo repositorio de Git en la carpeta actual. Crea la carpeta oculta `.git` donde se almacena todo el historial.
- **Uso**: `git init`

### `git status`
Muestra el estado actual del repositorio: qué archivos han sido modificados, cuáles están en el área de preparación (staging) y cuáles no están siendo rastreados.
- **Uso**: `git status`

### `git add <archivo>`
Añade un archivo específico al **Área de Preparación (Staging Area)**. Indica a Git que este archivo debe incluirse en el próximo commit.
- **Uso**: `git add README.md` (para un archivo) o `git add .` (para añadir todos los cambios del directorio).

### `git commit -m "mensaje"`
Crea una "foto" permanente (snapshot) de los archivos que están en el Staging Area. El mensaje debe describir brevemente qué se cambió.
- **Uso**: `git commit -m "Primer commit: añadir README"`

---

## 🔄 El Flujo Típico
El ciclo de trabajo más común es:
1. **Modificar** archivos $\rightarrow$ 2. `git add` (preparar) $\rightarrow$ 3. `git commit` (guardar)

## 💡 Analogía del Paquete
- **Working Directory**: Tu mesa de trabajo.
- **Staging Area**: La caja del paquete donde metes lo que vas a enviar.
- **Commit**: El envío final del paquete al archivo histórico.
