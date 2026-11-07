# Conversor Akountik v6.0

Sube `index.html`, `README.md` y `.nojekyll` a la raíz del repositorio GitHub Pages (rama `main`, carpeta `/(root)`).

Corrección BBP Bank: el lector procesa únicamente las tablas CREDITOS y DEBITOS y se detiene antes de SALDOS DIARIOS. Los saldos diarios no son movimientos y quedan excluidos.

La aplicación procesa los PDF localmente en el navegador. Valida siempre las filas e importes contra el extracto original antes de importar a Akountik.
