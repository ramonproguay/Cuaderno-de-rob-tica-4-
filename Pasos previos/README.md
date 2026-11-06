# Reto 1: Encendido alternativo de dos diodos led.
El reto trata de conseguir encender un diodo Led mientras que el otro esta apagado así sucesivamente.
El programa se hace con un Arduino conectando los cables a una Placa de pruebas.

[Pincha aquí para ver la prueba en tinkercad](https://www.tinkercad.com/things/7CJUpBiHZaA-arduino/editel?returnTo=https%3A%2F%2Fwww.tinkercad.com%2Fdashboard)

**La Prueba con Tinkercad:**

El circuito tiene un Arduino conectado a dos LEDs mediante una protoboard. El programa hace que los dos LEDs se enciendan y apaguen alternativamente cada 1 segundo.

El Arduino es el cerebro del circuito y controla los Leds.

La Protoboard sirve para montar y conectar los componentes sin soldar.

Los leds se encienden cuando reciben corriente.

La resistencia limita la corriente para proteger los Leds.

Los cables conectan el Arduino con los diferentes componentes.

El cable USB alimenta el Arduino y permite cargar el programa desde el ordenador.








<p align="center">
<img src="Imágenes/xjdsfhudxzgghsaghczuhjzscgcyjs.PNG" width="400" height="400" />
</p>



**El Código:**

Este programa controla dos LEDs conectados a Arduino.
Primero configura los pines 2 y 3.
Después enciende el LED del pin 2 y apaga el del pin 3.
Espera 1 segundo antes de cambiar.
Luego apaga el pin 2 y enciende el pin 3.
Este proceso se repite continuamente.

OUTPUT significa que el pin controla un componente

HIGH significa encendido

LOW significa apagado

pinMode sirve para decirle a Arduino cómo se va a usar un pin

digitalWrite sirve para poner un pin en HIGH o LOW

delay(1000) hace que Arduino espere 1 segundo antes de continuar




<p align="center">
<img src="Imágenes/Captura de pantalla 2026-09-24 173010.png" width="400" height="400" />
</p>




**Así quedaría el Reto 1:**


<a href="https://www.youtube.com/watch?v=2f6OHwZokGQ" target="_blank">
<img src="https://img.youtube.com/vi/2f6OHwZokGQ/hqdefault.jpg" width="500">
</a>

Vídeo realizado por (Lorenzo/@LorenRobótica879)

Licencia estandar de Youtube.

# Reto 2: Encendido de diodos led con pulsador.
**El Código:**

Este programa sirve para encender y apagar una luz LED usando un pulsador.

Primero, le decimos a Arduino que el LED está conectado al número 13 y el pulsador al número 2. 
Después, Arduino prepara el pulsador para recibir información y el LED para encenderse o apagarse.
Luego, Arduino comprueba continuamente si estamos pulsando el botón.

Si el botón **está pulsado, el LED se apaga**

Si **no estamos pulsando el botón, el LED se enciende.**

Todo esto se repite continuamente para que pueda saber siempre qué está pasando.
 

<p align="center">
<img src="Imágenes/Captura.PNG" width="450" height="450" />
</p>


**La Prueba:**

El circuito tiene un Arduino conectado a un LED mediante una protoboard. El programa trata de de si presionas el pulsador el LED se apaga y si no lo presionas el LED esta siempre encendido.

El Arduino es el cerebro del circuito.

La Protoboard sirve para montar y conectar los componentes sin soldar.

El leds se encienden esta siempre enciendo.

La resistencia limita la corriente para proteger el LED.

Los cables conectan el Arduino con los diferentes componentes.

El cable USB alimenta el Arduino y permite cargar el programa desde el ordenador.



<p align="center">
<img src="Imágenes/captura 2.png" width="1050" height="1050" />
</p>

# Reto 3: Uso de un Potenciometro y el Monitor Serie

En esta práctica conectamos una placa al ordenador usando varios cables.

Después usamos un programa para ver los números que recibe la placa. Estos números pueden cambiar según la señal que recibe.

En el programa usamos analogRead() para leer los valores y Serial.println() para verlos en la pantalla. También usamos delay(500) para que espere medio segundo entre cada lectura.

**El Codigo:**

P2 = A2: indica la entrada analógica que se utiliza.

entrada: guarda el valor leído, entre 0 y 1023.

DutyCycle: guarda el valor convertido, entre 0 y 255.

Serial.begin(9600): inicia la comunicación con el ordenador.

analogRead(P2): lee el valor de la entrada A2.

map(): convierte el valor de 0-1023 a 0-255.

Serial.print(): muestra el resultado en el ordenador.

delay(500): espera medio segundo antes de repetir el proceso.



<p align="center">
<img src="Imágenes/tfgyhyt6rygt6rfgytrfgytgtg.PNG" width="250" height="250" />
</p>


**El Video:**

[![](https://img.youtube.com/vi/u_LzLcUyPQk/0.jpg)](https://www.youtube.com/watch?v=u_LzLcUyPQk)

Vídeo realizado por (Lorenzo/@LorenRobótica879)

Licencia estandar de Youtube.

# Reto 4:  Mapeado de datos del potenciómetro.
Este programa sirve para leer los valores de un potenciómetro conectado a la entrada A0 de Arduino y verlos en el ordenador.

**El Código:**

P1 = A0: indica que se utiliza la entrada analógica A0.

float valor = 0: crea una variable para guardar el valor leído.

Serial.begin(9600): inicia la comunicación con el ordenador.

analogRead(P1): lee el valor de la entrada A0, que puede ir de 0 a 1023.

Serial.println(valor): muestra el valor en el monitor serie y salta a la siguiente línea.

delay(500): espera medio segundo antes de repetir la lectura.




<p align="center">
<img src="Imágenes/POTENCIOMETRO.PNG" width="250" height="250" />
</p>

**El vídeo:**

[![](https://img.youtube.com/vi/FqHJXZcOIXY/0.jpg)](https://www.youtube.com/watch?v=FqHJXZcOIXY)

Vídeo realizado por (Lorenzo/@LorenRobótica879)

Licencia estandar de Youtube.


# Reto 5: PWM

En esta práctica usamos Arduino para controlar el brillo de un LED.

El programa lee un valor por el pin A0 y lo convierte en un número entre 0 y 255. Después, envía ese valor al pin 9 para cambiar el brillo del LED.

**El Código:**

<p align="center">
<img src="Imágenes/captura1.PNG" width="250" height="250" />
</p>


**1. Variables**

#define LED9 9: indica que el LED está conectado al pin 9.

int P1 = A0: indica que vamos a leer los valores del pin A0.

float valor = 0: guarda el valor que recibe el programa.

float DutyCycle: guarda el valor que se usará para controlar el LED.

**2. Función setup()**

pinMode(LED9, OUTPUT): prepara el pin 9 para controlar el LED.

Serial.begin(9600): permite enviar datos al ordenador para verlos en la pantalla.

**3. Función loop()**

valor = analogRead(P1): lee el valor que llega al pin A0.

DutyCycle = map(valor, 0, 1023, 0, 255): convierte el valor leído a otro entre 0 y 255.

Serial.println(DutyCycle): muestra el valor en el ordenador.

analogWrite(LED9, DutyCycle): controla el brillo del LED según el valor obtenido.

delay(100): espera 100 milisegundos antes de repetir el proceso.


**El vídeo:**

[![](https://img.youtube.com/vi/ZORLppsyEgE/0.jpg)](https://www.youtube.com/watch?v=ZORLppsyEgE)

Vídeo realizado por (Lorenzo/@LorenRobótica879)

Licencia estandar de Youtube.

# Reto 6: Ultrasonido

Este programa sirve para detectar si hay algún objeto cerca de un sensor. Si el objeto está a menos de 15 cm, se enciende una luz LED. Si está más lejos, la luz se apaga.

#include "Ultrasonic.h"

Esta línea sirve para añadir una librería que nos ayuda a utilizar el sensor ultrasónico y medir distancias.

define TRIG_PIN 12

define ECHO_PIN 11

Aquí indicamos dónde están conectados los cables del sensor en Arduino. El TRIG envía una señal y el ECHO recibe esa señal cuando rebota contra un objeto.
Ultrasonic OurModule(TRIG_PIN, ECHO_PIN);

Esta parte se ejecuta una sola vez cuando encendemos Arduino.

Serial.begin: sirve para conectar Arduino con el ordenador y ver los resultados.
Serial.println: muestra un mensaje que dice «Aviso a 15 cm».
pinMode: indica que el pin 13 se va a utilizar para encender y apagar el LED.
void loop()

Esta parte se repite todo el tiempo mientras Arduino está encendido.

Serial.print: mide la distancia del objeto en centímetros.
Serial.println: escribe cm después del número para saber que la distancia está en centímetros.
delay: hace que Arduino espere 100 milisegundos antes de continuar.

<p align="center">
<img src="Imágenes/Captura (1).PNG" width="250" height="250" />
</p>

Video:


[![](https://img.youtube.com/vi/EXzA4VjIh4Y/0.jpg)](https://www.youtube.com/watch?v=EXzA4VjIh4Y)

Vídeo realizado por (Lorenzo/@LorenRobótica879)

Licencia estandar de Youtube.
