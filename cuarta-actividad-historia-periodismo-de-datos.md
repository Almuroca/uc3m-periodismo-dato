# Cuarta actividad: tu historia de periodismo de datos

## Datos seleccionados

He escogido un CSV del INE sobre la pobreza y variados de la misma en las Comunidades Autónomas de España durante los últimos trece años. De esta forma, aborda cuestiones como el riesgo de exclusión social o de pobreza, la tasa de carencia material severa y la de hogares con baja intensidad en el trabajo. 

Me parece un tema cuanto menos relevante e interesante para conocer las diferencias económicas que existen en España. Por todo ello, los gráficos realizados intentan mostrar de una manera visual la variedad económica que se produce en el país. 

## Gráficos realizados

### Tasa de riesgo de pobreza o exclusión social. 

![Tasa de riesgo de pobreza o exclusión social](/imagenes/tasa-de-riesgo-de-pobreza-o-exclusion-social-.png)

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

![Faceta de texto](/imagenes/Captura de pantalla1.png)

A continuación, mediante la opción de transformas celdas, modifiqué los datos de la segunda columna, "Total", en números. El OpenRefine no reconoce las comas, así que tuve que sustituirlas por puntos. Para ello, utilicé la transformación personalizada e introduje la expresión "value.replace(",","."). Una vez realizado este paso, pude transformarlo en números mediante la opción transformaciones comunes. 

![Transformar en número](/imagenes/Captura de pantalla2.png)

Cuando tenía todos los datos que necesitaba los exporté en DataWrapper.En esta herramienta de visualización, escogí la opción de Gráfico de Dispersión y a través de la customización personalizada le proporcioné los colores que quise a la gráfica. 


