<p align=center><img src=https://d31uz8lwfmyn8g.cloudfront.net/Assets/logo-henry-white-lg.png><p>

# <h1 align=center> **PROYECTO INDIVIDUAL Nº 2** </h1>

# <h1 align=center>**<span style="color:cadetblue">DATA ANALYSIS - Telecomunicaciones: INTERNET EN ARGENTINA</span>**</h1>

<p align="center">
  <img src="Imagenes/imagen_portada4.jpg"  height=300 />
</p>

<br>
<div style="text-align: center; color: blue; font-size: 1.2em; font-weight: bold;">
  <a href="https://www.linkedin.com/in/javier-dichiachio-34104857/" style="color: cadetblue; text-decoration: none;">
    Autor: Javier Dichiachio, Cohorte 16
  </a>
</div>

# <h1 align=center> **Introducción** </h1>

El desafío planteado para este proyecto consiste en asumir un rol de **Data Analyst** y brindar un **análisis completo** del **Sector Internet**, dentro del Sector Telecomunicaciones en **Argentina**, a una empresa prestadora de servicios de telecomunicaciones, cuya principal actividad es brindar acceso a Internet.


> El trabajo se compone, por un lado, por un **Análisis Exploratorio de Datos** en **Python** en el cual se busca conocer acerca de las **características y evolución del sector** en los últimos años; y se complementa con un **Dashboard interactivo** en **Power BI**, en el cual se **incluyen** ciertos **indicadores claves de rendimiento** del sector (**KPI**).
<br>

# <h1 align=center> **Desarrollo del Proyecto**</h1>
<br>

# EXPLORATORY DATA ANALYSIS (EDA)

El detalle de este proceso se detalla en el Jupyter Notebook [EDA.ipynb](/EDA.ipynb). En el mismo se trabaja con los siguientes archivos:

    - Internet_Penetracion.xlsx: incluye información sobre los accesos a Internet cada 100 hogares por Provincia y por Trimestre, desde el año 2014 al 2022.
    - Internet_BAF.xlsx: incluye información sobre los accesos a Internet por tipo de Banda por Provincia y por Trimestre, desde el año 2014 al 2022.
    - Accesos_por_tecnologia.xlsx.xlsx: incluye información sobre los accesos a Internet por tipo de tecnología utilizada en la conexión, por Provincia y por Trimestre, desde el año 2014 al 2022.
    - Internet_Accesos_Velocidad.xlsx: incluye información sobre los accesos a Internet de acuerdo a rangos de velocidad de descarga, por Provincia y por Trimestre, desde el año 2014 al 2022.
    - Historico_Velocidad.xlsx: incluye información sobre la velocidad media de bajada por Provincia y por Trimestre, desde el año 2014 al 2022.
    - mapa_conectividad.xlsx: incluye información acerca de las tecnologías disponibles por localidad, como así también la población y ubicación de las mismas.    


 En primer lugar se realiza control y tratamiento de valores nulos o duplicados en los datasets, y luego se crean distintas visualizaciones que resaltan información relevante, dentro de las cuales se destacan:

+ Evolución anual de accesos cada 100 hogares.
+ Distribución de la cantidad de accesos por Provincia.
+ Accesos por Tipo de Banda.
+ Accesos por Tipo de tecnología utilizada.
+ Accesos por Rango de Velocidad.
+ Velocidad media de bajada por Provincia.
+ Entre otros.

Del análisis realizado se obtuvieron las siguientes **conclusiones**:

