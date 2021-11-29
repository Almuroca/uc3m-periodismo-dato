# Cuarta actividad: tu historia de periodismo de datos

## Datos seleccionados

He escogido un archivo CSV del [Instituto Nacional de Estadística (INE)](https://www.ine.es/jaxiT3/Tabla.htm?t=10005&L=0) sobre la pobreza y sus componentes en las comunidades autónomas de España durante los últimos trece años. El documento, aborda cuestiones como el riesgo de exclusión social o de pobreza, la tasa de carencia material severa y la de hogares con baja intensidad en el trabajo.
 
Me parece un tema cuanto menos relevante e interesante para conocer las diferencias económicas que existen en España. Por todo ello, los gráficos realizados intentan mostrar de una manera visual la variedad económica que se produce en el país. Para realizar estos gráficos he utilizado OpenRefine y Datawrapper. 

## Gráficos realizados

### Tasa de riesgo de pobreza o exclusión social. 

![Tasa de riesgo de pobreza o exclusión social](/imagenes/tasa-de-riesgo-de-pobreza-o-exclusi-n-social-.png)
 
#### Análisis 

He realizado este gráfico de dispersión porque me parece la mejor manera de mostrar los cuatro componentes que recoge el CSV. Este gráfico se utiliza para relacionar dos variables, que en este caso serían la variable "X" que muestra la evolución temporal desde 2008 hasta 2020 y la variable "Y" que refleja la tasa de pobreza.

Los elementos que aparecen en el gráfico aparecen representados con colores diferentes:

- Carencia material severa: en color gris ya que alude a bienes materiales.
- Riesgo de pobreza: aparece en color rojo ya que se relaciona con el peligro o advertencia como vemos en señales de tráfico por ejemplo.
- Riesgo de exclusión social: aparece en color negro puesto que se relaciona con algo negativo, algo oscuro o trágico.
- Vivir en hogares con baja intensidad en el trabajo: he puesto un color azul porque este color recuerda al  cumplimiento de la ley que recoge que todos tenemos derecho a una vivienda justa.
 
Por todo ello, el gráfico puede resultar útil para deducir que la tasa más baja es la de "carencia de material severa" y la más elevada es la tasa de "riesgo de pobreza o exclusión social". Al mismo tiempo se aprecia que todas ellas contaron un pico ascendente en el año 2014.

La tipografía que utilizo es muy comprensible, igual que el título escogido. Al mismo tiempo, he optado por poner un rango muy cercano a la tasa que aparece en el CSV y los números van de cinco en cinco por lo que se aprecia mejor la realidad expuesta.

#### ¿Cómo se ha realizado esta gráfica?

**OpenRefine:**

Para empezar, busqué el tema que quería abordar en el INE y luego descargué el archivo como un .csv mediante el comando wget en la terminal. A continuación, lo exporté en el OpenRefine y por medio de la faceta de texto en la primera columna "Comunidades y Ciudades Autónomas" seleccioné la opción de "Total Nacional" dejando a parte el resto de Comunidades Autónomas, porque lo importante es conocer la evolución anual de estos cuatro componentes a nivel nacional.

![Faceta de texto](/imagenes/Capturadepantalla1.png)

A continuación, mediante la opción de transformas celdas, modifiqué los datos de la segunda columna, "Total", en números. El OpenRefine no reconoce las comas, así que tuve que sustituirlas por puntos. Para ello, utilicé la transformación personalizada e introduje la expresión "value.replace(",","."). Una vez realizado este paso, pude transformarlo en números mediante la opción transformaciones comunes.

![Transformar en número](/imagenes/Capturadepantalla2.png)

**Datawrapper:**

Cuando tenía todos los datos que necesitaba los exporté en Datawrapper. En esta herramienta de visualización, escogí la opción de Gráfico de Dispersión y en ese mismo paso de la "Visualizar" hay un apartado llamado "Mejorar" donde elegí la customización personalizada que me permitió proporcionar los colores que quise a la gráfica. En visualizar también recurrí a la opción de "Anotar" donde incluí la leyenda del gráfico. Por último, en el subartado "Diseño" escogí la opción de "Español" para que esta leyenda apareciera en este idioma.

### Tasa de riesgo de pobreza en España
 
#### Análisis

Las cuatro gráficas que muestro a continuación se centran en uno de los apartados mencionados anteriormente: el riesgo de pobreza.

![Tasa de riesgo de pobreza en España](/imagenes/tasa-de-riesgo-de-pobreza-en-españa.png)

La siguente gráfica es de flechas y resulta muy útil para ver que la que menor tasa de pobreza registra es la Comunidad Foral de Navarra, mientras que la que presenta una mayor tasa es Ceuta. Se convierte en un gráfico muy visual y cualquier periódico podría incluirlo en sus noticias pues de  un golpe de vista se refleja la diferencia que existe en España.

Aparecen en orden de menor a mayor, ya que proporciona un mayor entendimiento. Resulta más visual y práctico mostrar una grada descendente y poner en primera posición la tasa más pequeña. No obstante, depende de dónde quiera poner el foco la noticia, si quiere centrarse en la Comunidad con menor tasa de pobreza lo ideal es colocarla el primera posición. Si por el contrario prefiere hablar de la tasa más elevada, sería mejor poner Ceuta en la parte superior, es decir, invertir el orden.

El color utilizado es el rojo, de nuevo por su simbología de peligro o aspecto negativo. Cuando uno dice que no tiene dinero, suele decir "estoy en números rojos". De ahí la elección del color.

Al mismo tiempo he optado por poner el título en minúsculas porque resulta menos agresivo y he dejado la nomenclatura que utilizaba el INE para referirse a cada Comunidad Autónoma (Madrid, Comunidad de, en vez de Comunidad de Madrid). No lo he modificado, porque si alguien quiere ordenar los datos por orden alfabético es preferible identificar así las comunidades autónomas. La tipografía es la misma en todos los gráficos por la intención de seriedad que pretender mostrar.

#### ¿Cómo he realizado esta gráfica?

**OpenRefine:**

La gráfica presentada requiere un mayor nivel de limpieza que la anterior. Para realizarla he utilizado facetas de texto y transformaciones personalizadas.

En primer lugar, una vez exporté el CSV realicé una faceta de texto en la tercera columna "Tasa de riesgo de pobreza o exclusión social (y sus componentes) y seleccioné "En riesgo de pobreza".

A continuación, me situé en la columna de Comunidades y Ciudades Autónomas y escogí la opción de editar celdas, vaciar hacia abajo. Cuando hice esto, todas las Comunidades Autónomas que aparecían en cada uno de los años (2008, 2009, 2010...) excepto una, desaparecieron y dejaron el resto de celdas en blanco. Es decir, en esta columna solo aparecía una vez el nombre de la comunidad autónoma y al lado cada uno de los totales.

El siguiente paso consiste en realizar el sumatorio para obtener posteriormente la media. El OpenRefine, como ya he mencionado, no reconoce las comas, pero ya había transformado las cifras en números (ver en gráfico anterior). Para poder sumar todos los valores, reordené las columnas dejando en primera posición la de "Comunidades" y a su lado la columna sobre la que se realizaría el Sumatorio. Me sitúe sobre la columna del Total y agregué una columna basada en la anterior. Cuando la hice tuve que introducir un título para la misma donde puse Media y la siguiente fórmula: row.record.cells["Total"].value.sum(). De esta forma, obtuve el sumatorio pero lo que a mí me interesaba era la media de esos trece años. Para conseguirla tuve que editar cada una de las celdas dividiendo desde la calculadora las cifras. Por último, desplacé la columna donde aparece la media al lado de las Comunidades Autónomas para que en el Datawrapper no me aparezca ningún error. (Hasta ese momento tenía la columna de comunidades, la del total transformada en números y la de la media).

Así es como quedaba la tabla limpia.

![Tabla limpia](/imagenes/Capturadepantalla3.png)

**Datawrapper:**

Inserté la tabla limpia en el Datawrapper y elegí el gráfico de flechas en la tercera fase de "Visualizar". En este mismo paso, customicé el color y elegí el orden. También puse una pequeña leyenda antes de descargarla en el paso de visualizar. Por último, completé el último paso de publicar e integrar y la descargué en mi ordenador y desde la terminal la incluí en mi carpeta imágenes de mi Github.

### Tasa de riesgo de pobreza en Comunidad Foral de Navarra

![Riesgo de pobreza en Navarra](/imagenes/tasa-de-riesgo-de-pobreza-en-comunidad-foral-de-navarra.png)
 
#### Análisis
 
Como se aprecia en el gráfico anterior Navarra es la Comunidad que menor tasa de pobreza presenta. Es una gráfica muy sencilla de barras que sirve para mostrar la evolución de la tasa durante los últimos trece años. He dejado los porcentajes porque ayudan al lector a ver de foma directa las tasas teniendo en cuenta los decimales.
 
En esta gráfica he escogido el color rojo porque la bandera de la Comunidad Foral de Navarra es roja. Además he optado por este título porque es corto, preciso y explícito. He añadido una breve descripción en la leyenda por si alguien no lo entendiera bien.

#### ¿Cómo he realizado esta gráfica?

**OpenRefine:**

Como ya he mencionado, es una gráfica muy sencilla, lo único que he tenido que hacer es jugar con las facetas de texto y elegir las que me interesaban. En este caso solo necesitaba dos datos: Comunidad Foral de Navarra conseguida por una faceta de texto en la columna "Comunidades" y la tasa de riesgo de pobreza que se encontraba en la columna "Tasa de riesgo de pobreza o exclusión social (y sus componentes)".

**Datawrapper:**

Cuando tenía los datos seleccionados los exporté mediante la opción exportar valor delimitado por comas. A continuación, introduje los datos en el Datawrapper, verifiqué y describí quitando las columnas que no me interesaban. En la tercera fase de "Visualizar" escogí la opción de Gráfico de columnas y con la posibilidad de "Mejorar" escogí el color que quise y dejé el porcentaje fijo. En esta misma fase introduje el título y la leyenda. Por último, en el cuarto paso "Publicar e integrar" descargué mi infografía con formato PNG.

**Github y terminal:**

Una vez, tuve mi gráfica, igual que con el resto, las subí a mi carpeta "imagenes" que tengo en mi repositorio en Github y la añadí en mi editor de texto nano.

### Tasa de riesgo de pobreza en Ceuta 

![Riesgo de pobreza en Ceuta](/imagenes/tasa-de-riesgo-de-pobreza-en-ceuta.png)

#### Análisis

Esta gráfica es igual que la anterior así que no necesita mucha explicación, la única diferencia son los datos escogidos. En este caso seleccioné los referentes a Ceuta, la comunidad con mayor tasa de riesgo de pobreza. En este gráfico puse un color negro por su bandera y opté por este título porque era preciso y explícito.

#### ¿Cómo he realizado esta gráfica?

Limpié los datos mediante facetas de texto, en las mismas columnas que he citado en la anterior gráfica. Sin embargo, en la columna Comunidades seleccioné Ceuta. Al mismo tiempo, en **Datawrapper** escogí otro color en la fase de visualización.

El resto de pasos son iguales que en la gráfica de la Comunidad Foral de Navarra.

### Comparativa tasa de riesgo de pobreza en Navarra y Ceuta

![Comparación](/imagenes/comparacion.png)

#### Análisis

He considerado oportuno realizar esta gráfica para mostrar de forma visual la diferencia que existe entre la comunidad con mayor riesgo de pobreza y la que menos tiene. He optado por una gráfica de área porque muestra el total acumulado de cada una de ellas y lo lejos que están una de la otra.

Los colores que he utilizado son los mismos que había utilizado en las gráficas individuales de cada una de ellas para proporcionar unidad. El título intenta ser explícito, pero es cierto que no se entiende si no se visualizan las gráficas anteriores. De todas formas, la otra opción de titular sería muy larga y no podría utilizarse como título. Sería algo así como "Comparación entre la comunidad más rica y la más pobre". La tipografía empleada es la misma en todas las gráficas ya es comprensible y seria, es decir, apropiada al tema tratado. Por otro lado, el rango abarca del 5 al 55 ya que sino no sería del todo real, además como son cantidades pequeñas puedo permitirme poner un rango lo más cercano a la realidad posible.

#### ¿Cómo he realizado este gráfico?

**OpenRefine:**

Mediante facetas de texto escogí los datos que me interesaban: Comunidad Foral de Navarra y Ceuta de la columna de "Comunidades" y riesgo de pobreza de la columna "Riesgo de pobreza y exclusión (y sus componentes).

A continuación, reordené las columnas dejando en primera posición el período que abarca del 2008 al 2020. Luego añadí columna basada en el total que titulé "Comunidad Foral de Navarra" y mendiante la opción de value.replace sustituí el nombre de la comunidad por espacios en blanco. Una vez tuve una columna en blanco titulada Comunidad Foral de Navarra puse la tasa a mano en las trece celdas. Lo mismo hice con Ceuta, añadí una columna basada en la anterior que titulé Ceuta y la dejé en blanco para introducir a mano el total.

![Captura nombre](/imagenes/Capturadepantallas4.png) ![Captura añadir columna](/imagenes/Capturadepantallas5.png)

Por último, eliminé todas las filas que no aportaban la información que quería puesto que repetían información y reorganicé los datos: Período, Comunidad Foral de Navarra y Ceuta.

![Limpieza](/imagenes/Capturadepantallas6.png)

**Datawrapper:**

Inserté el CSV que había descargado y escogí la opción gráfico de área. En la fase de visualizar, en el subapartado "Mejorar" escogí los colores, los valores que quería mostrar del eje vertical y las cuadrículas que quería ocultar del ejer horizontal. Luego anoté la información que me interesaba y la descargué como PNG.
 
**Github:**

Incluí la explicación en nano, añadiendo las imágenes que había subido desde la terminal a mi carpeta "imagenes" de mi repositorio uc3m-periodismo-de-dato y publiqué todo mediante el git add, git commit -m, git push origin main.

## ¿Por qué todos estos gráficos?

He realizado todos y cada uno de estos gráficos porque tenía la idea de realizar una noticia a partir de ellos. Por eso, si quería hacer un artículo sobre la tasa de pobreza y exclusión en España me parecía importante presentar cuál es el componente  más característico, en este caso la tasa de riesgo de pobreza o exclusión social (como se ve en el gráfico 1). Por otro lado, también me consideraba interesante estudiar cada uno de los componentes. Yo por ejemplo, me centré en el apartado de la pobreza y comparé todas las comunidades y luego la que presentaba una tasa más alta y la que tenía una más baja. Lo mismo se podía hacer con el resto de puntos (vivienda, carencia material, riesgo de exclusión).
