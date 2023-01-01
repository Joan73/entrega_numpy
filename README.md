===================
Tercera entrega
===================

Autor:
    Joan Pont Escanellas

Este repositorio contiene la tercera entrega de ejercicios de la segunda parte de la asignatura. Fundamentalmente se analizan un total de 3 dataset diferentes utilizando solamente la librería numpy. Cada dataset tiene su análisis correspondiente en un notebook diferente.

Se recomienda previamente tener un environment limpio y utilizar el comando "$ pip install requirements.txt" para tener los paquetes necesarios para ejecutar el archivo en python. Aunque básicamente hemos usado la librería numpy para realizar el análisis y la librería matplotlib para realizar algún gráfico.

A continuación presentamos las conclusiones que se han extraído del análisis de los tres conjuntos de datos. Si se desea consultar el código, los gráficos y los resultados obtenidos, se recomienda consultar los notebooks.

DATOS A:

Este dataset contiene un total de 5 indicadores demográficos sobre los diferentes municipios de las islas baleares. En particular los 5 indicadores son:

- Nacidos vivos por residencia materna.
- Muertes fetales tardías por residencia materna.
- Matrimonios por el lugar en que han fijado residencia.
- Fallecidos por el lugar de residencia.
- Crecimiento vegetativo.

En el notebook podemos encontrar una descripción detallada del código y algunos gráficos ilustrativos. Hemos tratado de conocer la distribución de estos 5 indicadores calculando la media, mediana y desviación típica de cada uno de ellos. 

Concluimos que la variación en los datos es significativa. De hecho la desviación estándar en todos los indicadores es bastante alta. Por tanto, si quisiésemos aplicar algún modelo, tal vez deberíamos primero estandarizar los datos. A no ser que nos interese conservar esta varianza por algún motivo en el análisis. 

Por otro lado, vemos que en todos los indicadores la media y la mediana son significativamente diferentes. De hecho, en todos los casos la media es significativamente más alta que la mediana. Por tanto podemos deducir que la distribución de los 5 indicadores no es simétrica. Será en su defecto sesgada a la derecha (tendrá una asimetría positiva). Es decir, los datos se concentran en la parte inferior de la distribución.

DATOS B:

Este dataset contiene 534 observaciones con 24 variables que contienen información de ventas de viviendas en NYC. Las 24 variables proporcionan muchísima información contextual acerca de la vivienda. Hay información como el distrito, el número de identificación del edificio, el lote, la latitud, longitud, código postal, distrito del consejo, etc. También contiene información numérica como el precio o la tasa de capitalización. Concretamente nosotros hemos seleccionado para analizar el identificador del municipio, el precio de la vivienda y la tasa de capitalización. 

Hemos observado que hay 3 municipios diferentes con una cantidad similar de viviendas vendidas. Todos están por encima de las 140 viviendas vendidas. En cambio tenemos un municipio con alrededor de 60 viveindas. Y, un municipio con tan solo 4 viviendas vendidas. Es importante tener en cuenta la cantidad de observaciones para un análisis correcto. Fijémonos que el municipio con tan solo 4 observaciones no es estadísticamente significativo en comparación con el resto. Pero también nos puede proporcionar información: Tal vez ese municipio es muy exclusivo o limitado en términos de superficie y por tanto hay menos viviendas.

También podemos concluir que los precios de las viviendas varían mucho dentro de cada municipio. Por tanto la media no es una buena medida de centralidad de los datos. De hecho hemos calculado dentro de cada municipio la probabilidad de que una vivienda tenga un precio superior a la media. Y, hemos visto, que en todos los muncipios esta probabilidad es baja. De aquí podemos deducir que hay un pequeño número de viviendas con un precio muy elevado que hacen que la media sea muy alta, pero el grueso de las observaciones se encuentra en la parte baja de la distribución.

Finalmente, hemos usado la moda como medida de centralidad en la serie de la tasa de capitalización de las viviendas por municipio debido a la varianza de los datos. Hemos visto que se espera una rentabilidad que se mueve entre el 2 y el 3 por ciento en todos los municipios. Está la excepción del municipio con 4 observaciones, que todas las viviendas tienen una tasa de capitalización diferente y la moda en este caso no tiene sentido (todas las observaciones se repiten una sola vez).


DATOS C:

Este dataset contiene la información del gasto público de diferentes países desde el año 2012 hasta el año 2020. En particular, las variables que hemos seleccionado para realizar el análisis es el código del país, el año y el gasto público. 

Hemos observado que hay un país, AT (Austria), que tiene información sobre el gasto público en el año 2021. El resto de países solo tienen la información hasta el año 2020. Gracias a la gráfica del tercer cuantil del gasto público por años, concluimos que el gasto público de la mayoría de países desde el año 2012 hasta el año 2019 tiene una tendencia negativa clara. Pero, en el año 2020, el gasto público aumenta muy significativamente en comparación al resto de años. Lo atribuimos a la pandemia.

También hemos observado que la variación en el gasto público por países no es muy elevada. Si observamos los datos, vemos que la variación se mueve entre 2 y 5 puntos. Por tanto podemos deducir que la distribución de los datos es (aproximadamente) simétrica. El hecho de que la variación no sea muy significativa, es probablemente debido al hecho de que todos los países que tenemos en el dataset son de Europa. Posiblemente si hubiese observaciones de otros países asíaticos, africanos o americanos, la variación sería más considerable.















