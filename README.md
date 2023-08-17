# Análisis de cancelaciones.

**Prueba técnica de la compañia GETT**

Proyecto de bussines analytics para mejorar el servicio de la compañía de transporte israelí GETT. 

## Índice

1. [Introducción](#introducción)
2. [Estructura](#estructura)
3. [Conclusiones](#resultados)

## Introducción

La empresa GETT quiere mejorar el servicio de transporte para evitar al máximo las cancelaciones de viajes, en la ciudad inglesa de Reading. Para ello, se proporciona un dataset que contiene información sobre las cancelaciones producidas; longitud y latitud, segundos entre la reserva y la cancelación, si tenía conductor reservado o no, etc.

## Estructura

El análisis se ha desarrollado en el notebook [Data Analysis](Notebooks/Data%20analysis.ipynb) y para ayudar a la empresa a buscar soluciones, se han respondido a las siguientes preguntas:

1) ¿Las cancelaciones se producen antes o después de asignar un conductor?
2) Trazar la distribución de pedidos fallidos por horas. ¿Existe una tendencia a que determinadas horas tengan una proporción anormalmente alta de una u otra categoría? ¿A qué horas se producen la mayoría de cancelaciones?
3) Trace el tiempo medio hasta la cancelación con y sin conductor, por horas. Si hay valores atípicos en los datos, sería mejor eliminarlos. ¿Podemos sacar alguna conclusión de este gráfico?
4) Traza la distribución del tiempo medio de llegada por horas. ¿Cómo se explica este gráfico?
5) Se ha graficado un mapa con los lugares donde más cancelaciones se producen.

#### ¿Las cancelaciones se producen antes o después de asignar un conductor?.
Dentro de la primera parte, los notebooks, se tienen dos archivos .ipynb:

- data_clean: En esta primera parte se unen los diferentes archivos, se eliminan nulos, se codifican los valores categóricos y se escalan los valores para su uso posterior.
- models: En este notebook se divide el dataframe obtenido en el notebook anterior para su entrenamiento y test, y se prueban los algoritmos Random Forest y linear regression. Se calculan las métricas MAE y R² y se hace una grafica comparando los valores reales con los predichos por el modelo.

#### ¿A qué horas se producen la mayoría de cancelaciones?

#### Tiempo medio hasta la cancelación con y sin conductor, por horas.

#### Tiempo medio desde la reserva a la llegada 

#### Mapa de zonas con mas cancelaciones. 
