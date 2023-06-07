---
title: "Invernadero 2.0"
layout: single
header:
  overlay_color: "#000000"
  teaser: http://placehold.it/350x250
excerpt: "Control de temperatura, humedad e iluminación de forma autonoma."
sidebar:
  - title: "Invernadero 2.0"
    image: http://placehold.it/350x250
    image_alt: "image"
    text: "Some text here."
  - title: "Lista de materiales"
    text: "
        - [Metacrilato]()

        - [ESP32]()


        __Versión aluminio__

        - [Perfiles de aluminio]()

        - [Tornillería]()

        - [Vertices de montaje]()


        __Versión impresa__

        - [Imprimir las piezas]()

        - [Tornillería]()


        __Electronica__

        - [Sensor de luminosidad BH1750]()
        
        - [Sensor de humedad y temperatura DHT22]()
        
        - 4 x [Mosfet]()
        
        - 2 x [Relé]()
        
        - [Sensor DTS]()
        
        - [Sensor de inundación]()
        
        - [Sensor de CO2]()
        "

toc: true
toc_label: "Pasos"
toc_icon: "cog"


gallery:
  - url: /assets/images/proyectos/invernadero_2_0/circuiteria.jpg
    image_path: /assets/images/proyectos/invernadero_2_0/circuiteria.jpg
    alt: "Circuiteria"
    title: "Circuiteria del prototipo"
  - url: /assets/images/proyectos/invernadero_2_0/iluminacion.jpg
    image_path: /assets/images/proyectos/invernadero_2_0/iluminacion.jpg
    alt: "Prueba de iluminación"
    title: "Prueba de iluminación"
  - url: /assets/images/proyectos/invernadero_2_0/aplicacion.jpg
    image_path: /assets/images/proyectos/invernadero_2_0/aplicacion.jpg
    alt: "Beta de la aplicación"
    title: "Image 3 title caption"
  - url: /assets/images/unsplash-gallery-image-4.jpg
    image_path: /assets/images/unsplash-gallery-image-4-th.jpg
    alt: "placeholder image 4"
    title: "Image 4 title caption"
---

{% include video id="XsxDH4HcOWA" provider="youtube" %}

## Montaje de la estructura

Lorem ipsum dolor sit amet, consectetur adipiscing elit. Nulla egestas ipsum ut risus euismod, in faucibus quam tincidunt. Ut elit purus, imperdiet a ante ut, pellentesque porta nibh. Nam vitae turpis non odio blandit volutpat venenatis et risus. Mauris ac suscipit tellus. Etiam sollicitudin eget sem vitae ultrices. Integer id tristique purus. Donec ac tellus non felis sollicitudin porta. Aenean ante erat, consectetur ac vestibulum ac, egestas sed nisi. Pellentesque non magna vitae erat vestibulum condimentum ac sed tellus. Nam fermentum odio dolor, sit amet pharetra orci porttitor sit amet. Praesent tincidunt hendrerit accumsan. Nulla facilisi. Nam a augue id nibh elementum aliquam nec sit amet arcu. Maecenas hendrerit nulla eget ante auctor, ac tempus sem pellentesque.

