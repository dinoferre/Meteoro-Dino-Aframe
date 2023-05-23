# Meteor|Dino / A-Frame

## HTML:

El archivo HTML define la estructura básica de la página web. Está compuesto por las siguientes secciones y elementos principales:

Sección `<head>`: Contiene las etiquetas meta para especificar la codificación de caracteres, la compatibilidad con navegadores y la configuración de la vista. También incluye el título de la página y los enlaces a los archivos de JavaScript necesarios.
  
Sección `<body>`: Aquí se encuentra el contenido visible de la página. Contiene un elemento <a-scene> que define la escena en 3D.
  
`<a-assets>`: Dentro de la escena, se utiliza la etiqueta `<a-assets>` para precargar imágenes de texturas que se utilizarán más adelante en la escena.
  
`<a-sky>`: Se crea un cielo utilizando la etiqueta `<a-sky>`. La imagen de textura precargada se aplica como fondo del cielo.
  
`<a-entity>`: Se generan cuatro entidades `<a-entity>` que representan órbitas en la escena. Cada una tiene atributos de posición y rotación, así como animaciones de rotación.
  
`<a-entity camera look-controls>`: Se crea una entidad de cámara con la etiqueta `<a-entity camera look-controls>`. Incluye un texto y un cursor en el centro de la escena. El cursor tiene propiedades para detectar los objetos con clase .meteor y tiene una apariencia de anillo.
  
## JavaScript:

El archivo JavaScript contiene código que se ejecuta cuando la página se carga y define un componente personalizado. Aquí está el resumen:

`window.addEventListener('load', initScene)`: Este código registra un evento de carga que llama a la función `initScene()` cuando la página se carga completamente.
  
`meteors`: Es un arreglo de objetos que representa las coordenadas x, y y z de diferentes meteoritos.
  
`meteor y score`: Son variables globales utilizadas en el código.
  
`initScene()`: Esta función se encarga de inicializar la escena. Itera sobre las órbitas y crea entidades de meteoritos utilizando las coordenadas del arreglo meteors. Se configuran atributos de geometría, material y clase para cada meteorito, y se agrega el componente shootable. Los meteoritos son hijos de las órbitas.
  
`'shootable'` (componente personalizado): Este componente se registra utilizando `AFRAME.registerComponent()`. Inicializa con el evento `'init'` y agrega un escucha de clic al elemento. Cuando se hace clic en un meteorito, se elimina del DOM y se actualiza la puntuación mostrada en un elemento de texto.
