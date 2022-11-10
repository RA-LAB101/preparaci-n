# Buenas prácticas **a la hora de manipular objetos en 3D**

Autor: _Diego Carvajal_

## Justificación:

Los objetos 3D son producto de muchos años de investigación y de desarrllo, no es de sorpresa que tengan detrás de ellos una complejidad considerable. Asomarse a ver esa complejidad nos asusta pero también nos da una comprensión general de sus componentes, para tener mayor control sobre ellos en un proyecto de RA.

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

### Archivos y objetos

- Reflejar en los nombres unicidad y orden.

  - Reflejar en el orden de las carpetas, el orden de las escenas, entonces, si tuvieramos 2 escenas, una para la UI y otra para RA, estas serían las subcarpetas de assets, así:

    ![imagen](/images/names/folderNames.png)

    Lo idean es que a medida en que se desarrollan esas escenas, ese mismo orden se refleje en las carpetas.

  - Nombrar los archivos de manera única y con nombres claves para facilitar las búsquedas

## Mesh

- Construir teniendo en cuenta la cantidad y necesidad de polígonos
  - Algunas herramientas de modelado necesitan un proceso final de optimización para quitarle peso al Mesh.
- Evitar triángulos muy largos y delgados
  ![imagen](/images/meshes/stairs.png)

  La imagen de la izquierda tiene 726 polígonos y la de la derecha solo 156.

- Una buena práctica es empezar muy simple e ir añadiendo detalles al modelo.

## Textures

- Si se usan texturas con medidas en potencias de 2 (512x512, 256\*512, etc), serán más eficientes y no necesitarán re-escalamiento en build-time

- Probar con texturas de menor tamaño, y negociar entre la calidad y el peso que le aporta a la escena.
- Guardar las texturas de salida (output textures) en una carpeta apartada.

- Como en la imagen, separar las texturas que requieren elementos alpha de las que no lo requiere.

  ![imagen](/images/textures/separateAlpha.jpeg)

Recursos recomendados relacionados

- [Good practices with assets](https://docs.unity3d.com/2020.1/Documentation/Manual/HOWTO-ArtAssetBestPracticeGuide.html)

- [Polygon Mesh](https://en.wikipedia.org/wiki/Polygon_mesh)

- [Textures](https://docs.unity3d.com/Manual/Textures.html)
