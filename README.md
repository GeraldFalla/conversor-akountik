# Conversor universal de extractos para Akountik

Prototipo inicial de aplicación web estática. Lee archivos PDF desde el navegador mediante PDF.js y genera un archivo de texto tabulado con extensión `.xls`.

## Publicar en GitHub Pages
1. Crea un repositorio nuevo en GitHub.
2. Sube `index.html` a la raíz del repositorio.
3. En Settings > Pages, selecciona Deploy from a branch, rama `main`, carpeta `/ (root)`.
4. Espera la publicación y abre la URL de GitHub Pages.
5. En SharePoint, agrega el elemento web **Insertar** e intenta insertar la URL publicada. Si el dominio no está permitido en el iframe, usa un vínculo/botón en la página para abrir la aplicación en otra pestaña.

## Importante
- Este es un prototipo de validación, no una versión productiva ni un parser universal terminado.
- La extracción PDF.js ocurre en el navegador; el PDF no se envía al repositorio ni a un servidor propio.
- PDF.js se carga desde cdnjs, por lo que el navegador requiere acceso a ese CDN. Para entorno corporativo se recomienda alojar también los archivos de PDF.js en el repositorio tras revisar sus licencias.
- Las reglas actuales son iniciales y conservadoras. BBVA Panamá, Helm Bank y Zions Bank tienen reglas dedicadas preliminares; otros formatos caen en un patrón genérico y pueden quedar marcados para revisión.
- Validar siempre movimientos, fechas, referencias y conciliación contra el extracto original antes de importar a Akountik.
- La exportación `.xls` es texto separado por tabulaciones, no un libro de Excel.
