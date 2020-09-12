# Producción de carne vs Producción de 4 cultivos base de la alimentación basada en plantas. Exploración de sus emisiones históricas y predicción.

# Tabla de contenido

* [0_Resumen](#0_Resumen)
* [1_Introducción](#1_Introducción)
* [2_Descripción de los datos](#2_Descripción_de_los_datos)
* [3_Metodología](#3_Metodología)
 * [3_1_Muestra_y_variables](##3_1_Muestra_y_variables)
 * [3_2_Procesamiento de datos](##3_2_Procesamiento_de_datos)
   * [3_2_2_Preprocesamiento de datos](###3_2_2_Preprocesamiento_de_datos)
 * [3_3_Comprobación de estacionariedad de las Seriesb Temporales](##3_3_Comprobación_de_estacionariedad_de_las_Series_Temporales)
 * [3_4_Forecasting](##3_4_Forecasting)

# 0_Resumen

En este análisis, visualizamos las emisiones de gases de efecto invernadero producidas por 2 sectores controversiales del Paraguay, la ganadería bovina y la producción agrícola, más específicamente, [4 cultivos](https://link.springer.com/article/10.1007/s11367-015-0931-6) que son la base en la producción de alimentos sustitutos de la carne vacuna (soja, maiz, trigo y guisantes). 

El periodo de estudio fue de 1961 a 2035, la visualización de las emisiones fue desde 1961 a 2017 y la predicción hasta el 2035. Esto, debido a que los datos públicos están disponibles desde 1961 a 2017 y la predicción hasta el 2035, ya que la politica agraria nacional se analizará recién en ese año.

La visualización de ambas variables determinaron una tendencia ascendente. Para el periodo 1961-2017, la emisión de GHG de los 4 cultivos, aumentó 30 veces más que en sus inicios. La ganadería aumento casi 4 veces más, sin embargo, cabe resaltar que en sector se emite principalmente CH4 y NO2, 2 gases con potencial de calentamiento mucho mayor al CO2. Las predicciones tampoco fueron nada esperanzadoras. El aumento de las emisiones de los cultivos es casi exponencial y la ganaderia seguiría en aumento.

# 1_Introducción

Paraguay es un país principalmente agrícola - ganadero. Su economía esta basada en actividades primarias, es racional decir que las emisiones de gases de efecto invernadero (GHG), provienen principalmente de estos sectores primarios. Actualmente existen casi [3 cabezas de ganado vacuno por habitante](https://www.senacsa.gov.py/index.php/Temas-pecuarios/estadisticas) en el país, y casi [2 toneladas de soja por habitante ](http://www.agr.una.py/ecorural/cultivo/soja_marzo_2020.pdf). Los datos son realmente abrumadores, para un país con apenas [7.000.000 de habitantes](http://www.fao.org/faostat/es/#data/OA).

El análisis de las emisiones que provienen de estos 2 sectores, nos permite visualizar de alguna manera el impacto ambiental que tienen estas actividades en el país y poder incluso compararlas con otros sectores en el futuro.

Este análisis lo realice, con el fin de poder aportar un poco de claridad en las publicaciones sobre emisiones de GHG provenientes de dichos sectores. Ya que muchas, estan sesgadas debido a la fuente de la cual provienen esos resultados.

El objetivo principal de este estudio es: crear una línea de tiempo con la emisión de GHG correspondientes a cada sector, desde 1961 (fecha desde que se tienen datos) hasta la nueva revisión de la politica agraria (2035).

# 2_Descripción_de_los_datos

Los datos de emisión de GHG del sector ganadería, fueron obtenidos de la base de datos de la [FAO](http://www.fao.org/faostat/es/#data).

Las emisiones provenientes de la ganadería se dividen en 2 fuentes de emisión:

- Fermentación entérica: es un proceso digestivo por el cual los micro-organismos descomponen los carbohidratos en moléculas simples para la absorción en el flujo sanguíneo). La cantidad de metano que se libera depende del tipo de tracto digestivo, la edad y el peso del animal, así como de la calidad y la cantidad del alimento consumido. 
 
 - Gestión del estiércol: es el CH4 y el NO2 producido durante el almacenamiento y el tratamiento del estiércol, así como del estiércol depositado en la pastura. El término «estiércol» se utiliza aquí, colectivamente, de modo que incluye la bosta y la orina (es decir, los sólidos y los líquidos) producidos por el ganado. Los principales factores que inciden en las emisiones de CH4 son la cantidad de estiércol que se produce y la porción que se descompone anaeróbicamente. 

Los datos provenientes de los 4 cultivos (soja, trigo, maiz, guisantes), fueron obtenidos mediante el cálculo en base a la metodología del [IPCC 2006](https://www.ipcc-nggip.iges.or.jp/public/2006gl/spanish/pdf/4_Volume4/V4_05_Ch5_Cropland.pdf). Esto, debido a que los datasets disponibles no tratan la información de emisión de GHG individualmente por tipo de cultivo, sino, como un conjunto que se declara como "Emisiones provenientes de Tierras de cultivo". En este apartado, explicaré brevemente la metodología de cálculo.

El cálculo de las emisiones por tipo de cultivo tiene en cuenta 6 variables: 

    - Categoría (Cultivos anuales o temporales), 
    
    - Área de cultivo, 
    
    - Carbono de referencia CF (parámetro que se establece de acuerdo a la regimen climático de la zona), 
    
    - Factor de cambio para sistemas de uso de la tierra FLU (parametro de cambio de carbono de acuerdo al sistema de cultivo y al régimen hidrico), 
    
    - Factor de cambio para sistemas de manejo FMG (parametro dependiente del sistema de manejo de cultivo), 
    
    - Factor de cambio para la entrada de materia órganica FI (parámetro que establece la entrada de carbono anual en los suelos).

Esto da como resultado las exitencias de carbono de los cultivos en ton C, que deben ser multiplicadas por 44/12 para convertirlas a tonCO2. Siguiendo el mismo proceso para cada cultivo y para cada año de cálculo.

# 3_Metodología

## 3_1_Muestra_y_variables

El análisis se realizó, teniendo en cuenta 2 variables: 

  - Emisiones de gases de efecto invernadero generadas en el Paraguay por la ganadería vacuna. Los datasets estan disponibles [aquí](http://www.fao.org/faostat/es/#data)
  
  - Emisiones de gases de efecto invernadero producidas por 4 cultivos primarios en la alimentación basada en plantas. La metodología utilizada para el cálculo de estos datos esta disponible [aquí](https://www.ipcc nggip.iges.or.jp/public/2006gl/spanish/pdf/4_Volume4/V4_05_Ch5_Cropland.pdf)


# 3_2_Procesamiento_de_datos:

# 3_2_1_Para_el_análisis:

Herramientas:

- Jupyter notebook
- Python 3

En el entorno:
```python
- import numpy as np
- import pandas as pd
- import matplotlib.pyplot as plt
- import statsmodels as sm
- import statsmodels.api as sm
```

Modelo:
```python
- from statsmodels.tsa.statespace.sarimax import SARIMAX
```

Gráficos de métricas y métricas:
```python
- from statsmodels.tsa.stattools import acf
- from statsmodels.tsa.stattools import pacf
- from statsmodels.graphics.tsaplots import plot_acf
- from statsmodels.graphics.tsaplots import plot_pacf
- from statsmodels.tsa.stattools import adfuller
- from statsmodels.tsa.seasonal import seasonal_decompose
- from sklearn.metrics import mean_squared_error, r2_score, mean_absolute_error, median_absolute_error, mean_squared_log_error
```
### 3_2_2_Preprocesamiento_de_datos

Los datos de emisión de la ganadería se obtienen por separado: [Fermentación entérica](https://github.com/Paola-almiron/Final_proyect_DS/blob/master/FAOSTAT_data_enteric1960.csv) y [Gestión del estiércol](https://github.com/Paola-almiron/Final_proyect_DS/blob/master/FAOSTAT_data_manure1960.csv). Debemos fusionarlos, eliminar variables que no se utilizarán y luego sumar las emisiones de ambas para obtener las emisiones totales de ese sector.

Los datos de emisión de los cultivos se calcularon en 4 archivos.xlsx: [Emisión de la soja](https://github.com/Paola-almiron/Final_proyect_DS/blob/master/soy_emissions1961.xlsx), [Emisión del trigo](https://github.com/Paola-almiron/Final_proyect_DS/blob/master/wheat_emissions1961.xlsx), [Emisión del maiz](https://github.com/Paola-almiron/Final_proyect_DS/blob/master/corn_emissions1961.xlsx) y [Emision de guisantes](https://github.com/Paola-almiron/Final_proyect_DS/blob/master/pea_emissions1961.xlsx). Debemos fusionar los 4, eliminar las variables que fueron utlizadas para el cálculo y sumar las emisiones para obtener los totales del sector.

## 3_3_Comprobación_de_estacionariedad_de_las_Series_Temporales

Una vez realizada la limpieza de datos, debemos comprobar si son estacionarios. Esto, debido a que el modelo ARIMA (modelo que utilizaremos para la predicción de nuestras variables), exige que las series sean estacionarias.

Se utilizaron 3 métodos para la comprobacion de la estacionariedad:

- ACF: proporciona la estructura de dependencia lineal de la misma.
- PACF: proporciona la relación directa que existe entre observaciones separadas por k retardos 
- Rolling mean: de forma visual podemos identificar si la serie es estacionaria o no
- Test de Dickey-Fuller: la forma matemática de identificar si la serie es estacionaria. h0 = raíz unitaria está presente en una muestra de series de tiempo.

Ambas series son NO estacionarias, por lo que aplicamos el método de diferenciación para estacionarlas y así realizar la predicción.

## 3_4_Forecasting

Las predicciones se realizaron con SARIMAX. 

Para determinar el orden (p,d,q), entrenamos diferentes ordenes para el modelo. Utilizamos las paramétricas de AIC Y BIC para determinar la mejor combinación. La 'd' es la diferenciación que realizamos para estacionar cada serie. p = el mejor AIC, q = mejor BIC.

Una vez obtenido el mejor orden para nuestros modelos, dividimos el dataset en train y test con una proporción de 90:10, esto, debido a que ambas series son pequeñas (56 datos cada una).

Realizamos las predicciones para ambas series, hasta el año 2035.

Utilizamos las métricas para determinar la bondad de nuestro modelo predictivo, tanto el modelo predictivo de la ganaderia, como la de los cultivos, poseen un ajuste bueno de prediccion, con un r2 score >~ 0.90, MAPE < 10 para ambas predicciones. El RSME de la ganaderia es de 887 Gg de CO2, considero es bajo, ya que las emisiones son mayores a 10.000Gg CO2. El RMSE de los cultivos es de 174 Gg de CO2, y también lo considero un valor bajo, debido a que las emisiones son mayores a 5000 Gg de CO2.





























