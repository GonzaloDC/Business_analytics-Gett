# Análisis de cancelaciones de viajes.

**Prueba técnica de la compañia GETT**

Proyecto de bussines analytics para mejorar el servicio de la compañía de transporte israelí GETT. 

## Índice

1. [Introducción](#introducción)
2. [Estructura](#estructura)
3. [Conclusiones](#conclusiones)

## Introducción

La empresa GETT quiere mejorar el servicio de transporte para evitar al máximo las cancelaciones de viajes, en la ciudad inglesa de Reading. Para ello, se proporciona un dataset que contiene información sobre las cancelaciones producidas; longitud y latitud, fecha de la cancelación, segundos entre la reserva y la cancelación, si tenía conductor reservado o no, etc.

## Estructura

El análisis se ha desarrollado en el notebook [Data Analysis](Notebooks/Data%20analysis.ipynb). Para ayudar a la empresa a buscar soluciones, se han respondido las siguientes preguntas:

1) ¿Las cancelaciones se producen antes o después de asignar un conductor?
2) Distribución de cancelaciones por horas. ¿Existe una tendencia de cancelaciones en algún momento del día? ¿A qué horas se producen la mayoría de cancelaciones?
3) Tiempo medio hasta la cancelación con y sin conductor, por horas. ¿Se puede sacar alguna conclusión de este gráfico?
4) Tiempo medio de llegada por horas. ¿Cómo se explica este gráfico?
5) Mapa con los lugares donde más cancelaciones se producen.

#### 1) ¿Las cancelaciones se producen antes o después de asignar un conductor?.

Para saber la distribución de cancelaciones (que pueden ser por el cliente o por el sistema de GETT) se ha graficado el número de éstas diferenciando entre conductor asignado o no:

[Cancelaciones por conductor asignado](artifacts/img/cancelacion%20conductor%20asignado.png)

Como se puede comprobar, una vez que un conductor es asignado, el sistema prácticamente no cancela ninguna reserva. La mayoría de las cancelaciones se producen cuando no se asigna conductor.

#### 2) Distribución de cancelaciones por horas. ¿Existe una tendencia de cancelaciones en algún momento del día? ¿A qué horas se producen la mayoría de cancelaciones?

Veamos, por horas, la distribución de cancelaciones:

[distribución de cancelaciones por hora](artifacts/img/maxima%20cancelacion%20hora.png)

Según el gráfico, la hora con mayor número de cancelaciones se da a a las 8 de la mañana, seguido de las 21, 22 y 23 horas. Las horas de madrugada entre las 3 y las 12, también tienen un número alto de cancelaciones. 

#### 3) Tiempo medio hasta la cancelación con y sin conductor, por horas. ¿Se puede sacar alguna conclusión de este gráfico?

Veamos la distribución del tiempo (en segundos) de cancelación de la reserva: 

[tiempo de cancelacion](artifacts/img/tiempo%20de%20cancelacion.png)

el 75% de las cancelaciones se producen por debajo de los 154 segundos, mientras que el valor más frecuente son 85 segundos desde que se reserva. Para ver el tiempo de cancelacion por horas:

[tiempo de cancelacion por horas](artifacts/img/cancelacion%20en%20tiempo%20por%20hora.png)

Por regla general, el tiempo trascurrido para cancelar es mayor si hay conductor asignado.

#### 4) Tiempo medio de llegada por horas. ¿Cómo se explica este gráfico?

[tiempo medio de llegada](artifacts/img/tiempo%20transcurrido%20entre%20recogida.png)

El tiempo entre recogidas aumenta considerablemente a las 7, 8 y 17 horas. Esto indica que durante los horarios de entrada y salida del trabajo se produce un tráfico más denso, con el consiguiente retraso a la hora de recoger al cliente.


#### 5) Mapa con los lugares donde más cancelaciones se producen.

El siguiente mapa se ha creado usando las librerias Folium y h3. Los hexágonos muestran dónde se producen el 80% de las cancelaciones en la ciudad de Reading:

[mapa](artifacts/img/mapa.JPG)

Se puede observar que el principal punto de cancelaciones es el centro de la ciudad. 

## Conclusiones

Para mejorar el sistema de transporte, se propone lo siguiente:

- Aumentar el número de conductores en la zona centro de la ciudad en contra de la periferia.
- Incentivar el servicio en horario de jornada laboral, es decir, entre las 7 y las 9 horas, y a partir de las 17 horas.
- Diferenciar el número de conductores entre semana (mayor número durante horario matinal) y el fin de semana (más numero de conductores en horario comprendido entre las 22 y las 3 de la madrugada)