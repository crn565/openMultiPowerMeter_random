# openMultiPowerMeter_random
Muestras aletaorias de 5 electrodomesticos más el agregado usando el OMPM  (equipo de medida propio  basados en un bus RS485 con modulos PZEM004) entre  las 14:49 y las 18:07.

El sentidio de las muestras aleatorias es intentar comprender si mejoran las metricas con tiempos de encendido /apagados mas cortos.

En este sentido  hay tres criterios de aleatoriedad:

- La secuecia de aplicativos para encender (un numero aletaorio entre 0 y 33 que convertimos en binario para activar/desactivar los aplicativos).

- Tiempo pausa: entre  10 y 60 segundos.

- Tiempo encendido: entre 1 y 5 minutos.

El periodo de entrenamiento,validacion  y test  se hace en la proporcion 60/20/20, es decir : 

- Entrenamiento :de 14:49 a 16:19

- Validacion : de 16:19 a 17:13

- Test: de 17:13 a 18:07

# Resultados Metricas  con algoritmo CO, metodo Median  y 10"

## Datos anteriores con secuencia fija

| Metrica          | Fryer   | LED Lamp | Incandescent lamp | Laptop Computer | Fan     | Media Aritmética |
|-----------------|---------|----------|------------------|----------------|---------|------------------|
| F1              | 0.420   | 0.789    | 0.756            | 0.453           | 0.741   | 0.632            |
| EAE            | 0.002   | 0.001    | 0.011            | 0.002           | 0.012   | 0.006            |
| MNEAP       | 1.138   | 0.349    | 0.484            | 1.150           | 0.502   | 0.725            |
| RMSE        | 17.417 | 7.339     | 22.688         | 13.816         | 12.651 | 14.382           |



## Datos actuales con muestras aleatorias 

| Metrica          | Fryer   | LED Lamp | Incandescent lamp | Laptop Computer | Fan     | Media Aritmética |
|-----------------|---------|----------|------------------|----------------|---------|------------------|
| F1              | 0.591   | 0.158    | 0.752            | 0.349           | 0.577   | 0.485            |
| EAE            | 0.000 | 0.005   | 0.005             | 0.003          | 0.001  | 0.002             |
| MNEAP       | 0.726   | 1.596     | 0.443            | 1.212           | 0.823   | 0.960            |
| RMSE        | 11.169 | 9.259     | 18.718          | 8.170           | 15.660 | 12.995           |



Tabla


| Metrica          | Fryer   | LED Lamp | Incandescent lamp | Laptop Computer | Fan     | Media Aritmética |
|-----------------|---------|----------|------------------|----------------|---------|------------------|
| F1	| 0.591| 	0.158| 	0.752| 	0.349| 	0.577| 
| EAE	| 0.000| 	0.000	| 0.000| 	0.000| 	0.000| 
| MNEAP	| 0.726| 	1.596| 	0.443| 	1.212| 	0.823| 
| RMSE	| 11.169| 	9.259| 	18.718| 	8.170| 	15.660| 
En el formato Markdown, un título se crea usando uno o más s




# Interpretacion de los resultados

En cuanto a la métrica F1, que mide la precisión y exhaustividad del modelo, el primer dataset tomado  con secuencia fija tiene valores más altos para todos los dispositivos, lo que sugiere un mejor desempeño en términos generales.

En cuanto a la métrica EAE, que mide el error absoluto medio, este dataset tiene valores más bajos para todos los dispositivos, lo que sugiere que los resultados de este dataset son más precisos.

En cuanto a la métrica MNEAP, que mide el error absoluto medio normalizado por la potencia aparente media, este dataset tiene valores más bajos para la mayoría de los dispositivos, lo que sugiere que este dataset se comporta mejor en términos de precisión de la predicción.

En cuanto a la métrica RMSE, que mide el error cuadrático medio, este dataset tiene valores más bajos para tres de los cinco dispositivos, lo que sugiere que los resultados de este dataset son más precisos en términos de la magnitud del error.

Teniendo en cuenta todos estos factores, no es posible determinar de forma clara cuál de los dos datasets se comporta mejor en general. Depende de los criterios específicos que se quieran priorizar en la evaluación del desempeño del modelo.


