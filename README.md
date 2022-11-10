# Buenas prácticas **a la hora de manipular objetos en 3D**

Autor: _Diego Carvajal_

## Justificación:

## Conceptos Claves:

- Materials: Describe la apariencia del objeto 3D, usando implementaciones de una clase shader en Unity. Generalmente se manipulan mediante una interfaz en unity, en donde podemos controlar variables de color y de Texturas.
- Textures: es una imagen estandar que es aplicada a través de la superficie de un Mesh. Está relacionado a los Shaders, haciendo posible efectos de luminancia.
- Polygon Meshes: En español "malla" o como mejor lo entiendo "palitos" es una colección de datos que describen **la superficie** de una figura en 3D, esta colección está dada por vértices, aristas y caras, aunque algunas implementaciones guardan polígonos y superficies.

  Estos "palitos" están involucrados en la detección de colisiones, modelamiento de luz (ray tracing) y movimiento de cuerpo rígido

  Suele usarse triángulos, por la facilidad de cómputo, aunque también pueden emplearse cuadriláteros, o polígonos cóncavos/convexos

## Buenas prácticas:

### Escala y unidades:

Es de importancia ajustar las unidades de medida, tanto para la luminancia como efectos de física y la preservación de realismo en un objeto 3D en RA.

- Ajustar en el programa de modelado el sistema de medida y tenerlo en cuenta al exportar a Unity.

  - Algunos vienen por defecto en cm mientras otros en pulgadas.
  - En caso de duda, exportar un métro cúbico y compararlo con el objeto en cuestión

- Ajustar y tener en cuenta el velocidad de animación (frame rate).

Recursos recomendados relacionados
https://docs.unity3d.com/2020.1/Documentation/Manual/HOWTO-ArtAssetBestPracticeGuide.html
https://docs.unity3d.com/es/530/Manual/HOWTO-ArtAssetBestPracticeGuide.html
https://en.wikipedia.org/wiki/Polygon_mesh
https://docs.unity3d.com/Manual/Textures.html

Ejemplos
