# openMultiPowerMeter_random
Muestras aletaorias de 5 electrodomesticos más el agregado usando el OMPM  ( equipo de medida propio  basados en un bus RS485 con modulos PZEM004) entre  las 14:49 y las 18:07

El sentidio de las muestras aleatorias es intentar comprender si mejoran las metricas con tiempos de encendido /apagdos mas cortos.

En este sentido  hay tres criterios de aleatoriedad:

- La secuecia de aplicativos para encender (un numero aletaorio entre 0 y 33).

- Tiempo pausa : entre  10 y 60 segundos.

- Tiempo encendido ; eentre 1 y 5 minutos.

El periodo de entrenamiento/val y test  es 60/20/20, es decir : 

- Entrenamiento :de 14:49 a 16:19

- Validacion : de 16:19 a 17:13

- Test: de 17:13 a 18:07



