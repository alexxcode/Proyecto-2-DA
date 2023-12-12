



## La seguridad vial en la Ciudad Autónoma de Buenos Aires: un desafío que requiere datos y análisis.

La seguridad vial es un tema de preocupación constante en la Ciudad Autónoma de Buenos Aires. Los siniestros viales son eventos frecuentes que afectan la vida de sus residentes y visitantes. Cada año, miles de personas son víctimas de accidentes de tráfico, algunos de los cuales resultan en lesiones graves o incluso en tragedias fatales. La magnitud de este problema no solo impacta en la salud y seguridad de las personas, sino que también afecta la infraestructura vial y los servicios de emergencia.

En este contexto, surge nuestro proyecto individual #2, una iniciativa que busca utilizar el poder de los datos y el análisis para abordar el desafío de los siniestros viales en dicha ciudad.

Nos hemos propuesto la tarea de analizar a fondo los incidentes de tráfico ocurridos en los últimos años. Nuestro objetivo es generar información valiosa que permita a las autoridades locales tomar medidas efectivas para reducir la cantidad de víctimas fatales en estos incidentes.

Este proyecto no solo es una oportunidad para aplicar nuestras habilidades de análisis de datos, sino también un compromiso con la seguridad y el bienestar de la comunidad. A través de este informe, te invitamos a explorar nuestro enfoque y descubrir cómo los datos pueden desempeñar un papel fundamental en la construcción de una ciudad más segura en las carreteras de Buenos Aires.

> [!NOTE]
>  Es importante aclarar que los resultados y conclusiones aquí presentadas deben usarse solo con fines académicos y orientativos, de ningún modo en la toma de decisiones finales.

## Fases del Proyecto

El proyecto se desarrolló siguiendo estos aspectos clave:

