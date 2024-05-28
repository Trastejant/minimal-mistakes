---
title: "PANTALLA NOKIA 3310/5110"
layout: single
header:
  overlay_color: "#000000"
  image: /assets/images/nokia_3310/3310.png
excerpt: "Aprende a controlar una pantalla como la que llevaban los Nokia 3310 para mostrar información de tu proyecto."

toc: true
toc_label: "Pasos"
toc_icon: "cog"

---

{% include video id="8Yl7PG-Dxq4" provider="youtube" %}

## Introducción

Creo que a no me equivoco al afirmar que a todos nos encantan las pantallas en nuestros proyectos. Es una forma elegante y vistosa de mostrar la información y le da un acabado profesional a cualquier montaje.

Anteriormente ya vimos como conectar un display de 16×2 a nuestro Arduino, pero hay veces que esto se nos queda un poco pequeño. Entonces es el momento de apostar más fuerte y emplear pantallas que nos permitan más lineas, o incluso, mostrar gráficos.

Para ello, una solución económica y sencilla es utilizar una pantalla como las que llevaba el mítico Nokia 3310 (el mismo de los modelos 5110). Que nos permite nada menos que 84 x 84 pixeles. Se pueden sacar de un teléfono viejo o adquirirlas directamente en tiendas.

## Conexión

Conectar esta pantalla con Arduino es muy sencillo, y únicamente tenemos que tener una cosa importante: Estas pantallas funcionan a 3.3V, así que NO PODEMOS ALIMENTARLAS CON 5V O LA DAÑAREMOS.

![image-center](/assets/images/nokia_3310/3310_conexiones.png){: .align-center}

| Pin Arduino  | Pin del LCD  |
|---|---|
| 3.3V  | VCC |
| GND  | GND |
| 7  | SCE |
| 6  | RST |
| 5  | D/C |
| 4  | DN |
| 3  | SCLK |
| 1  | Iluminación |

Como podemos ver, ha que conectar la alimentación de la pantalla a las salidas de 3.3V y GND de arduino, el resto a salidas digitales y el ultimo pin (cable ) es la alimentación de la retro-iluminación. Si queremos mantenerla encendida siempre podemos conectarla a la salida de 5V, pero nos ha parecido más interesante conectarla a una salida digital de Arduino y poder controlar el encendido y apagado por software.

## Programación

Si conectar la pantalla a Arduino ha sido fácil, controlarla lo será aun más gracias a la Librería Nokia. Si la descargamos desde Trastejant vendrá ya preparada para las versiones nuevas del compilador de Arduino y únicamente tendremos que instalarla.

Vamos a probar el montaje usando el código que trae la librería como ejemplo:

```java
#include <nokialcd.h>
 
NokiaLCD NokiaLCD(3,4,5,6,7); // (SCK, MOSI, DC, RST, CS) 
 
void setup() 
{ 
 Serial.begin(9600); 
 NokiaLCD.init(); // Init screen. 
 NokiaLCD.clear(); // Clear screen. 
} 
 
void loop() 
{ 
 NokiaLCD.setCursor(1,1); 
 NokiaLCD.print("Hello World!"); 
 
 NokiaLCD.setCursor(4,2); 
 NokiaLCD.print("Nokia 3310"); 
 
 NokiaLCD.setCursor(30,3); 
 NokiaLCD.print("con"); 
 
 NokiaLCD.setCursor(15,4); 
 NokiaLCD.print("Arduino"); 
}
```

Y en nuestra pantalla aparecerá esto:

![image-center](/assets/images/nokia_3310/3310_conexiones.png){: .align-center}

### La librería Nokia

Ahora que ya tenemos la pantalla funcionando vamos a ver las funciones que nos ofrecerte la librería Nokia para sacarle el máximo partido.

#### NokiaLCD NokiaLCD 

Crea un objeto de la librería NokiaLCD para que podamos usar sus funciones (en este caso el objeto se llamará NokiaLCD) y asigna los pines, los cuales recibe como parametro (SCK, MOSI, DC, RST, CS).

Ejemplo:

```java
NokiaLCD NokiaLCD (3,4,5,6,7);
```

#### init()

Inicializa el LCD

Ejemplo:

```java
NokiaLCD.init();
```

#### Clear

Borra la pantalla y situa el cursor en la posición inicial.

Ejemplo:

```java
NokiaLCD.clear();
```

#### setCursor(x,y)
Con esta función podemos colocar el cursos en la posición que queramos para que empiece a escribir desde allí.

Ejemplo:

```java
NokiaLCD.setCursor(5,2);
```

#### print(String)

Escribe una cadena de caracteres en pantalla, podemos enviar tanto una variable cómo una cadena constante.
Ejemplo:

```java
NokiaLCD.print(“Hola Mundo”);
```

#### character(caracter)

Escribe un unico carácter en pantalla.
Ejemplo:

```java
NokiaLCD.character(‘T’);
```

#### Mostrar imágenes

Como ya dijimos antes, estas pantallas nos permiten incluso mostrar imágenes. Para ello tendremos que convertir una imagen en BMP a un Array de Bytes. Existen varias herramientas para hacer esto, pero aquí vamos a mencionar únicamente dos: bitmap_converter de en.radzio.dxp.pl y Nokia BMP Loader de Cuningan e iPadnano. Esta ultima en castellano y de muy fácil uso.
Una vez tenemos la imagen convertida en un array tenemos dos opciones, podemos introducir en nuestro código un array de Bytes con nuestra imagen y después mostrarla en pantalla con la función bitmap(array):

Ejemplo:

```java
Byte array[] = {0xff, 0xff, 0xff, 0xff, 0xff, 0xff, 0xff, 0xff, 0xff, 
0xff, 0xff, 0xff, 0xff, 0xff, 0xff,0xff, 0xff, 0xff, 0xff, 0xff, 0xff, 
0xff, 0xff, 0xff, 0xff, 0xff, 0xff, 0xff, 0xff, 0xff, 0xff, 0xff, 0xff, 
0xff, 0xff, 0xff, 0xff, 0xff, 0xff, 0xff, 0xff, 0xff, 0xff, 0xff, 0xff, 
0xff, 0xff, 0xff, 0xff, 0xff, 0xff, 0xff, 0xff, 0xff, 0xff, 0xff, 0xff, 
0xff, 0xff, 0xff, 0xff, 0xff, 0xff, 0xff, 0xff, 0xff, 0xff, 0xff, 0xff, 
0xff, 0xff, 0xff, 0xff, 0xff, 0xff, 0xff, 0xff, 0xff, 0xff, 0xff, 0xff, 
0xff, 0xff, 0xff, 0xff, 0xff, 0xff, 0xff, 0xff, 0xff, 0xff, 0xff, 0xff, 
0xff, 0xff, 0xff, 0xff, 0xff, 0xff, 0xff, 0xff, 0xff, 0xff, 0xff, 0xff, 
0xff, 0xff, 0xff, 0xff, 0xff, 0xff, 0xff, 0xff, 0xff, 0xff, 0xff, 0xff, 
0xff, 0xff, 0xff, 0xff, 0xff, 0xff, 0xff, 0xff, 0xff, 0xff, 0xff};
```

#### NokiaLCD.bitmap(array);

O enviarla via serial y usar la función sBitmap():
Ejemplo:

```java
NokiaLCD.sBitmap();
```

Con esto ya tienes todo lo que necesitas para incorporar una pantalla gráfica a tus proyectos.