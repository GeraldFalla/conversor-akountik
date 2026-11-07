# Conversor Akountik v6.7.3

Actualización del lector universal para tablas delimitadas con operaciones que pueden continuar en una o varias líneas del texto extraído del PDF.

## Cambios
- Conserva la operación cuando la fecha y descripción aparecen en una línea y los importes/referencia en la siguiente.
- Reconoce continuaciones de descripción y recupera referencias al final de la fila continuada.
- Interpreta importes con espacios como separador de miles, por ejemplo `1 250,50`, mediante el normalizador numérico existente.
- Mantiene los movimientos del lector universal en revisión manual y no habilita su exportación automáticamente.
- No modifica los lectores específicos de bancos.

## Publicación en GitHub Pages
Reemplaza `index.html`, `README.md` y `.nojekyll` en la raíz del repositorio y espera el despliegue. Actualiza el navegador con `Ctrl + F5`.

## Validación
La sintaxis JavaScript y la estructura del ZIP se validan antes de publicar. La lectura del PDF de prueba debe verificarse en navegador; no se considera aprobada hasta comparar movimientos, importes y referencias con el documento original.
