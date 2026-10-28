# CotiStudio 2.0 — Plantillas reutilizables y catálogo automático

Aplicación estática para navegador. Importa PDFs, conserva cada página como fondo visual para proteger dibujos e imágenes, intenta recuperar texto del PDF como objetos editables, permite añadir elementos libres, guardar diseños como plantillas y añadir páginas de catálogo automáticamente.

## Publicar en GitHub Pages
1. Haz una copia de seguridad de la versión anterior.
2. Sube `index.html` y `README.md` a la raíz del repositorio.
3. En Settings → Pages, elige Deploy from a branch, `main`, `/(root)` y guarda.
4. Espera a que termine el despliegue y abre la URL de Pages.

## Funciones
- Editor de texto, líneas, rectángulos, círculos, imágenes, etiquetas y máscaras para cubrir zonas.
- Selección, movimiento, redimensionado, propiedades, capas, duplicado, eliminación y orden.
- Importación de PDF de varias páginas. PDF.js renderiza cada página y también intenta extraer sus fragmentos de texto para reconstruirlos encima de máscaras blancas; se mantienen las imágenes y gráficos originales en el fondo.
- Biblioteca de plantillas guardadas en el almacenamiento local del navegador.
- Exportación/importación de plantillas como archivos JSON para respaldarlas o trasladarlas a otro dispositivo.
- Las plantillas guardan los elementos gráficos y una lista de productos/accesorios; al aplicarlas, pueden añadir automáticamente páginas de catálogo.
- Guardar/abrir proyectos `.cotistudio` y exportar el documento final como PDF.

## Guardar y aplicar una plantilla
1. Importa un PDF y corrige/revisa los textos recuperados.
2. Ajusta el diseño de la página actual.
3. En “Plantillas guardadas”, introduce un nombre y los repuestos/accesorios, y pulsa “Guardar plantilla”.
4. Para reutilizarla, importa otra cotización, selecciona la plantilla y pulsa “Aplicar”.
5. Si está marcada la opción de catálogo automático, se añadirán páginas con los productos configurados. Las listas largas se distribuyen en páginas adicionales.
6. Para usar la plantilla en otro dispositivo, selecciónala y pulsa “Exportar”; en el otro navegador importa el archivo JSON.

## Limitaciones importantes
- La extracción de texto es heurística. El PDF puede tener fragmentos mal posicionados, estilos perdidos o zonas en las que la máscara blanca tape parte de una línea o dibujo. Revisa y corrige todas las páginas tras importar.
- No hay reconstrucción semántica completa de tablas ni asociación automática garantizada entre cada producto y su fotografía. El diseño se aplica mediante elementos y posiciones; no es un sustituto perfecto de un sistema de edición de PDF estructural.
- El PDF exportado se compone como imagen por página; el texto del PDF final no será seleccionable. La nitidez depende de la escala de importación.
- Las plantillas guardadas en el navegador no se sincronizan entre dispositivos. Exporta copias JSON para respaldo. Si el almacenamiento local se borra, las plantillas locales podrían perderse.
- PDF.js y pdf-lib se cargan desde CDN; hace falta conexión a internet. El procesamiento del PDF ocurre en el navegador.
- La aplicación no modifica automáticamente los importes originales ni valida la exactitud comercial. Antes de enviar una cotización, compara cantidades, precios, subtotales y total.
