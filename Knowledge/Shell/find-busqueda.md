# Comando `find`: Búsqueda Avanzada de Archivos y Directorios 🔍
#shell #bash #linux #find

El comando `find` es una de las herramientas más potentes de Linux para localizar archivos y directorios basándose en diversos criterios (nombre, tipo, tamaño, fecha, etc.).

## 🚀 Casos de Uso Comunes

### 1. Buscar por nombre (Exacto o Parcial)
Para buscar un elemento que contenga una palabra específica en su nombre:

- **Comando**: `find /ruta/donde/buscar -name "*palabra*"`
- **Ejemplo**: `find . -name "*liceo*"` (Busca cualquier cosa que contenga "liceo" desde la carpeta actual).

> [!TIP] Case Insensitive
> Usa `-iname` en lugar de `-name` para que la búsqueda ignore mayúsculas y minúsculas.

### 2. Buscar solo Directorios o solo Archivos
Puedes filtrar los resultados por el tipo de elemento:

- **Solo Directorios**: `find . -type d -name "*palabra*"`
- **Solo Archivos**: `find . -type f -name "*palabra*"`

### 3. Limpiar la salida (Omitir errores de Permiso)
Al buscar en carpetas del sistema (como `/`), es común ver muchos errores de "Permiso denegado". Puedes redirigirlos al vacío:

- **Comando**: `find / -type d -iname "*liceo*" 2>/dev/null`

---

## 📊 Tabla de Parámetros Rápidos

| Parámetro | Descripción | Ejemplo |
| :--- | :--- | :--- |
| `-name` | Busca por nombre (distingue mayúsculas) | `-name "notas.txt"` |
| `-iname` | Busca por nombre (ignora mayúsculas) | `-iname "notas.txt"` |
| `-type d` | Filtra solo directorios | `-type d` |
| `-type f` | Filtra solo archivos | `-type f` |
| `2>/dev/null` | Oculta errores de permisos | (al final del comando) |

---
*Documentación generada colaborativamente con Claude Code.*