> - El índice de accesos cada 100 hogares se incrementó un 90% desde el primer trimestre de 2014 hasta el último de 2022.
> - La jurisdicción con mayor índice de accesos cada 100 hogares a cierre de 2022 es Capital Federal, con un valor de 122.73, es decir más de un acceso por hogar.
> - Existen provincias como Chaco, Formosa, Santa Cruz y Santiago del Estero donde el índice de accesos aún no supera el 50%.
> - Al cierre de 2022, más del 99% de las conexiones se realizan a traves de conexión por Banda Ancha.
> - A fines del mismo período, más del 50% de las conexiones se realizan utilizando tecnología de Cablemodem, seguidas por las conexiones de Fibra óptica; tecnologías su vez fueron las que más crecieron en los últimos años y que proveen de una velocidad de conexión más rápida.
> - El uso de la tecnología ADSL decrece de manera inversamente proporcional al crecimiento de Cablemodem.
> - Más del 70% de los accesos se realizan a través de una velocidad superior a los 30 Mbps y la velocidad promedio de descarga a nivel país es de 68.5 Mbps; sin embargo, existen 9 provincias en las cuales la velocidad media de descarga es inferior a 50 Mbps.

Por último, se realizan ciertas transformaciones sobre los dataframes y se exportan  a archivos csv para ser levantados en Power BI.

<br>

# DASHBOARD INTERACTIVO - POWER BI

Una vez logrado el entendimiento acerca de los datos con los que disponíamos, se procedió al desarrollo de un **Dashboard o Tablero de Control** en **Power BI**, incluido en el archivo [Telecomunicaciones_Internet_Dashboard.pbix](/Telecomunicaciones_Internet_Dashboard.pbix).

El mismo incluye diferentes gráficos y visualizaciones que permiten obtener, en un vistazo, una **idea general** acerca del **comportamiento y evolución del sector** en un período determinado. 

Se organiza en **3 páginas o tableros**:

> 1. **Portada**: Se presenta el tablero e incluye accesos directos a las demás páginas.

> 2. **Accesos**: Incluye información referente a la **cantidad de accesos a Internet** por provincia.
El mismo incluye:

+ **2 Segmentadores (filtros)**: por **año** y por **trimestre**.
+ **3 Tarjetas**: la primera incluye **tasa de accesos cada 100 hogares promedio** al **cierre del período**, la segunda incluye el **KPI** de **accesos al servicio de Internet** (a desarrollar en el punto siguiente), y la última incluye el **valor** de la **tasa de accesos cada 100 hogares objetivo** del **Trimestre siguiente**
+ **Tabla** que incluye la **tasa de accesos cada 100 hogares** y el **valor del KPI** al **cierre** del período analizado, por Provincia.
+ Visualización comparativa de la **evolución trimestral** de la **tasa de accesos** y el **KPI** de acceso al servicio de Internet.
+ **Gráfico de torta** representativo de la cantidad de **accesos por Tipo de Banda**.
+ **Gráfico de barras** comparativo de la cantidad de **accesos por Teconología utilizada** en la conexión.
+ **Gráfico de barras** comparativo de la cantidad de **accesos según rango de Velocidad** en la conexión.

Todos los gráficos descriptos se pueden **consultar a nivel país, o a nivel Provincia** seleccionando alguna de ellas desde la tabla.


> 3. **Velocidad y Fibra óptica**: Incluye información referente a la **velocidad media de descarga** por provincia y cantidad de **localidades con acceso** a la tecnología de **Fibra Óptica**.
El mismo incluye:

+ **2 Segmentadores (filtros)**: por **año** y por **trimestre**.
+ **Tabla** que incluye la **velocidad media de descarga** , cantidad de **localidades**, cantidad de **localidades con acceso a Fibra Óptica** y el **valor del KPI de Fibra Óptica** al **cierre** del período analizado, por Provincia.
+ **Medidor** que incluye el **KPI** de **velocidad media mínima** por Provincia (a desarrollar en el punto siguiente).
+ **Gráfico de líneas** representativo de la **evolución trimestral** de la **velocidad media de descarga**.
+ **Medidor** que incluye el **KPI** de **localidades con acceso a Fibra Óptica**  (a desarrollar en el punto siguiente).
+ **Gráfico de líneas** representativo de la **evolución trimestral** de la **participación de Fibra Óptica** sobre el **total de accesos a Internet**.
+ **Tooltip** con el **mapa** de puntos de acceso a la **red de Fibra Óptica en Argentina**.

