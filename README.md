# CotiStudio v7

Editor reorganizado para cotizaciones FireGroup.

## Funciones
- Herramientas agrupadas por elementos, plantillas, páginas y capas.
- Elementos movibles con arrastre, redimensionamiento y rotación.
- Formas: línea diagonal, rectángulo, círculo, franja completa y franja diagonal tipo chevron.
- Importación de logotipos e imágenes.
- Importar PDF y añadir otro PDF como páginas al final.
- Guardar/abrir proyecto `.cotistudio`.
- Guardar plantillas en el navegador y exportar/importar JSON.
- Exportar PDF.

## Publicación
Reemplaza `index.html` en la raíz del repositorio que publica GitHub Pages.

## Limitaciones importantes
- Los PDF importados se rasterizan como fondo para conservar su apariencia; el texto original no se convierte en texto editable.
- Los PDFs añadidos se incorporan como páginas rasterizadas, no como objetos PDF originales.
- La exportación mantiene los fondos como imágenes y dibuja los elementos añadidos; revisar visualmente el resultado antes de usarlo comercialmente.
- Las librerías PDF.js y pdf-lib se cargan desde CDN y requieren conexión a internet.
- Las plantillas se guardan en localStorage de ese navegador; exporta JSON para respaldarlas.
