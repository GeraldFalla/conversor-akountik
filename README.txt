Akountik v6.8.1 – ajuste del lector existente de Itaú

Base: v6.7.9, conservando lectores específicos existentes.
Cambio: el lector existente de Itaú ahora reconoce el estado de cuenta de Itaú Panamá por la estructura del encabezado y procesa la columna Valor como movimiento firmado, excluyendo la columna Saldo.

Validación con el archivo estadocta102066939_092026.pdf:
- 19 movimientos detectados.
- Débitos: 4,765,606.86 USD.
- Créditos: 4,799,997.60 USD.
- Coincide con los totales de movimientos declarados en el extracto.

No se creó un lector paralelo. No se modificó el lector de Citibank ni los demás lectores.
