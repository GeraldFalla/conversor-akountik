# Akountik v6.8.0

Corrección del lector BBVA España para extractos EUR procesados mediante OCR.

Cambios:
- Reconocimiento por SWIFT BBVAESMM y estructura de columnas del extracto.
- Lectura de filas con fechas y columna IMPORTE aunque el OCR separe conceptos y referencias.
- Captura del primer importe de la fila como movimiento; el segundo importe (SALDO) no se exporta.
- Asociación de conceptos y referencias multilínea.
- No se modificaron los lectores de Citibank ni los demás bancos.

Validar el resultado contra el PDF original antes de importar a Akountik.
