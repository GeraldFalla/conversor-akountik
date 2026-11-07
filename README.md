# Conversor Akountik v6.7.4

Aplicación estática para convertir extractos bancarios PDF a archivo tabulado `.xls` compatible con Akountik.

## Publicación en GitHub Pages
Reemplaza `index.html`, `README.md` y `.nojekyll` en la raíz del repositorio que publica GitHub Pages. Conserva la rama y configuración actuales. Espera el despliegue y actualiza con Ctrl+F5.

## Cambios v6.7.4
- Excluye líneas de saldos iniciales/finales y totales cuando aparecen como continuaciones.
- Evita incorporar importes y referencias a la descripción en las continuaciones del lector universal.
- Conserva las reglas de perfiles JSON, el contador de revisión y la revisión manual.
- No modifica los lectores bancarios específicos.

## Alcance
La corrección debe verificarse con `Northstar_multilineas_numeros.pdf`. La sintaxis JavaScript y la estructura del paquete se validan antes de publicar; el comportamiento integral debe confirmarse en navegador. Los formatos universales permanecen sujetos a revisión manual.
