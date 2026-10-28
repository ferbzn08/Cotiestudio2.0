# CotiStudio — revisión de importación y franjas

## Cambios de esta revisión
- El PDF se importa como fondo visual sin volver a generar capas de texto detectado; evita que el texto original se duplique y se superponga.
- Nuevo botón **Franja**: crea una banda horizontal de ancho completo, editable y con color corporativo azul marino. Puede cambiarse el color desde Propiedades.
- Se mantiene el botón Rectángulo para formas de tamaño libre.
- Se actualizaron las instrucciones para explicar que el fondo original se conserva visualmente, pero no se convierte en texto u objetos editables.
- Se pulió el encabezado y el comportamiento de los controles en pantallas pequeñas.

## Uso
1. Importa el PDF.
2. El documento original se mostrará sin texto duplicado.
3. Añade una **Franja** para crear una banda horizontal; selecciona la banda para ajustar su posición, altura y color.
4. Si la banda debe tapar contenido existente, ten presente que lo cubrirá. Para reemplazar texto, usa **Cubrir zona** y luego añade un texto nuevo.
5. Exporta y revisa visualmente todas las páginas.

## Límites conocidos
- El PDF original se rasteriza para preservar su apariencia y dibujos; el contenido original de fondo no es editable como texto.
- Las capas añadidas son editables, pero la exportación sigue siendo rasterizada y el texto exportado no es seleccionable.
- Esta revisión pasó la comprobación sintáctica de JavaScript; no equivale a una prueba completa en todos los navegadores/dispositivos.
- Las librerías PDF.js y pdf-lib se cargan desde CDN y requieren conexión a internet.

## Publicación en GitHub Pages
Sube este `index.html` a la raíz del repositorio y confirma el cambio. No subas únicamente el ZIP: GitHub Pages necesita que `index.html` esté en la raíz publicada.
