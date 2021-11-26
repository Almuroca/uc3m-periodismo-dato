# Cuarta actividad: tu historia de periodismo de datos

## Datos seleccionados

He escogido un CSV del INE sobre la pobreza y variados de la misma en las Comunidades Autónomas de España durante los últimos trece años. De esta forma, aborda cuestiones como el riesgo de exclusión social o de pobreza, la tasa de carencia material severa y la de hogares con baja intensidad en el trabajo. 

Me parece un tema cuanto menos relevante e interesante para conocer las diferencias económicas que existen en España. Por todo ello, los gráficos realizados intentan mostrar de una manera visual la variedad económica que se produce en el país. 

## Gráficos realizados

### Tasa de riesgo de pobreza o exclusión social. 

![Tasa de riesgo de pobreza o exclusión social](/imagenes/tasa-de-riesgo-de-pobreza-o-exclusi-n-social-.png)

#### Análisis 

He realizado este gráfico de dispersión porque me parece la mejor manera de mostrar los cuatro componentes que recoge el CSV. Este gráfico se utiliza para relacionar dos variables, que en este caso serían la variable "X" que muestra la evolución temporal desde 2008 hasta 2020 y la variable "Y" que refleja la tasa de pobreza. 

Los elementos que aparecen en el gráfico aparecen representados con colores diferentes:
- Carencia material severa: en color gris ya que alude a bienes materiales. Este color es bastante neutro lo que permite que puedan entran muchos componentes en el mismo (ropa, muebles, comida)
- Riesgo de pobreza: aparece en color rojo ya que se relaciona con la atención, peligro o advertencia como vemos en señales de tráfico por ejemplo. 
- Riesgo de exclusión social: aparece en color negro puesto que se relaciona con algo negativo, algo oscuro o trágico.
- Vivir en hogares con baja intensidad en el trabajo: he puesto un color azul porque este color recuerda al  cumplimiento de la ley que recoge que todos tenemos derecho a una vivienda justa. 

Por todo ello, el gráfico puede resultar útil para deducir que la tasa más baja es la de "carencia de material severa" y la más elevada es la tasa de "riesgo de pobreza o exclusión social". Al mismo tiempo se aprecia que todas ellas contaron un pico ascendente en el año 2014. 


#### ¿Cómo se ha realizado esta gráfica?

Para empezar buscamos el CSV en el Instituto Nacional de Estadística (INE). A continuación lo exportamos en el OpenRefine y por medio de la faceta de texto en la primera columna "Comunidades y Ciudades Autónomas" seleccionamos la opción de "Total Nacional" dejando a parte el resto de Comunidades Autónomas porque lo importante es conocer la evolución anual de estos cuatro componentes a nivel nacional. 

![Faceta de texto](/imagenes/Capturadepantalla1.png)

A continuación, mediante la opción de transformas celdas, modifiqué los datos de la segunda columna, "Total", en números. El OpenRefine no reconoce las comas, así que tuve que sustituirlas por puntos. Para ello, utilicé la transformación personalizada e introduje la expresión "value.replace(",","."). Una vez realizado este paso, pude transformarlo en números mediante la opción transformaciones comunes. 

![Transformar en número](/imagenes/Capturadepantalla2.png)

Cuando tenía todos los datos que necesitaba los exporté en DataWrapper. En esta herramienta de visualización, escogí la opción de Gráfico de Dispersión y a través de la customización personalizada le proporcioné los colores que quise a la gráfica. 

### Tasa de riesgo de pobreza en España

#### Análisis

Las tres gráficas que muestro a continuación se centran en uno de los apartados mencionados anteriormente: el riesgo de pobreza.

![Tasa de riesgo de pobreza en España](/imagenes/tasa-de-riesgo-de-pobreza-en-españa.png)

La siguente gráfica es de flechas y resulta muy útil para ver que la que menor tasa de pobreza registra es la Comunidad Foral de Navarra, mientras que la que presenta una mayor tasa es Ceuta. Se convierte en un gráfico muy visual y cualquier periódico podría incluirlo en sus noticias pues de un golpe de vista se refleja la diferencia que existe en España.

Aparecen en orden de menor a mayor, ya que proporciona un mayor entendimiento. Resulta más visual y práctico mostrar una grada descendente y poner en primera posición la tasa más pequeña. No obstante, depende de dónde quiera poner el foco la noticia, si quiere centrarse en la Comunidad con menor tasa de pobreza lo ideal es colocarla el primera posición. Si por el contrario prefiere hablar de la tasa más elevada, sería mejor poner Ceuta en la parte superior, es decir, invertir el orden.

El color utilizado es el rojo, de nuevo por su simbología de peligro o aspecto negativo. Cuando uno dice que no tiene dinero, suele decir "estoy en números rojos". De ahí la elección del color.

Al mismo tiempo he optado por poner el título en minúsculas porque resulta menos agresivo y he dejado la nomenclatura que utilizaba el INE para referirse a cada Comunidad Autónoma (Madrid, Comunidad de, en vez de Comunidad de Madrid). 

#### ¿Cómo se ha realizado esta gráfica?

La gráfica presentada requiere un mayor nivel de limpieza que la anterior. Para realizarla he utilizado facetas de texto y transformaciones personalizadas.

En primer lugar, una vez exporté el CSV realicé una faceta de texto en la tercera columna "Tasa de riesgo de pobreza o exclusión social (y sus componentes) y seleccioné "En riesgo de pobreza". 

A continuación me situé en la columna de Comunidades y Ciudades Autónomas y escogí la opción de editar celdas, vaciar hacia abajo. Cuando hice esto, todas las Comunidades Autónomas que aparecían en cada uno de los años (2008, 2009, 2010...) excepto una, desaparecieron y dejaron el resto de celdas en blanco. 

El siguiente paso consiste en realizar el sumatorio para obtener posteriormente la media. El OpenRefine, como ya he mencionado, no reconoce las comas, pero ya había transformado las cifras en números (ver en gráfico anterior). Para ello, reordené las columnas dejando en primera posición la de Comunidades y a su lado la columna sobre la que se realizaría el Sumatorio. Me sitúe sobre la columna del Total y agregué una columna basada en la anterior. Cuando la hice tuve que introducir un título para la misma y la siguiente fórmula: row.record.cells["Total"].value.sum(). De esta forma, obtuve el sumatorio pero lo que a mí me interesaba era la media de esos trece años. Para conseguirla tuve que editar cada una de las celdas dividiendo desde la calculadora las cifras.

Así es como quedaba la tabla limpia. 

![Tabla limpia](/imagenes/Capturadepantalla3.png)

Luego la inserté en el DataWrapper y elegí el gráfico de flechas. En el tercer paso, de Visualizar, customicé el color y elegí el orden. También puse una pequeña leyenda antes de descargarla en el último paso. 


### Tasa de riesgo de pobreza en Comunidad Foral de Navarra

![Riesgo de pobreza en Navarra](/imagenes/tasa-de-riesgo-de-pobreza-en-comunidad-foral-de-navarra.png)

### Tasa de riesgo de pobreza en Ceuta 

![Riesgo de pobreza en Ceuta](/imagenes/tasa-de-riesgo-de-pobreza-en-ceuta.png)
