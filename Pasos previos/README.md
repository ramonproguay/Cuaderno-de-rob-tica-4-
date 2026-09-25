# Reto 1: Encendido alternativo de dos diodos led.
El reto trata de conseguir encender un diodo Led mientras que el otro esta apagado así sucesivamente.
El programa se hace con un Arduino conectando los cables a una Placa de pruebas.

[Pincha aquí para ver la prueba en tinkercad](https://www.tinkercad.com/things/7CJUpBiHZaA-arduino/editel?returnTo=https%3A%2F%2Fwww.tinkercad.com%2Fdashboard)

La Prueba con Tinkercad:







<p align="center">
<img src="Imágenes/xjdsfhudxzgghsaghczuhjzscgcyjs.PNG" width="800" height="600" />
</p>



El Código:

Este programa controla dos LEDs conectados a Arduino.
Primero configura los pines 2 y 3 como salidas.
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