- Análisis Exploratorio de Datos: [EDA link](https://github.com/alexxcode/Proyecto-2-DA/blob/main/EDA.ipynb)

- Desarrollo KPIs: [Desarrollo de los KPIs link](https://github.com/alexxcode/Proyecto-2-DA/blob/main/KPI.ipynb)

- Dashboard en Power BI: [Dashboard link](https://github.com/alexxcode/Proyecto-2-DA/blob/main/Dashboard.pbix)

</br>

## ETL

Si bien el proyecto no requería un ETL o transformación de datos, fue necesario realizar algunas modificaciones con el fin de alcanzar el objetivo del proyecto forma más eficiente, por tanto, previamente al análisis se realizaron las siguientes acciones para garantizar la calidad y coherencia de los datos:

- **1. Eliminación de Duplicados.** 
- **2. Filtrado de Fechas Inválidas:** Se ha realizado un filtrado riguroso en la columna 'release_date' para identificar y cuantificar los valores atípicos que no cumplen con el formato aaaa-mm-dd. 
- **3. Unión de las tablas:** Como parte de la transformación se ha realizado la unión de las tablas por medio de un inner.
- **4. Gestión de Valores Nulos:** Dado que los valores nulos podrían afectar negativamente el funcionamiento de la API, se han eliminado de manera consciente. 
- **5. Identificación de Outliers.** 
- **6. Eliminación de Registros Incoherentes.** 
- **7. Creación de nuevas columnas:** se crearon dos columnas nuevas llamadas SEMESTRE y CATEGORIA_EDAD  para realizar los KPIs y el Deshboard sin modificación posterior. 

</br>


## EDA

Utilizando los datos resultantes del proceso ETL, se llevó a cabo un análisis exploratorio de datos (EDA) que reveló resultados sorprendentes y patrones que no eran evidentes a simple vista.
A continuación, haremos un análisis exhaustivo por categoría:

**1. Relación entre AÑO y el Número de Víctimas :**

![Relación entre AÑO y el Número de Víctimas](https://github.com/alexxcode/Proyecto-2-DA/blob/main/images/year_victima.png)


**Análisis de la gráfica #1:**

- Tendencia temporal

La gráfica presenta datos desde 2016 hasta 2021, lo que permite analizar la evolución del número de víctimas a lo largo de este periodo. Se observa que el número de víctimas disminuyó desde 2018 hasta 2021, tras un pico en 2018.

- Pico en 2018

El año 2018 destaca como el año con el mayor número de víctimas, con 149. Es necesario investigar las causas de este aumento significativo en comparación con los años anteriores y posteriores.

- Disminución en 2019 y 2020

En 2019, el número de víctimas disminuyó a 104, y en 2020 disminuyó aún más a 81. Esta tendencia a la baja podría deberse a una serie de factores, como políticas gubernamentales o medidas de seguridad.

- Aumento en 2021

En 2021, el número de víctimas aumentó nuevamente a 97. Es necesario investigar las causas de este aumento, que podría deberse a factores similares a los que provocaron el pico en 2018.

- Posibles factores influyentes

Para un análisis más completo, sería necesario considerar posibles factores que podrían haber contribuido a las variaciones en el número de víctimas a lo largo de estos años. Algunos factores que podrían influir incluyen:

Políticas gubernamentales.
Cambios en la economía.
Medidas de seguridad.
Otros factores sociales o económicos.

**2. Relación entre el género de las Víctimas y el Número de Víctimas :**

![Relación entre el género de las Víctimas y el Número de Víctimas](https://github.com/alexxcode/Proyecto-2-DA/blob/main/images/genero_victima.png)

**Análisis de la distribución de víctimas por género:**

- Distribución por género

El DataFrame presenta dos categorías principales de género: femenino y masculino. La categoría femenina tiene 166 víctimas, mientras que la categoría masculina tiene 545 víctimas.

- Diferencia significativa en el número de víctimas

Es evidente que hay una diferencia significativa en el número de víctimas entre los géneros. El género masculino tiene un número mucho mayor de víctimas que el género femenino. Esta diferencia es de aproximadamente 3.29:1

- Proporción de género

La proporción de género es una medida que indica la relación entre dos categorías. En este caso, la proporción de género masculino a femenino es de 3.29:1. Esto significa que por cada mujer víctima, hay 3.29 hombres víctimas.

- Implicaciones y análisis adicional

Esta diferencia en el número de víctimas entre géneros podría ser el resultado de múltiples factores. Algunos de estos factores podrían incluir:  La distribución de roles de género en la sociedad, la exposición a diferentes riesgos o la subnotificación de casos en función del género.


**3. Relación entre la edad y el número de víctimas:**

![Relación entre EDAD y el Número de Víctimas](https://github.com/alexxcode/Proyecto-2-DA/blob/main/images/edad_victimas.png)

**Análisis de la distribución de muertes por siniestros viales por categoría de edad:**

- Distribución por categoría de edad

El DataFrame presenta tres categorías principales de edad: niños, adultos jóvenes y adultos mayores. La categoría de niños tiene 80 muertes por siniestros viales, la categoría de adultos jóvenes tiene 424 y la categoría de adultos mayores tiene 161.

- Diferencias en el número de muertes por categoría de edad

Se observan diferencias significativas en el número de muertes por siniestros viales entre las categorías de edad. La categoría de adultos jóvenes tiene el mayor número de muertes, seguida por la categoría de adultos mayores, mientras que la categoría de niños tiene el menor número de muertes con 79.

- Interpretación de los resultados

Estas diferencias en el número de muertes por categoría de edad podrían estar relacionadas con el tipo de actividad que realiza de cada grupo de forma frecuente, así como con la exposición a diferentes riesgos en la carretera.

- Análisis demográfico

Sería útil considerar las características demográficas de cada grupo de edad, como la población total en cada categoría, para comprender mejor si estas diferencias son proporcionales a la población en riesgo.

- Prevención y seguridad vial

Estos datos pueden ser útiles para evaluar políticas y programas de seguridad vial dirigidos a grupos específicos de edad. Por ejemplo, si los adultos mayores tienen un alto número de muertes en siniestros viales, podría ser importante implementar medidas adicionales de seguridad para este grupo en particular, como campañas de concienciación y mejoras en las infraestructuras viales.


**4. Diagrama de Barras por el tipo de calle:**

![Diagrama de Barras por Tipo de Calle](https://github.com/alexxcode/Proyecto-2-DA/blob/main/images/diagrama_calle.png)


**Análisis de la distribución de víctimas por tipo de calle:**

- Distribución por tipo de calle

El DataFrame presenta cuatro categorías principales de tipo de calle: autopista, avenida, calle y General Paz. La categoría de avenida tiene la mayor cantidad de víctimas por siniestros viales, con 442. Le sigue la categoría de calle con 137, la categoría de General Paz con 69 y la categoría de autopista con 67.

- Diferencias en el número de víctimas por tipo de calle

Se observan diferencias significativas en el número de víctimas por siniestros viales entre los tipos de calle. La categoría de avenida tiene el mayor número de víctimas, seguida por la categoría de autopista. La categoría de calle tiene un número significativamente menor de víctimas, y la categoría de General Paz tiene el menor número de víctimas.

- Proporciones de víctimas por tipo de calle

Calcular la proporción de víctimas en cada tipo de calle puede ayudar a comprender mejor la relación entre ellos. Por ejemplo, la proporción de víctimas en avenidas es de 68.3%, mientras que la proporción de víctimas en autopistas es de 6.9%. Esto sugiere que las avenidas tienen un mayor riesgo de siniestros viales que las autopistas.

- Interpretación de los resultados

Estas diferencias en el número de víctimas por tipo de calle podrían estar relacionadas con una serie de factores, como la velocidad máxima permitida en cada tipo de carretera, el volumen de tráfico, la presencia de semáforos y señalización, y otros factores de seguridad vial.

- Medidas de seguridad vial

Los datos pueden ser útiles para evaluar la efectividad de las medidas de seguridad vial en diferentes tipos de carreteras. Por ejemplo, si las avenidas tienen una alta cantidad de víctimas, podría ser necesario revisar las medidas de seguridad y la infraestructura en ese tipo de carretera.


**5. Distribución de Víctimas por Rol:**

![Distribución de Víctimas por Rol](https://github.com/alexxcode/Proyecto-2-DA/blob/main/images/rol_victima.png)


**Análisis de la distribución de víctimas por rol y tipo de vehículo:**

- Distribución de roles y tipos de vehículos

El DataFrame presenta datos sobre el rol de las víctimas en siniestros viales, el tipo de vehículo involucrado y la cantidad de casos para cada combinación.

- Las combinaciones de roles y tipos de vehículos incluyen:

Conductor de auto
Conductor de moto
Ciclista
Pasajero de auto
Pasajero de moto
Peaton

- Número de casos

El DataFrame también presenta el número de casos para cada combinación. Por ejemplo, la combinación "Ciclista" - "Bicicleta" tiene 29 casos. Esto significa que hubo 29 siniestros viales en los que la víctima era un ciclista que conducía una bicicleta.

- Interpretación de los resultados

Los resultados del análisis sugieren que los peatones y los ciclistas son los usuarios más vulnerables de las carreteras. Los peatones representan el 34% de las víctimas, mientras que los ciclistas representan el 12%.

Los conductores de autos y motos también representan un número significativo de víctimas. Los conductores de autos representan el 29% de las víctimas, mientras que los conductores de motos representan el 11%.

- Implicaciones y análisis adicional

Estos resultados sugieren que se deben tomar medidas para mejorar la seguridad de los peatones y los ciclistas. Estas medidas podrían incluir:

Mejorar la infraestructura vial para proteger a los peatones y ciclistas.

Implementar campañas de educación vial para concienciar a los conductores sobre la importancia de compartir la carretera con los peatones y ciclistas.

También se podrían tomar medidas para mejorar la seguridad de los conductores de autos y motos. Estas medidas podrían incluir:

Reducir los límites de velocidad.
Mejorar la seguridad de los vehículos.
Implementar campañas de educación vial para concienciar a los conductores sobre la importancia de conducir de forma segura.



Este análisis proporciona información valiosa sobre la relación entre el rol de las víctimas y el tipo de vehículo involucrado en siniestros viales. Esta información puede ser utilizada para abordar problemas de seguridad vial específicos y tomar medidas adecuadas para reducir los riesgos en las carreteras.


**6. Cantidad de Siniestros por Mes:**

![Cantidad de Siniestros por Mes](https://github.com/alexxcode/Proyecto-2-DA/blob/main/images/mes_victima.png)


**Análisis de la distribución de víctimas de siniestros viales por mes:**

- Distribución de víctimas por mes

El DataFrame presenta datos sobre el número de víctimas de siniestros viales para cada mes del año.

- Variación en el número de víctimas por mes

Se observa variación en el número de víctimas de siniestros viales en diferentes meses. El mes con el mayor número de víctimas es diciembre, con 80, mientras que los meses con la menor cantidad de víctimas son julio y septiembre, ambos con 51.

- Diferencias en la seguridad vial

Estas diferencias en el número de víctimas podrían estar relacionadas con factores como:

Condiciones climáticas: Los meses con condiciones climáticas adversas, como lluvia o nieve, podrían tener un mayor riesgo de siniestros viales.
Actividades recreativas: Los meses con más actividades recreativas, como fiestas de fin de año o navidad, podrían tener un mayor riesgo de siniestros viales.

- Políticas de seguridad vial

Estos datos pueden ser útiles para evaluar la efectividad de las políticas de seguridad vial en diferentes meses y para identificar aquellos que podrían requerir medidas de prevención adicionales.



Este análisis proporciona información valiosa sobre la distribución de víctimas de siniestros viales por mes. Esta información puede ser utilizada para mejorar la seguridad vial en diferentes meses, identificando factores de riesgo e implementando medidas de prevención.


Este análisis proporciona información valiosa sobre la distribución de víctimas de siniestros viales por mes. Esta información puede ser utilizada para mejorar la seguridad vial en diferentes meses, identificando factores de riesgo e implementando medidas de prevención.



**7. Número de Víctimas por Comuna :**

![Número de Víctimas por Comuna](https://github.com/alexxcode/Proyecto-2-DA/blob/main/images/comuna_victima.png)


**Análisis de la gráfica de víctimas por comuna**

- Distribución de víctimas

La tabla muestra los datos de 15 comunas diferentes, numeradas del 1 al 15. La cantidad de víctimas varía significativamente entre las comunas, desde 22 hasta 93.

- Comuna con el mayor número de víctimas

La comuna con el mayor número de víctimas es la Comuna 1, con 93 víctimas. Este dato es llamativo y podría indicar un área de interés para investigar más a fondo las razones detrás de esta cifra alta.

- Comuna con el menor número de víctimas

Las Comunas 5 y 6 tienen el menor número de víctimas, con 22. Este dato también es significativo y podría ser un punto de partida para investigar las condiciones que llevan a esta cifra baja.

- Distribución general

La distribución de víctimas en estas comunas parece ser bastante heterogénea, ya que algunas comunas tienen un número significativamente mayor de víctimas que otras.

- Análisis estadístico

Sería útil realizar un análisis estadístico más detallado para comprender mejor la variabilidad en el número de víctimas entre las comunas. Esto podría incluir cálculos como la media, la mediana, la desviación estándar y otros estadísticos descriptivos.

- Factores influyentes

Para un análisis más completo, sería importante considerar factores que podrían influir en el número de víctimas en cada comuna. Estos factores podrían incluir:

La densidad de población.
La presencia de servicios de seguridad.
Medidas de prevención del delito.
Otros factores sociales, económicos o culturales.

</br>

## KPIs

**KPI 1: Reducción del 10% en la tasa de homicidios en siniestros viales en CABA en comparación con el semestre anterior**

![KPI 1](https://github.com/alexxcode/Proyecto-2-DA/blob/main/images/kpi1.png)

Este KPI se enfoca en medir la evolución de la tasa de homicidios en siniestros viales en la Ciudad Autónoma de Buenos Aires (CABA) en un período de varios años, comparando los dos últimos semestres.  Análisis más detallado:

- **Tendencia general:** La tendencia en este KPI varía año tras año. En algunos años, se logra una disminución significativa, mientras que en otros se observa un aumento en la tasa de homicidios en siniestros viales.

- **Año 2020:** Se destaca un aumento significativo en la tasa de homicidios en el primer semestre (61.29%), pero una mejora en el segundo semestre (10%), lo que puede ser atribuible a factores específicos, como el impacto de la pandemia o medidas de seguridad vial.

- **Año 2021:** Los datos parecen estar incompletos, ya que falta información para el segundo semestre. Esto puede dificultar una evaluación precisa del rendimiento en ese año.

- **Comparación entre semestres:** En algunos casos, se logra la reducción deseada del 10% entre semestres, mientras que en otros no se alcanza.

- **Análisis de causas:** Sería útil profundizar en las razones detrás de las variaciones en la tasa de homicidios en siniestros viales, como cambios en las políticas de seguridad vial, mejoras en la infraestructura vial, o la influencia de eventos externos como la pandemia.


**KPI 2: Reducción del 7% en la cantidad de accidentes mortales de motociclistas en CABA en comparación con el año anterior**

![KPI 2](https://github.com/alexxcode/Proyecto-2-DA/blob/main/images/kpi2.png)


Este KPI se centra en evaluar la evolución de la cantidad de accidentes mortales de motociclistas en la Ciudad Autónoma de Buenos Aires (CABA) en un período de varios años, comparando los dos últimos años. Análisis más detallado:

- **Tendencia general:** En este KPI, también se observa una variación año tras año, con fluctuaciones tanto positivas como negativas.

- **Año 2020:** Destaca un aumento significativo del 64.29% en la cantidad de accidentes mortales de motociclistas, lo que podría requerir una atención inmediata para comprender las razones detrás de este aumento.

- **Año 2021:** Al igual que en el KPI 1, faltan datos para el año 2021 en este KPI, lo que dificulta una evaluación precisa.

- **Comparación anual:** La reducción del 7% en la cantidad de accidentes mortales de motociclistas es el objetivo, pero no siempre se logra. Por ejemplo, en el año 2019, se observa una disminución significativa del 44%.

- **Análisis de causas:** Para entender las fluctuaciones en este KPI, sería importante analizar factores como las medidas de seguridad específicas para motociclistas, el aumento en la cantidad de motociclistas en la ciudad y la aplicación de políticas de tráfico.


**KPI 3: Reducción del 15% en la cantidad de accidentes mortales de niños en CABA respecto al año anterior.**

![KPI 3](https://github.com/alexxcode/Proyecto-2-DA/blob/main/images/kpi3.png)

El KPI 3 se centra en evaluar la evolución de la cantidad de accidentes mortales de niños en la Ciudad Autónoma de Buenos Aires (CABA) en un período de varios años, comparando los dos últimos años.

- **Tendencia General:** En general, hubo una reducción en la cantidad de accidentes mortales de niños en CABA durante los años analizados.

- **Año 2017:** El año 2017 muestra una disminución significativa con 37 accidentes mortales menos que en el año anterior. Esto podría ser un punto de interés para investigar más a fondo.

- **Años 2018 y 2019:** En 2018, hubo un aumento de 25 accidentes mortales, seguido por una disminución aún mayor de 47 accidentes mortales en 2019. Es importante entender las razones detrás de estos cambios bruscos.

- **Año 2020:** Aunque hubo una disminución de 12 accidentes mortales en 2020, esta cifra sigue siendo negativa. Sería relevante investigar las circunstancias específicas de estos accidentes.

- **Análisis Cualitativo:** Además de los números, es importante analizar las causas subyacentes de estos accidentes. ¿Hubo cambios en las políticas de seguridad vial? ¿Se implementaron programas de concienciación? ¿Factores como el tráfico, la infraestructura o el comportamiento de los conductores influyeron en estas cifras?




*Todo este proceso fue desarrollado localmente en **Visual Studio Code (VSCODE)** utilizando **Jupyter Notebook** como nuestro entorno de trabajo principal. La combinación de herramientas tecnológicas que empleamos incluye **Python** como lenguaje de programación, junto con bibliotecas esenciales como **numpy y pandas** para la manipulación eficiente de datos. Además, utilizamos **matplotlib y seaborn** para la creación de visualizaciones gráficas impactantes, que nos permitieron revelar patrones y tendencias ocultas en los datos de manera efectiva.*
