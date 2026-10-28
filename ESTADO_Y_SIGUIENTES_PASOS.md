# CotiStudio 2.0 — Estado de la versión

## Implementado en esta entrega
- Importación de PDFs de varias páginas y conservación visual del original como fondo.
- Intento de extracción de fragmentos de texto con PDF.js: cada fragmento se representa como texto editable con una máscara blanca detrás, mientras se conserva el fondo para mantener dibujos e imágenes.
- Editor de elementos gráficos y de texto, movimiento, redimensionado, propiedades, capas, duplicación, eliminación, orden, deshacer/rehacer.
- Guardar diseños como plantillas reutilizables en localStorage.
- Exportar plantillas como JSON e importarlas en otro navegador/dispositivo.
- Campos para configurar catálogo de accesorios y opción de páginas automáticas por plantilla.
- Generación de páginas de catálogo con encabezado, lista de accesorios y pie de página; las listas largas se reparten en varias páginas.
- Aplicar una plantilla a la cotización actual y generar las páginas extra configuradas.
- Guardar/abrir proyecto `.cotistudio` y exportar PDF.

## Limitaciones que siguen vigentes
- La reconstrucción de texto usa posiciones aproximadas. Es posible que algunos fragmentos se desplacen, pierdan estilo o se superpongan; las máscaras pueden cubrir líneas o partes de gráficos cercanos.
- No se reconocen de forma semántica las filas de tablas ni se asocian de forma garantizada los dibujos con sus productos.
- La exportación PDF sigue siendo rasterizada y el texto no queda seleccionable.
- La biblioteca de plantillas se guarda localmente en el navegador; no hay sincronización en nube. Para moverla entre dispositivos se debe exportar/importar el JSON.
- Se requiere conexión a internet para cargar PDF.js y pdf-lib.
- La versión requiere pruebas en navegador real con distintas cotizaciones antes de considerarse lista para producción.

## Pruebas mínimas antes de uso comercial
1. Importar `COT-2026-0839.pdf` y revisar texto, líneas, dibujos y máscaras.
2. Crear una plantilla con 3 accesorios, guardarla, recargar la página y comprobar que sigue disponible.
3. Exportar la plantilla JSON e importarla en otro navegador.
4. Aplicar la plantilla a una segunda cotización y confirmar que añade la página de catálogo.
5. Probar más de 7 accesorios y verificar que se generen varias páginas.
6. Exportar el PDF final y comprobar todas las páginas, cantidades, precios, subtotal y total.
