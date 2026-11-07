# Conversor Akountik v6.7.6

Aplicación estática para convertir extractos bancarios PDF a archivo tabulado `.xls` compatible con Akountik.

## Cambios v6.7.6
- Corrige el lector Citibank Account Statement Details: admite etiquetas y valores en líneas separadas y toma el importe firmado aunque el PDF lo ubique antes de la etiqueta.
- Reconoce los movimientos por Bank Reference, Value Date, Transaction Description y Transaction Amount.
- No clasifica el banco por intermediarios o beneficiarios y no modifica los demás lectores.

## Cambios v6.7.5
- Bancolombia Panamá se identifica por la estructura de la tabla de movimientos, no por el titular, tipo de cuenta ni número de cuenta.
- El lector admite las columnas intermedias de sucursal/canal y DCTO./REF. antes del valor y saldo.
- Reconstruye descripciones en varias líneas y elimina de ellas referencias repetidas y etiquetas de canal.
- Conserva la clasificación de débitos y créditos por el signo del valor.
- No modifica las funciones de los demás lectores bancarios.

## Publicación en GitHub Pages
Reemplaza `index.html`, `README.md` y `.nojekyll` en la raíz del repositorio que publica GitHub Pages. Conserva la rama y configuración actuales. Espera el despliegue y actualiza con Ctrl+F5.

## Validación realizada
- Citibank Account Statement Details, septiembre de 2026: 29 movimientos extraídos del PDF de prueba (26 débitos y 3 créditos).
- Débitos: USD 10,287,562.36.
- Créditos: USD 10,866,732.11.
- Validación del lector sobre el texto extraído; falta la prueba final en navegador y la regresión con otros extractos reales.

## Validación anterior
- Ucipharma Panamá, julio de 2026: 15 movimientos detectados.
- Débitos: USD 333,540.08.
- Créditos: USD 265,000.86.
- Los valores coinciden con los totales del resumen del extracto.
- La prueba se realizó sobre el texto extraído del PDF y el lector JavaScript; falta la prueba final en navegador y la regresión con otros extractos reales.
