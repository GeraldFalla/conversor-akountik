# Conversor Akountik v6.7.8

Aplicación estática para convertir extractos bancarios PDF a archivo tabulado `.xls` compatible con Akountik.

## Cambios v6.7.8
- Corrige el lector `Citibank Account Statement Details` para leer campos cuando etiqueta y valor aparecen en la misma línea (formato real extraído por PDF.js) o en líneas separadas.
- Agrupa cada movimiento por `Bank Reference` y extrae `Value Date`, `Transaction Description`, `Payment Details` y `Transaction Amount`.
- Interpreta importes negativos como débitos y positivos como créditos.
- Excluye saldos y resúmenes, que no forman parte de los bloques de movimiento.
- No modifica las funciones de los demás lectores bancarios.

## Validación realizada
Con el diagnóstico de texto del PDF `1. Account Statement Details Report 67984 USD September 2026.pdf`:
- 29 movimientos detectados.
- 26 débitos por USD 10,287,562.36.
- 3 créditos por USD 10,866,732.11.
- Se conservaron las referencias bancarias.

La validación se realizó ejecutando la función JavaScript del lector sobre el diagnóstico real y verificando la sintaxis del JavaScript de la aplicación. Falta la prueba final en navegador y la regresión de los demás bancos con sus extractos.

## Publicación en GitHub Pages
Reemplaza `index.html`, `README.md` y `.nojekyll` en la raíz del repositorio que publica GitHub Pages. Conserva la rama y configuración actuales. Espera el despliegue y actualiza con Ctrl+F5.


## v6.7.8
- Se incorpora reconocimiento y extracción del formato BBVA España (Extracto Mensual) mediante OCR cuando el PDF no contiene texto seleccionable.
- Se conservan separados los lectores de BBVA Panamá y los demás bancos.
