



## La seguridad vial en la Ciudad Autónoma de Buenos Aires: un desafío que requiere datos y análisis

La seguridad vial es un tema de preocupación constante en la Ciudad Autónoma de Buenos Aires. Los siniestros viales son eventos frecuentes que afectan la vida de sus residentes y visitantes. Cada año, miles de personas son víctimas de accidentes de tráfico, algunos de los cuales resultan en lesiones graves o incluso en tragedias fatales. La magnitud de este problema no solo impacta en la salud y seguridad de las personas, sino que también afecta la infraestructura vial y los servicios de emergencia.

En este contexto, surge nuestro proyecto individual #2, una iniciativa que busca utilizar el poder de los datos y el análisis para abordar el desafío de los siniestros viales en dicha ciudad.

Nos hemos propuesto la tarea de analizar a fondo los incidentes de tráfico ocurridos en los últimos años. Nuestro objetivo es generar información valiosa que permita a las autoridades locales tomar medidas efectivas para reducir la cantidad de víctimas fatales en estos incidentes.

Este proyecto no solo es una oportunidad para aplicar nuestras habilidades de análisis de datos, sino también un compromiso con la seguridad y el bienestar de la comunidad. A través de este informe, te invitamos a explorar nuestro enfoque y descubrir cómo los datos pueden desempeñar un papel fundamental en la construcción de una ciudad más segura en las carreteras de Buenos Aires.

*NOTA: Es importante aclarar que los resultados y conclusiones aquí presentadas, deben usarse solo con fines académicos, y de ningún modo en la toma de decisiones finales. 
---

## Fases del Proyecto

El proyecto se desarrolló siguiendo estos aspectos clave:

- Análisis Exploratorio de Datos: [EDA link](https://github.com/alexxcode/Proyecto-2-DA/blob/main/EDA.ipynb)

- Desarrollo KPIs: [Desarrollo de los KPIs link](https://github.com/alexxcode/Proyecto-2-DA/blob/main/KPI.ipynb)

- Dashboard en Power BI: [Dashboard link](https://github.com/alexxcode/Proyecto-2-DA/blob/main/Dashboard.pbix)

</br>

## ETL

Si bien el proyecto no requería un ETL o transformación de datos, fue necesario realzar algunas modificaciones con el fin de alcanzar el objetivo de forma mas eficiente, por tanto, previamente al análisis se realizaron las siguientes acciones para garantizar la calidad y coherencia de los datos:
**1. Eliminación de Duplicados** 
**2. Filtrado de Fechas Inválidas:** Se ha realizado un filtrado riguroso en la columna 'release_date' para identificar y cuantificar los valores atípicos que no cumplen con el formato aaaa-mm-dd. 
**3. Unión de las tablas:** Como parte de la transformación se ha realizado la unión de las tablas por medio de un inner 
**4. Gestión de Valores Nulos:** Dado que los valores nulos podrían afectar negativamente el funcionamiento de la API, se han eliminado de manera consciente. 
**5. Identificación de Outliers** 
**6. Eliminación de Registros Incoherentes** 
**7. Creación de nuevas columnas:** se crearon dos columnas nuevas llamadas SEMESTRE y CATEGORIA_EDAD  para realizar los KPIs y el Deshboard sin modificación posterior. 

</br>


## EDA

Utilizando los datos resultantes del proceso ETL, se llevó a cabo un análisis exploratorio de datos (EDA) que reveló resultados sorprendentes y Se descubrió patrones que no eran evidentes a simple vista.
A continuación, haremos un análisis exhaustivo por categoría:

**1. Relación entre AÑO y el Número de Víctimas :**

![Relación entre EDAD y el Número de Víctimas](https://github.com/alexxcode/Proyecto-2-DA/blob/main/images/edad_victimas.png)

**Análisis de la distribución de muertes por siniestros viales por categoría de edad**

- Distribución por categoría de edad

El DataFrame presenta tres categorías principales de edad: niños, adultos jóvenes y adultos mayores. La categoría de niños tiene 80 muertes por siniestros viales, la categoría de adultos jóvenes tiene 262 y la categoría de adultos mayores tiene 322.

- Diferencias en el número de muertes por categoría de edad

Se observan diferencias significativas en el número de muertes por siniestros viales entre las categorías de edad. La categoría de adultos mayores tiene el mayor número de muertes, seguida por la categoría de adultos jóvenes, mientras que la categoría de niños tiene el menor número de muertes.

- Interpretación de los resultados

Estas diferencias en el número de muertes por categoría de edad podrían estar relacionadas con la vulnerabilidad de cada grupo de edad en siniestros viales, así como con la exposición a diferentes riesgos en la carretera.

- Análisis demográfico

Sería útil considerar las características demográficas de cada grupo de edad, como la población total en cada categoría, para comprender mejor si estas diferencias son proporcionales a la población en riesgo.

- Prevención y seguridad vial

Estos datos pueden ser útiles para evaluar políticas y programas de seguridad vial dirigidos a grupos específicos de edad. Por ejemplo, si los adultos mayores tienen un alto número de muertes en siniestros viales, podría ser importante implementar medidas adicionales de seguridad para este grupo en particular, como campañas de concienciación y mejoras en las infraestructuras viales.

**2. Diagrama de Barras por Tipo de Calle:**

![Diagrama de Barras por Tipo de Calle]()
