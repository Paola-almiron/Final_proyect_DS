# Producción de carne vs Producción de 4 cultivos base de la alimentacion basada en plantas. Exploración sus emisiones históricas y predicción.
# Table of Contents
* [0_Resumen](#0_Resumen)
* [1_Introducción](#1_Introducción)
* [2_Descripción de los datos](#2_Descripción_de_los_datos)
  * [2_1_Regression](#2_1_Regression)
    * [2_1_1_MAE_Mean Absolute Error](#2_1_1_MAE_Mean-Absolute-Error)
    * [2_1_2_MAPE_Mean Absolute Percentage Error](#2_1_2_MAPE_Mean-Absolute-Percentage-Error)
    * [2_1_3_RMSE_Root Mean Squared Error](#2_1_3_RMSE_Root-Mean-Squared-Error)
    * [2_1_4_Correlation](#2_1_4_Correlation)
    * [2_1_5_Bias](#2_1_5_Bias)
    * [2_1_6_Variance](#2_1_6_Variance)
  * [2_2_Classification](#2_2_Classification)

* [6_References](#6_References)

# 0_Resumen
En este análisis, visualizamos las emisiones de gases de efecto invernadero producidas por 2 sectores controversiales del Paraguay, la ganadería bovina y la producción agrícola, más específicamente, [4 cultivos](https://link.springer.com/article/10.1007/s11367-015-0931-6) que son la base en la producción de alimentos sustitutos de la carne vacuna (soja, maiz, trigo y guisantes). 
El periodo de estudio fue de 1961 a 2035, la visualización de las emisiones fue desde 1961 a 2017 y la predicción hasta el 2035. Esto, debido a que los datos públicos están disponibles desde 1961 a 2017 y la predicción hasta el 2035, ya que la politica agraria nacional se analizará recién en ese año.
La visualización de ambas variables determinaron una tendencia ascendente. Para el periodo 1961-2017, la emisión de GHG de los 4 cultivos, aumentó 30 veces más que en sus inicios. La ganadería aumento casi 4 veces más, sin embargo, cabe resaltar que en sector se emite principalmente CH4 y NO2, 2 gases con potencial de calentamiento mucho mayor al CO2. Las predicciones tampoco fueron nada esperanzadoras. El aumento de las emisiones de los cultivos es casi exponencial y la ganaderia seguiría en aumento.

# 1_Introducción
Paraguay es un país principalmente agrícola - ganadero. Su economía esta basada en actividades primarias, es racional decir que las emisiones de gases de efecto invernadero (GHG), provienen principalmente de estos sectores primarios. Actualmente existen casi [3 cabezas de ganado vacuno por habitante](https://www.senacsa.gov.py/index.php/Temas-pecuarios/estadisticas) en el país, y casi [2 toneladas de soja por habitante ](http://www.agr.una.py/ecorural/cultivo/soja_marzo_2020.pdf). Los datos son realmente abrumadores, para un país con apenas [7.000.000 de habitantes](http://www.fao.org/faostat/es/#data/OA).
El análisis de las emisiones que provienen de estos 2 sectores, nos permite visualizar de alguna manera el impacto que tienen estas actividades en el país y poder incluso compararlas con otros sectores.
Este análisis lo realice, con el fin de poder aportar un poco de claridad en las publicaciones sobre emisiones de GHG provenientes de dichos sectores. Ya que muchas, estan sesgadas debido a la fuente de la cual provienen esos resultados.
El objetivo principal de este estudio es: crear una linea de tiempo con la emisión de GHG correspondientes a cada sector, desde 1961 (fecha desde que se tienen datos) hasta la nueva revisión de la politica agraria (2035).

# 2_Descripción de los datos

