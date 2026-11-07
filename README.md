# Conversor Akountik v6.6

Aplicación estática para convertir extractos bancarios PDF a un archivo tabulado `.xls` compatible con Akountik.

## Publicación en GitHub Pages

1. Descomprime el ZIP.
2. Copia `index.html`, `README.md` y `.nojekyll` a la raíz del repositorio.
3. Confirma los cambios en la rama `main`.
4. Espera la publicación de GitHub Pages y actualiza con `Ctrl + F5`.

## Lectura y exportación

- Los lectores específicos de bancos incluidos en la versión base v6.5 se conservan.
- Los formatos desconocidos pasan por el lector universal conservador.
- Los PDF sin texto seleccionable pueden intentar OCR mediante Tesseract.js; requiere conexión para cargar la biblioteca.
- La exportación Akountik conserva cinco columnas: `Fecha`, `Descripción`, `Número de Referencia`, `Débito`, `Crédito`.
- Los movimientos ambiguos quedan marcados para revisión y bloquean la exportación .xls.
- No se eliminan movimientos repetidos.

## Aprendizaje de formatos (v6.6)

En el panel **Aprendizaje de formatos bancarios** puedes guardar reglas para un formato no reconocido:

1. Escribe un nombre para el banco/formato.
2. Escribe una frase distintiva que aparezca en el encabezado del extracto. Esa frase permite seleccionar la regla automáticamente.
3. Define palabras que indiquen débito y crédito, separadas por comas.
4. Guarda las reglas.

Las reglas se guardan en el almacenamiento local del navegador. Puedes exportarlas a JSON para respaldarlas o importarlas en otro equipo. El JSON contiene únicamente las reglas configuradas, no extractos ni movimientos.

**Límite importante:** el aprendizaje v6.6 configura la identificación del formato y las palabras para clasificar débito/crédito en líneas compatibles con el lector universal (fecha, descripción e importe en la misma línea). No aprende automáticamente diseños complejos de columnas ni sustituye una validación humana. Si el formato no encaja con esa estructura, debe revisarse y no debe forzarse su importación.

## Privacidad

El procesamiento de PDF ocurre en el navegador. Las reglas se guardan localmente en ese navegador hasta que se exporten o borren los datos del sitio. No se envían extractos a GitHub. PDF.js y Tesseract.js se cargan desde CDN.
