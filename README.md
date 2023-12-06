



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