En este caso también se pueden consultar todos los gráficos descriptos **a nivel país, o a nivel Provincia** seleccionando alguna de ellas desde la tabla.
<br>

## Observaciones efectuadas

Del análisis realizado a través de los Dashboards implementados, se identificó un **punto crítico** en la **prestación del servicio**: la **gran diferencia** en la **velocidad media de bajada entre jurisdicciones**; si bien la **velocidad media a nivel país** es de **68.5 Mbps**, existen **9 provincias** con una **velocidad media inferior** a los **50 Mbps**.

Por otro lado, se observa que existe una **relación directa** entre el **crecimiento** en la **velocidad media de descarga** a través de los años, con el **crecimiento** de los **accesos** a través de **Fibra óptica**, por lo que el **incremento** en las conexiones a traves **de esta tecnología** se define como vía de **acción clave** para la **mejora** en la **prestación del servicio**.

Como consecuencia de todo lo descripto anteriormente, se establecieron los **indicadores claves de desempeño (KPI)** descriptos en el siguiente apartado.

## Indicadores clave de Desempeño (KPIs)

El Dashboard incluye los siguientes Indicadores Clave de Desempeño (KPIs):

> + Acceso al servicio de Internet: **(Nuevoacceso / Accesoactual - 1) * 100**

Este KPI mide la **variación trimestral** de la **tasa de accesos cada 100 hogares**. Permite el cálculo a nivel país (tomando el promedio de la tasa de accesos de las provincias). El **objetivo** planteado es que este **indicador** sea **igual o superior al 2%**, por provincia, en el trimestre.

> + Velocidad media de descarga **mínima**:

Se define que la **velocidad media por provincia y a nivel país** debe ser **superior** a los **70 Mbps** al cierre del próximo año. Esto podría lograrse a través de un mayor acceso a la tecnología de Fibra óptica, por lo que se definió otro indicador complementario, descripto a continuación:

> + % Localidades con acceso a Fibra óptica: **(LocalidadesFibraOptica / Total_Localidades) * 100**

Este KPI mide la **proporción de localidades** que cuentan con la tecnología de **Fibra óptica sobre** el **total de localidades** por provincia (o a nivel país). Se establece como objetivo que este indicador **debe ser superior al 50%** en el cierre del próximo año.

Se estima que **de cumplirse** estos indicadores clave, **se obtendrá un crecimiento** en la cantidad de **accesos** a una mayor **velocidad**, obteniendo una **mejora en la prestación del servicio**.

<br>


# Índice de Archivos del Repositorio

## Carpeta Datasets

+ Carpeta **Archivos Power BI**: incluye los archivos en formato csv utilizados en el Dashoard de Power BI.
+ [Dataset - Accesos a Internet por Tecnología](Accesos_por_tecnología.xlsx)
+ [Dataset - Velocidad media de bajada por Provincia](Historico_Velocidad.xlsx)
+ [Dataset - Accesos a Internet por Rangos de Velocidad](Internet_Accesos_Velocidad.xlsx)
+ [Dataset - Accesos a Internet por Tipo de Banda](Internet_BAF.xlsx)
+ [Dataset - Accesos a Internet cada 100 Hogares](Internet_Penetracion.xlsx)
+ [Dataset - Disponibilidad de Tecnologías por Localidad](mapa_conectividad.xlsx)

## Carpeta Imagenes

+ Incluye imágenes utilizadas en el dashboard y README.

## Carpeta raíz del repositorio

+ [EDA - Jupyter Notebook](EDA.ipynb)
+ [Dashboard: Internet en Argentina (Power BI)](Telecomunicaciones_Internet_Dashboard.pbix)


# Fuentes de datos

+ Los datasets fueron extraídos de la [página oficial de datos abiertos de ENACOM](https://datosabiertos.enacom.gob.ar/dashboards/20000/acceso-a-internet/).

+ [Puntos de acceso a la red de Fibra Óptica en Argentina](https://datos.gob.ar/dataset/arsat-puntos-conexion-refefo).
<br/>
