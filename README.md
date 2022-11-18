# Responsive de UI en Unity

Autor: _Diego Carvajal_

# Documentacion

## Justificación:
- Se plantea una herramienta útil y accesible, y por eso, debe verse bien sin importar los tamaños de pantalla, que pueden diferir bastante de un dispositivo a otro.

## Conceptos Claves:
- Anchors: O también llamados anclas, son sub-componentes de un objeto de Transformación usado en elementos UI en Unity:
  ![rect transform imagen](/images/rectTransform.png)

  Son útiles para definir el punto de anclaje que servirá para posicionar los elementos UI en los distintos tamaños de pantalla.

- Canvas Scaler: Es un componente de Unity que por defecto está dentro del objeto Canvas en una escena con elementos UI:
 ![canvas scaler imagen](/images/canvasScaler.png)

  Con este componente definimos el comportamiento de escalado al cambiar de tamaño de pantalla.
## Buenas prácticas:
- Trabajar con una resolución base de 1920×1080:
  ![Resolución de referencia](/images/resolutionRef.png)
  Nota: Estas resoluciones pueden obtenerse al cambiar el target build a dispositivos Android.
# Ejemplos

## Ajustar elementos de UI
[Ejemplo en la documentación de Unity](https://docs.unity3d.com/es/2020.1/Manual/HOWTO-UIMultiResolution.html)
