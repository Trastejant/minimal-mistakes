---
layout: splash
header:
    image: /assets/images/lowconsumption.png
title:  Código y Consumo
---                


Llevo mucho tiempo queriendo hacerme eco de un articulo que vi hace tiempo, concretamente este. En él se habla de la relación entre la forma en la que programamos y el consumo del «cacharro» que estemos programando, por ejemplo, un Arduino o una Raspberry Pi. 
No solemos pararnos a pensar mucho en esta relación, pero en cuanto nos abren los ojos todo cuadra. No puede ser lo mismo  que el microcontrolador tenga que hacer mil iteraciones a que tenga que hacer una docena. Incluso a nivel de carga de trabajo no todas las tareas requieren el mismo esfuerzo y, por lo tanto, esto tiene que repecutir de alguna manera en el consumo que tiene nuestro micro. 
Esto puede no ser muy critico cuando sabemos que nuestro proyecto va a estar conectado a la corriente de la casa o directamente via USB. A fin de cuentas, los consumimos máximos de estos dispositivos no van a engrosar demasiado nuestra factura de la luz. Pero cuando pensamos en proyectos que tienen que ser alimentados por baterías, o por paneles solares (últimamente estoy muy volcando en este tema, espero poder escribir dentro de poco al respecto) la cosa cambia mucho. 
En el articulo que comentaba anteriormente se hizo un experimento muy sencillo, se cargó el siguiente código: 
volatile int a, b = 123, c= 321; void setup(){    cli();//Eliminar las interrupciones } void loop(){     for(word i = 0; i<50000; i++){        a = b * c;     }    for(word i = 0; i<5000; i++){     a = b <<c;    } }
Se usan variables volatiles para que el compilador no las optimice, lo que podría afectar a los resultados del experimento. También se desactivan las interrupciones por el mismo motivo. Por supuesto se prescinde de cualquier tipo de modo de bajo consumo. 
En el loop se crean dos bucles, uno de ellos realiza una multiplicación, el otro realiza un desplazamiento a nivel de bit. El motivo por el que no se realizan el mismo número de veces responde a la cómo funciona internamente el Attiny. A diferencia de otros microcontroladores que realizan los desplazamientos a nivel de bit usando barrel shifter Arduino lo hace realizando un pequeño bucle internamente. Las iteraciones necesarias para realizar esta operación más las veces que tiene que realizarla suponen, a nivel de ciclos de trabajo, más o menos lo mismo. Por ello podríamos decir que ambos bucles se realizan, más o menos, el mismo número de veces.
Entendido el código veamos que resultados muestra cuando ponemos el osciloscopio y medimos su consumo: 
Imagen sacada del post original: https://jeelabs.org/2012/06/13/code-vs-power-consumption/
Resultados del experimento
A simple vista vemos que hay mucha diferencia entre el consumo de un bucle y del otro. De la mitad hacia la izquierda, con un consumo muy superior encontramos el bucle que realiza la multiplicación, a la derecha está el de desplazamiento. La diferencia, a simple vista es significativa, pero lo es aún más si atendemos a las explicaciones que aportan en el experimento, en el cual se detalla lo siguiente: 
El primer bucle ( el de multiplicar) necesita 93.48 ms para realizar las 50.000 iteraciones. Por lo tanto cada una de ellas lleva unos 1.8 µs Por su parte el desplazamiento, pese a ser muchas menos iteraciones, debido a la forma en la que Arduino lo realiza de forma interna requiere 108.52 ms para completarse, lo que significa que cada vuelta del bucle requiere 21,8 µs
Dicho de otra manera, el segundo bucle consume menos a pesar de tardar muchísimo más en completarse. Lo cual es aun más espectacular. 
Sobre esto creo que se podría escribir y experimentar muchísimos. Y nos muestra que la clave para crear proyectos de bajo consumo reside no solo en una buena gestión de los tiempos de deep sleep, sino también en qué y cómo lo hacemos en el tiempo que nuestro dispositivo está despierto. 


