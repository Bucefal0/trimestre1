# Consulta de exámenes · Matemáticas · Trimestre 1

Sitio estático (un solo archivo HTML, sin dependencias) donde cada alumno elige
**grado → grupo → su nombre** y ve en pantalla completa la hoja de respuestas
escaneada de su examen.

## Publicación

El sitio se sirve con **GitHub Pages** desde la rama `main`:

👉 https://bucefal0.github.io/trimestre1/

## Estructura

```
index.html        Página (contiene el índice de los 195 alumnos)
Segundo D/        Hojas de respuestas escaneadas (.jpg)
Tercero A/ ... F/
Grupos.xlsx       Libro de calificaciones (fuente de los nombres y resultados)
```

## Configuración

Dentro de `index.html`, al inicio del `<script>`, está el bloque `CONFIG`:

| Campo | Para qué sirve |
|---|---|
| `base` | Ruta de las carpetas si no están junto al HTML (por defecto `""`) |
| `whatsapp` | Activa el botón **"Tengo una duda"** (número con lada, sin signos) |
| `email` | Alternativa por correo para el mismo botón |
| `clavePorGrupo` | Candado opcional por grupo, p. ej. `{ "Tercero C": "mate2026" }` |

## Aviso

El repositorio es **público**: contiene nombres, calificaciones y las imágenes de
los exámenes. Cualquier persona con la liga puede consultarlos y el historial de
Git conserva las versiones anteriores.
