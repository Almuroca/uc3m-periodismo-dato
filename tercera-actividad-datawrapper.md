# TERCERA ACTIVIDAD GRÁFICO DATAWRAPPER

![#FelizMartes Junio 2020](/imagenes/ejercicio3.png)

## ¿POR QUÉ UN GRÁFICO DE BARRAS?

El objetivo de este trabajo consiste en realizar un análisis del 
desarrollo de #FelizMartes durante el mes de junio de 2020. Por 
eso, el gráfico más apropiado para reflejar dicha evolución es uno 
de barras, ya que refleja de forma más visual cuan utilizado es 
este hastag a lo largo del mes.

## PROCESO DE SELECCIÓN

En primer lugar, es necesario localizar #FelizMartes en el archivo 
feliz.csv y para ello, he realizado una faceta de texto. El 
problema se encuentra en que hay más de una forma de escribir este 
tweet (#Feliz Martes, #FelizMartesAtodos). Por ello, se recurre al 
cluster para fusionar todas las formas en una sola; #FelizMartes. 
He elegido analizar este hastag porque existen estudios que 
confirman que el martes se considera el peor día de la semana, 
además es el más repetido según el archivo csv. Por otro lado, he 
escogido el mes de junio porque es el mes en el que más se repetía 
el hastag, para saber esto he realizado faceta de texto en la 
columna que he añadido de "Mes". He considerado oportuno añadir 
una columna más ya que con las fechas en general era muy 
complicado trabajar. Para incluir esta columna me he basado en la 
de los días y a través del juego con las estrellas, las facetas de 
estrellas y la transformación de value.replace incluí los meses. 
Lo que me ha resultado un poco más complicado ha sido agrupar los 
datos del mismo día. Por eso, he dejado en la gráfica el número de 
los tweets del día, no el conjunto de ellos. No obstante, como necesitaba solo los días del jueves tuve que añadir una columna más con los días como tal eliminando la parte final que acompañaba a los días.

Por último subí el csv al Datawrapper y utilicé solo dos columnas, 
la de "Días" y la "Cantidad de Tweets". A continuación elegí el gráfico de columnas y modifiqué un poco los datos para que aparecieran más claros. También escogí el color azul porque estábamos hablando de Twitter. 
A continuación incluí la gráfica a mi carpeta imagenes del Github desde la terminal y publiqué este texto con el editor de texto nano y lo subí también a mi Github. 