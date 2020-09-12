# Producción de carne vs Producción de 4 cultivos base de la alimentacion basada en plantas. Exploración sus emisiones históricas y predicción.
# Table of Contents
* [0_Resumen](#0_Resumen)
* [1_Introducción](#1_Introducción)
  * [1_1_Regression](#1_1_Regression)
    * [1_1_1_Linear Regression](#1_1_1_Linear-Regression)
    * [1_1_2_K-Nearest Neighbor Regressor_KNN)](#1_1_2_K-Nearest-Neighbor-Regressor_KNN)
    * [1_1_3_Decision Tree Regressor](#1_1_3_Decision-Tree-Regressor)
  * [1_2_Classification](#1_2_Classification)
    * [1_2_1_Logistic Regression](#1_2_1_Logistic-Regression)
    * [1_2_2_K Nearest Neighbor Classifier_KNN](#1_2_2_K-Nearest-Neighbor-Classifier_KNN)  
    * [1_2_3_Support Vector Machine_SVM](#1_2_3_Support-Vector-Machine_SVM)
    * [1_2_4_Decision_Tree_Classifier](#1_2_4_Decision-Tree-Classifier)
* [2_Metrics](#2_Metrics)
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
En este análisis, visualizamos las emisiones de gases de efecto invernadero producidas por 2 sectores controversiales del Paraguay, la ganadería bovina y la producción agrícola, más específicamente, 4 cultivos que son la base en la producción de alimentos sustitutos de la carne vacuna (soja, maiz, trigo y guisantes). 
El periodo de estudio fue de 1961 a 2035, la visualización de las emisiones fue desde 1961 a 2017 y la predicción hasta el 2035. Esto, debido a que los datos públicos están disponibles desde 1961 a 2017 y la predicción hasta el 2035, ya que la politica agraria nacional se analizará recién en ese año.
La visualización de ambas variables determinaron una tendencia ascendente. Para el periodo 1961-2017, la emisión de GHG de los 4 cultivos, aumentó 30 veces más que en sus inicios. La ganadería aumento casi 4 veces más, sin embargo, cabe resaltar que en sector se emite principalmente CH4 y NO2, 2 gases con potencial de calentamiento mucho mayor al CO2. Las predicciones tampoco fueron nada esperanzadoras. El aumento de las emisiones de los cultivos es casi exponencial y la ganaderia seguiría en aumento.

# 1_Introducción



