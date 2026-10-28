# CotiStudio v5 — edición de elementos corregida

## Cambios
- Corregido el flujo de arrastre: la selección ya no reemplaza el nodo DOM antes de comenzar a moverlo.
- El arrastre y el redimensionamiento se manejan con listeners de documento y coordenadas relativas a la página.
- Se actualizan las posiciones del elemento en tiempo real sin volver a dibujar el lienzo en cada movimiento.
- Tirador de redimensionamiento más grande para pantallas táctiles.
- Las bandas del diseño rápido se crean como elementos `band` y no como rectángulos genéricos.
- Las bandas empiezan a ancho completo, pero pueden moverse verticalmente y redimensionarse desde el tirador.
- Se puede corregir posición y tamaño desde los campos X, Y, ancho y alto.

## Instalación
Reemplaza `index.html` en la raíz del repositorio GitHub y espera a que GitHub Pages publique el cambio. Recarga la página de forma completa. Si tienes un proyecto viejo abierto, elimina las franjas pequeñas defectuosas y vuelve a añadirlas; los elementos guardados antiguos no se transforman automáticamente.

## Limitación
El PDF importado sigue siendo un fondo visual rasterizado; este cambio corrige la manipulación de los elementos añadidos, no convierte el contenido original del PDF en objetos editables.
