Akountik v6.8.5

Ajuste para Banco de Bogotá – Miami Agency:
- Reconoce el emisor por la estructura del Account Statement / Transactions Detail, evitando clasificarlo por bancos intermediarios o beneficiarios mencionados en movimientos.
- Lee fecha de contabilización, descripción y columnas Debit Amount, Credit Amount, Fee y Balance.
- Las comisiones y cargos de servicio con importe distinto de cero se exportan como débitos independientes.
- Excluye Previous Balance, Account Summary, Current Balance, total y texto legal.
- Conserva los lectores anteriores de Itaú, Citibank, JPMorgan, Wells Fargo, Ficohsa y demás bancos.

Validación con ExtractoDeCuenta.pdf:
22 movimientos; débitos USD 1,282,973.50 (incluye USD 255.00 en comisiones); créditos USD 1,216,109.25.
La extracción y los totales coinciden con el resumen del extracto. Revisar el archivo original antes de importar.
