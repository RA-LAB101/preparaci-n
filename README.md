# Clases importantes en AR Foundation con C#

Autor: _Diego Carvajal_

# Documentacion

## Justificación:

## Conceptos Claves:

- AR Foundation: AR Foundation es el puente entre las distintas plataformas y el desarrollo en **Unity**, representa en sí una interfaz que no implementa ninguna tecnología de AR. Por tal motivo, para ser usada, debe combinarse con un plug-in capaz de dirigir el desarrollo a una plataforma específica, estos plug-ins son:

  - [Google ARCore XR Plug-in](https://docs.unity3d.com/Packages/com.unity.xr.arcore@5.0/manual/index.html)
  - [Appli ARKit](https://docs.unity3d.com/Packages/com.unity.xr.arkit@5.0/manual/index.html)

  En cada uno hay características/funcionamientos de RA que se soportan en unity y otras [que no](https://docs.unity3d.com/Packages/com.unity.xr.arfoundation@5.0/manual/index.html).

- XR: es una forma de incluir todas estas aplicaciones en un mismo término:
  - Virtual Reality
  - Mixed Reality
  - Augmented Reality

## Buenas prácticas:

# Ejemplos

## Clase [MonoBehavior](https://docs.unity3d.com/2021.2/Documentation/ScriptReference/MonoBehaviour.html)

- Es la clase base en la que todo Script deriva.
- Cuenta con varios métodos para sobre-escribir, como:
  - _Start()_ como el método inicial de todo Script, se ejecuta antes de que cualquier método _update()_ lo haga.
  - _Update()_ se activa en cada recuadro (frame (o acutialización de dibujo))
- Cuenta con varios métodos a modo de eventos, como por ejemplo:
  - _OnCollisionEnter()_
  - _OnDestroy()_
  - _OnGUI()_
- Es útil y muy usado para conectarnos con valores propios de un objeto, como su geometría de colisión, sus propiedades de movimiento/rotación/escala, etc.

## ARSession

- Controla la sesión de Realidad Aumentada en el dispositivo
- Sirve para hacer acciones cuando ciertos comportamientos ocurren en el dispositivo, como:

  - attemptUpdate: cuando el dispositivo soporta XR pero no tiene el software requerido.
  - notTrackingReason: Cuando AR Tracking se ha perdido.
  - stateChanged: Cuando el estado de la AR session ha cambiado.
    Algunos de sus estados son:
    ![imagen de estados](/images/ARSession/states.png)
