# Comando `ls`: Listar Directorios 📁

Este documento detalla las formas de filtrar la salida del comando `ls` para mostrar únicamente las carpetas (directorios), omitiendo los archivos.

## 🚀 Métodos de Filtrado

### 1. Método Rápido (Patrón de Shell)
La forma más sencilla de listar solo carpetas en el directorio actual.
- **Comando**: `ls -d */`
- **Explicación**: 
    - `-d`: Indica a `ls` que liste los directorios mismos, en lugar de listar el contenido de esos directorios.
    - `*/`: El asterisco es un comodín y el slash `/` final obliga a que el patrón solo coincida con elementos que sean directorios.

### 2. Método Detallado (Usando `grep`)
Ideal cuando necesitas ver permisos, dueño, tamaño y fecha de modificación.
- **Comando**: `ls -l | grep '^d'`
- **Explicación**:
    - `ls -l`: Lista los archivos en formato largo (long format).
    - `|`: Tubería (pipe) que pasa la salida de `ls` al siguiente comando.
    - `grep '^d'`: Filtra las líneas que comienzan (`^`) con la letra `d` (que representa *directory* en los permisos de Linux).

### 3. Método Preciso (Usando `find`)
La mejor opción si necesitas una lista limpia de rutas para usar en scripts o automatizaciones.
- **Comando**: `find . -maxdepth 1 -type d`
- **Explicación**:
    - `.`: Busca en el directorio actual.
    - `-maxdepth 1`: Limita la búsqueda solo al nivel actual, evitando entrar en subcarpetas.
    - `-type d`: Filtra estrictamente para que solo se devuelvan elementos de tipo directorio.

---

## 📊 Tabla Comparativa

| Método | Salida | Velocidad | Uso Ideal |
| :--- | :--- | :--- | :--- |
| `ls -d */` | Nombres con `/` | Muy Rápido | Consulta visual rápida |
| `ls -l \| grep '^d'` | Detallada | Rápido | Auditoría de permisos |
| `find` | Rutas limpias | Medio | Scripts y automatización |