![image-right](http://placehold.it/350x250){: .align-right}

Quisque tincidunt leo at ipsum dictum, ac mollis erat pellentesque. Cras bibendum lectus at neque consectetur egestas. Proin laoreet, arcu vitae vehicula vehicula, diam augue feugiat mi, ac lobortis lorem ante ut orci. Mauris fringilla aliquam pulvinar. Morbi suscipit congue sapien ut porttitor. Suspendisse eu ultrices turpis. Quisque ex ante, dignissim tempor pulvinar a, viverra sit amet quam. Maecenas sit amet lorem interdum, vulputate justo non, condimentum eros. Aliquam ut sodales lorem, vel posuere ante. Aliquam augue magna, laoreet non nisl tincidunt, egestas pharetra erat. Fusce malesuada, sem at placerat tincidunt, enim nulla feugiat ipsum, nec vulputate sapien erat a turpis. Donec enim nunc, suscipit tristique sem vitae, dapibus malesuada ex. Proin vitae orci eget diam tristique accumsan id eget neque. Donec consequat, purus ac tincidunt scelerisque, sem mi fringilla ante, vel vestibulum arcu ligula eu nisl. Suspendisse potenti. Nullam vitae eros a tortor consequat pharetra sit amet ac metus.

![image-left](http://placehold.it/350x250){: .align-left}

Etiam viverra, elit dapibus convallis finibus, lacus leo fermentum nisl, et porttitor diam risus in odio. Sed tincidunt congue volutpat. Sed hendrerit odio at sem posuere dignissim. Aliquam a feugiat quam, sed aliquet odio. Curabitur leo sapien, ullamcorper eget mauris et, fermentum lacinia nulla. Morbi vel facilisis metus. In pretium orci ac massa aliquet, ut sollicitudin urna tempor. Etiam imperdiet in ipsum non porttitor.

Quisque non vestibulum augue. Vivamus mauris mi, ultrices non mollis sed, viverra in lectus. Aenean vitae turpis ligula. Vivamus vel lectus quis lorem cursus pretium in quis nibh. Suspendisse convallis urna vel libero dictum malesuada. Pellentesque dignissim a libero et ullamcorper. Nam dignissim euismod tristique.

Quisque rutrum nunc quis lectus faucibus sodales quis posuere augue. Orci varius natoque penatibus et magnis dis parturient montes, nascetur ridiculus mus. Maecenas rhoncus dui malesuada nisi vulputate, sit amet rhoncus odio pellentesque. Curabitur non sapien ut arcu semper pretium. Nulla sollicitudin ipsum quis finibus aliquam. Nulla facilisi. Vestibulum a purus cursus, vulputate libero at, lacinia dolor.

### Versión aluminio

Esta fue la primera versión que se desarrollo de este invernadero. Requiere de doce [perfiles de aluminio como estos](https://aliexpres.com) y 6 planchas de metacrilato. Idealmente el grosor de las planchas debería ser el adecuado para poder encajarlas dentro de los perfiles de aluminio. Esto mejora el aislamiento del interior del invernadero, impidiendo fugas de humedad y temperatura al mismo tiempo que hace la estructura más robusta y firme. Por contra, el precio de esta versión es superior al de la versión impresa, ya que los perfiles de aluminio encarecen el proyecto.

![image-center](/assets/images/proyectos/invernadero_2_0/iluminacion.jpg){: .align-center}

Etiam viverra, elit dapibus convallis finibus, lacus leo fermentum nisl, et porttitor diam risus in odio. Sed tincidunt congue volutpat. Sed hendrerit odio at sem posuere dignissim. Aliquam a feugiat quam, sed aliquet odio. Curabitur leo sapien, ullamcorper eget mauris et, fermentum lacinia nulla. Morbi vel facilisis metus. In pretium orci ac massa aliquet, ut sollicitudin urna tempor. Etiam imperdiet in ipsum non porttitor.

Quisque non vestibulum augue. Vivamus mauris mi, ultrices non mollis sed, viverra in lectus. Aenean vitae turpis ligula. Vivamus vel lectus quis lorem cursus pretium in quis nibh. Suspendisse convallis urna vel libero dictum malesuada. Pellentesque dignissim a libero et ullamcorper. Nam dignissim euismod tristique.

### Versión impresa

En realidad no es una extrctura impresa en 3D como tal, pero si las piezas necesarias para unir y crear la estructura usando metacrilato. Para este diseño hemos usado placas de metacrilato de 25x25 que se mantienen unidas gracias a estas [esquinas impresas en 3D](https://github.com/). Las esquinas delanteras contienen también las visagras para que puedas montar la puerta, que es sencillamente otra placa de metacrilato con su correspondiente pieza impresa para hacer de bisagra.

![image-center](http://placehold.it/350x250){: .align-center}

Por lo tanto, en total vas a necesitar para montar esta versión:

- 6 planchas de metacrilato, en mi caso de 25x25x1.5.
- 4 esquinas posteriores
- 2 esquinas de bisagra
- 2 esquinas de cierre para la puerta

Adicionalmente puedes imprimir y montar otros accesorios que puedes encontrar en el mismo repositorio, como las [rejillas para ventiladores](https://github.com).

Esta versión es más economica que la versión de aluminio, pero también algo más frágil que esta anterior.

## Electronica

El invernadero tiene todo lo necesario para ser lo más autonomo posible, vamos a repasar los siguiente circuitos, que se encargan de mantener la iluminación, temperatura, humedad y riego de forma que se ajusten a las necesidades de las plantas que contiene en tiempo real. En futuras versiones puede que se incluyan otros pareametros que podrían ser interesantes, como la calidad del agua de riego, el PH del sustrado o la acumulación de gaseses como el CO2 y el óxigeno en el interior del invernadero.

Vamos a ver en detalle cada uno de los circuitos y al final lo juntaremos todo para poder pasarlo a una PCB y hacer un desarrollo mucho más robusto y profesional.

### Midiendo la luminosidad

Etiam viverra, elit dapibus convallis finibus, lacus leo fermentum nisl, et porttitor diam risus in odio. Sed tincidunt congue volutpat. Sed hendrerit odio at sem posuere dignissim. Aliquam a feugiat quam, sed aliquet odio. Curabitur leo sapien, ullamcorper eget mauris et, fermentum lacinia nulla. Morbi vel facilisis metus. In pretium orci ac massa aliquet, ut sollicitudin urna tempor. Etiam imperdiet in ipsum non porttitor.

Quisque non vestibulum augue. Vivamus mauris mi, ultrices non mollis sed, viverra in lectus. Aenean vitae turpis ligula. Vivamus vel lectus quis lorem cursus pretium in quis nibh. Suspendisse convallis urna vel libero dictum malesuada. Pellentesque dignissim a libero et ullamcorper. Nam dignissim euismod tristique.

Quisque rutrum nunc quis lectus faucibus sodales quis posuere augue. Orci varius natoque penatibus et magnis dis parturient montes, nascetur ridiculus mus. Maecenas rhoncus dui malesuada nisi vulputate, sit amet rhoncus odio pellentesque. Curabitur non sapien ut arcu semper pretium. Nulla sollicitudin ipsum quis finibus aliquam. Nulla facilisi. Vestibulum a purus cursus, vulputate libero at, lacinia dolor.

### Activando la iluminación cuando sea necesario

### Midiendo la temperatura y la humedad

Etiam viverra, elit dapibus convallis finibus, lacus leo fermentum nisl, et porttitor diam risus in odio. Sed tincidunt congue volutpat. Sed hendrerit odio at sem posuere dignissim. Aliquam a feugiat quam, sed aliquet odio. Curabitur leo sapien, ullamcorper eget mauris et, fermentum lacinia nulla. Morbi vel facilisis metus. In pretium orci ac massa aliquet, ut sollicitudin urna tempor. Etiam imperdiet in ipsum non porttitor.

Quisque non vestibulum augue. Vivamus mauris mi, ultrices non mollis sed, viverra in lectus. Aenean vitae turpis ligula. Vivamus vel lectus quis lorem cursus pretium in quis nibh. Suspendisse convallis urna vel libero dictum malesuada. Pellentesque dignissim a libero et ullamcorper. Nam dignissim euismod tristique.

### Controlando la temperatura y humedad

Quisque tincidunt leo at ipsum dictum, ac mollis erat pellentesque. Cras bibendum lectus at neque consectetur egestas. Proin laoreet, arcu vitae vehicula vehicula, diam augue feugiat mi, ac lobortis lorem ante ut orci. Mauris fringilla aliquam pulvinar. Morbi suscipit congue sapien ut porttitor. Suspendisse eu ultrices turpis. Quisque ex ante, dignissim tempor pulvinar a, viverra sit amet quam. Maecenas sit amet lorem interdum, vulputate justo non, condimentum eros. Aliquam ut sodales lorem, vel posuere ante. Aliquam augue magna, laoreet non nisl tincidunt, egestas pharetra erat. Fusce malesuada, sem at placerat tincidunt, enim nulla feugiat ipsum, nec vulputate sapien erat a turpis. Donec enim nunc, suscipit tristique sem vitae, dapibus malesuada ex. Proin vitae orci eget diam tristique accumsan id eget neque. Donec consequat, purus ac tincidunt scelerisque, sem mi fringilla ante, vel vestibulum arcu ligula eu nisl. Suspendisse potenti. Nullam vitae eros a tortor consequat pharetra sit amet ac metus.

### Midiendo la calidad del agua

Etiam viverra, elit dapibus convallis finibus, lacus leo fermentum nisl, et porttitor diam risus in odio. Sed tincidunt congue volutpat. Sed hendrerit odio at sem posuere dignissim. Aliquam a feugiat quam, sed aliquet odio. Curabitur leo sapien, ullamcorper eget mauris et, fermentum lacinia nulla. Morbi vel facilisis metus. In pretium orci ac massa aliquet, ut sollicitudin urna tempor. Etiam imperdiet in ipsum non porttitor.

Quisque non vestibulum augue. Vivamus mauris mi, ultrices non mollis sed, viverra in lectus. Aenean vitae turpis ligula. Vivamus vel lectus quis lorem cursus pretium in quis nibh. Suspendisse convallis urna vel libero dictum malesuada. Pellentesque dignissim a libero et ullamcorper. Nam dignissim euismod tristique.

### Midiendo la calidad del aire

Etiam viverra, elit dapibus convallis finibus, lacus leo fermentum nisl, et porttitor diam risus in odio. Sed tincidunt congue volutpat. Sed hendrerit odio at sem posuere dignissim. Aliquam a feugiat quam, sed aliquet odio. Curabitur leo sapien, ullamcorper eget mauris et, fermentum lacinia nulla. Morbi vel facilisis metus. In pretium orci ac massa aliquet, ut sollicitudin urna tempor. Etiam imperdiet in ipsum non porttitor.

### Comprobado si el depostio tiene agua

Etiam viverra, elit dapibus convallis finibus, lacus leo fermentum nisl, et porttitor diam risus in odio. Sed tincidunt congue volutpat. Sed hendrerit odio at sem posuere dignissim. Aliquam a feugiat quam, sed aliquet odio. Curabitur leo sapien, ullamcorper eget mauris et, fermentum lacinia nulla. Morbi vel facilisis metus. In pretium orci ac massa aliquet, ut sollicitudin urna tempor. Etiam imperdiet in ipsum non porttitor.

### Regando

Etiam viverra, elit dapibus convallis finibus, lacus leo fermentum nisl, et porttitor diam risus in odio. Sed tincidunt congue volutpat. Sed hendrerit odio at sem posuere dignissim. Aliquam a feugiat quam, sed aliquet odio. Curabitur leo sapien, ullamcorper eget mauris et, fermentum lacinia nulla. Morbi vel facilisis metus. In pretium orci ac massa aliquet, ut sollicitudin urna tempor. Etiam imperdiet in ipsum non porttitor.

### Circuito completo

Etiam viverra, elit dapibus convallis finibus, lacus leo fermentum nisl, et porttitor diam risus in odio. Sed tincidunt congue volutpat. Sed hendrerit odio at sem posuere dignissim. Aliquam a feugiat quam, sed aliquet odio. Curabitur leo sapien, ullamcorper eget mauris et, fermentum lacinia nulla. Morbi vel facilisis metus. In pretium orci ac massa aliquet, ut sollicitudin urna tempor. Etiam imperdiet in ipsum non porttitor.

## Software

Ahora que tenemos todo el Hardware montado es el momento de añadirle al ESP32 el software que sea capaz de gestionar todo ello y darle la coherencia necesaria. Es decir, que sepa que tiene activar los humidificadores en caso de que la humedad sea baja, o los ventiladores para hacer descender la temperatura cuando sea necesario, regar si la tierra esta seca, y en general llevar a cabo las tareas para las que estamos desarrollando todo esto.


### Sin Home Assistant

[![status: Discontinuded](https://github.com/GIScience/badges/raw/master/status/archive.svg)](https://github.com/GIScience/badges#discontinued )

Inicialmente comencé creando un programa dentro del porpio ESP32. Además del control autonomo exponia una web en la que podian verse las lecturas de los distintos sensores y accionar los actuadores de forma manual.

Pero en mi busqueda de simplificar mi vida pronto abandone esta idea y me decante por delegar al gestión y la lógica en mi instalación de Home Assistant. Esto me permite realizar la gestión desde esta plataforma y mantenerla integrada con la domotica de la casa. Lo cual me resulta muy cómodo.

Pero si no tienes una instalación de home assitant o no quieres realizar esta integración te explio como lo monté, no deja de ser un boceto de lo que podría ser, si quieres contribuir [Este es el repositorio en el que se encuentra](https://github.com) y las aportaciones son bienvenidas.

```c
```

### Home Assistant

Esta es la versión que actualmente tengo en funcionamiento en todos los invernaderos que utilizo. Lo que hice fue cargar [ESPHome](https://esphome.io/) en el ESP32 y configurarlo con el siguiente yamel para poder acceder a todos los sensores y actuadores:

```yml
version: '2'

services:
  jekyll:
    image: jekyll/jekyll:latest
    command: jekyll serve --watch --force_polling --verbose
    ports:
      - 4000:4000
    volumes:
      - .:/srv/jekyll
```

A partir de aquí puedo visualizar la información directamente en Home Assistant y utilizar las automatizaciones para controlar las distintas funciones dependiendo de las lecturas registradas. Además permite actualizar el sofwtware del ESP32 sin necesidad de conectarlo por cable, lo que me evita tener que mover el invernadoro una vez situado en su ubicación final.

## Galeria de imagenes

{% include gallery caption="Imagenes del invernadero 2.0" %}
