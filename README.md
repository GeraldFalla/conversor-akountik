# Akountik v6.7.9

Corrección del lector BBVA España para extractos mensuales escaneados.

- Fuerza OCR local cuando BBVA España se identifica por encabezados, pero la capa de texto no contiene movimientos.
- Reconstruye operaciones por fecha contable, fecha valor e importe, asociando conceptos y referencias cercanas.
- Interpreta importes europeos y separa débitos/créditos.
- Conserva los lectores existentes de Citi, BBVA Panamá y los demás bancos; el cambio está limitado al flujo OCR de BBVA España y su parser.

La prueba con el PDF de septiembre de 2026 produjo 8 movimientos: débitos EUR 5.454,73 y créditos EUR 68.438,57. Debe validarse en navegador y contra el extracto antes de usarlo como versión estable.
