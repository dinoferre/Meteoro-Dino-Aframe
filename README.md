# Meteor|Dino / A-Frame

Este proyecto del Metaverso utiliza la tecnología de `A-Frame` para crear una experiencia interactiva en 3D. Está compuesto por un archivo HTML y JavaScript que trabajan en conjunto para renderizar una escena en la que se pueden disparar meteoritos.

El archivo HTML define la estructura básica de la página web y contiene una sección `<head>` con metadatos y enlaces a archivos JavaScript necesarios. La sección `<body>` contiene el contenido visible de la página, incluyendo la etiqueta `<a-assets>` para precargar imágenes de texturas y la etiqueta `<a-sky>` para crear un cielo con una imagen de fondo. Además, se generan entidades `<a-entity>` que representan órbitas en la escena, y se crea una entidad de cámara con texto y un cursor en el centro.

El archivo JavaScript contiene código que se ejecuta cuando la página se carga. Utiliza el evento `'load'` para llamar a la función `initScene()`, la cual inicializa la escena. Se itera sobre las órbitas y se crean entidades de meteoritos utilizando coordenadas predefinidas. Cada meteorito tiene atributos de geometría, material y clase, y se agrega el componente `'shootable'`. Este componente personalizado se registra utilizando `AFRAME.registerComponent()` y añade un escucha de clic a cada meteorito. Cuando se hace clic en un meteorito, se elimina del `DOM` y se actualiza la puntuación mostrada en un elemento de texto.

Este proyecto utiliza la biblioteca `A-Frame` y el componente personalizado `'shootable'` para crear una experiencia interactiva en el metaverso. Combina elementos de realidad virtual y elementos web tradicionales para proporcionar una experiencia inmersiva y divertida para los usuarios.

Dino Ferré 👽 - Link del proyecto 👇

https://dinoferre.github.io/Meteoro-Dino-Aframe/
