---
layout: splash
header:
  image: /assets/images/arduino-yun.jpg
title: Arduino Yun
---

Hoy os traigo un poco de información sobre esta nueva placa de Arduino, la Arduino Yun que estará disponible a finales de mes.

No es necesario hablar del potencial que posee Arduino, ni de sus miles de aplicaciones, pero si hablamos de colectividad, la cosa se complica un poco. Si bien es verdad que existen shields para dotar a Arduino de una conexión a Internet, bien sea por cable ethernet o por Wifi lo cierto es que las limitaciones de memoria Ram y de las propias características de Arduino complican realizar proyectos que utilicen la nube. Para salvar esta limitación nace Arduino Yun.

En esencia Arduino Yun es un Arduino leonardo con dos añadidos importantes, por un lado incorpora una conexión Arduino Yun PinoutWifi y por otro lleva embebido Linux, concretamente la distribución Linino. Esto abre un mundo de posibilidades en cuanto a conectividad y potencia a la hora programar y realizar proyectos más complejos.

<figure style="width: 300px" class="align-right">
  <img src="{{ site.url }}{{ site.baseurl }}/assets/images/arduinoYun.png" alt="">
  <figcaption>Feels good to be right all the time.</figcaption>
</figure> 

En cuanto al resto de sus características se trata, como ya hemos dicho, de un Arduino Leonardo cuenta con 14 entradas/salidas digitales (7 pueden ser usadas cómo canales PWM), 12  analógicas y tiene una velocidad de 16Mhz. Cómo añadidos, a parte del wifi, la versión Yun incluye una ranura para tarjetas microSD.

Cuando se conecta la Arduino Yun esta aparece para nuestros dispositivos cómo un punto de acceso wiffi, de esta forma podemos conectarnos a ella. En cuanto a programación, se puede programar con sketches cómo cualquier otra tarjeta de Arduino, pero lo verdaderamente interesante es que mediante la librería Bridge se puede interactuar con el Linino embebido, lo que nos permite utilizar la potencia de Linux para ejecutar programas en él que interaccionen con los periféricos conectados al Arduino Yun.

En cuanto al precio, se habla de que rondará los 69€, habrá que esperar aun un poco más para descubrir todo el potencial de esta nueva placa.

