# CotiStudio Web — prototipo 0.2

## Qué incluye
- Página web adaptable a móvil y escritorio.
- Importación de PDF y renderizado de todas las páginas con PDF.js.
- Las páginas originales se conservan visualmente como fondo, incluyendo los dibujos y las imágenes que ya están incrustadas.
- Capas nuevas de texto e imágenes que se pueden mover y editar.
- Controles de marca y cuatro plantillas visuales.
- Exportación a PDF y guardado/carga de un archivo de proyecto JSON.

## Cómo probar
1. Abre `index.html` en Chrome, Edge o Firefox con conexión a internet (las librerías PDF se cargan desde CDN).
2. Importa un PDF de prueba.
3. Añade un texto o una imagen, arrástralo y edita sus propiedades.
4. Exporta el PDF y verifica el resultado.

## Limitaciones conocidas
- En esta fase el PDF original se conserva como fondo de página, por lo que los textos/precios originales no son elementos individuales editables.
- Las plantillas añaden una banda visual; no remaquetan automáticamente los contenidos existentes porque hacerlo podría tapar o alterar información.
- El PDF exportado se rasteriza como imagen por página, por lo que el texto del fondo no será seleccionable y el archivo puede pesar más.
- El archivo JSON de proyecto incluye el PDF original en base64 numérico y puede ser grande. No subir cotizaciones privadas a servicios públicos sin consentimiento.
- El guardado aún no está sincronizado entre dispositivos. Para tener URL permanente se requiere despliegue en hosting y conectar el repositorio.
