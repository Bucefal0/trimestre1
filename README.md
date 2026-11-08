# Consulta de exámenes · Matemáticas · Trimestre 1

Sitio estático (un solo archivo HTML, sin dependencias) donde cada alumno elige
**grado → grupo → su nombre** y ve en pantalla completa la hoja de respuestas
escaneada de su examen.

También incluye las **claves de respuestas** (2.º D y 3.º), que se abren en el
mismo visor con las mismas herramientas: ajustar, acercar, girar, descargar e
imprimir. Se puede llegar a ellas de dos formas:

- Botón **"Ver la clave de respuestas"** en la pantalla de inicio.
- Botón **🔑** dentro del visor del examen (y **📄** para regresar a él).

## Publicación

El sitio se sirve con **GitHub Pages** desde la rama `main`:

👉 https://bucefal0.github.io/trimestre1/

## Estructura

```
index.html                  Página (contiene el índice de los 195 alumnos)
Segundo D/                  Hojas de respuestas escaneadas (.jpg)
Tercero A/ ... F/
Claves/clave-2D.jpg         Clave 2.º D (generada de "Clave Examen 2D.pdf")
Claves/clave-3ros.png       Clave 3.º   (generada de "Clave Examen 3ros.pptx")
Grupos.xlsx                 Libro de calificaciones (fuente de nombres y resultados)
```

Las claves se generaron como imagen para poder reutilizar el visor (zoom, ajuste,
giro) en cualquier celular. Si actualizas el PDF o el PPTX hay que volver a
exportar la imagen correspondiente en `Claves/`.

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
