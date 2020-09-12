# Producción de carne vs Producción de 4 cultivos base de la alimentacion basada en plantas. Exploración sus emisiones históricas y predicción.
# Table of Contents
* [Resumen](# Resumen)
* [1.Introducción](## 1.Introducción)
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
    * [2_2_1_Accuracy](#2_2_1_Accuracy)
    * [2_2_2_Precision](#2_2_2_Precision)
    * [2_2_3_Recall or Sensitivity](#2_2_3_Recall-or-Sensitivity)
    * [2_2_4_F1 score](#2_2_4_F1-score)
    * [2_2_5_Classification Report](#2_2_5_Classification-Report)
    * [2_2_6_ROC Curve_Receiver Operating Characteristic Curve](#2_2_6_ROC-Curve_Receiver-Operating-Characteristic-Curve)
    * [2_2_7_AUC_Area Under the Curve](#2_2_7_AUC_Area-Under-the-Curve)
    * [2_2_8_Confusion Matrix](#2_2_8_Confusion-Matrix)
* [3_Cross Validation Score](#3_Cross-Validation-Score)
* [4_Testing Parameters](#4_Testing-Parameters)
  * [4_1_GridSearchCV](#4_1_GridSearchCV)
  * [4_2_RandomizedSearchCV](#4_2_RandomizedSearchCV)
* [5_Ensemble Learning](#5_Ensemble-Learning)
  * [5_1_VotingClassifier](#5_1_VotingClassifier)
  * [5_2_Bagging or Bootstrap Aggregation](#5_2_Bagging-or-Bootstrap-Aggregation)
  * [5_3_Random Forest Regressor](#5_3_Random-Forest-Regressor)
  * [5_4_Random Forest Classifier](#5_4_Random-Forest-Classifier)  
  * [5_5_Gradient Boosting Regressor](#5_5_Gradient-Boosting-Regressor)
  * [5_6_Gradient Boosting Classifier](#5_6_Gradient-Boosting-Classifier)
* [6_References](#6_References)

# Resumen
En este análisis, visualizamos las emisiones de gases de efecto invernadero producidas por 2 sectores controversiales del Paraguay, la ganadería bovina y la producción agrícola, más específicamente, 4 cultivos que son la base en la producción de alimentos sustitutos de la carne vacuna (soja, maiz, trigo y guisantes). El periodo de estudio fue de 1961 a 2035, visualización de las emisiones desde 1961 a 2017 y predicción hasta el 2035. Esto, debido a que los datos públicos están disponibles desde 1961 a 2017 y la predicción hasta el 2035 ya que la politica agraria nacional se analizará recién en ese año.
La visualización de ambas variables determinaron una tendencia ascendente. Para el periodo 1961-2017, la emisión de GHG de los 4 cultivos, aumentó 30 veces más que en sus inicios. La ganadería aumento casi 4 veces más, sin embargo cabe resaltar que en sector se emite principalmente CH4 y NO2, 2 gases con potencial de calentamiento mucho mayor al CO2. Las predicciones tampoco fueron nada esperanzadoras. El aumento de las emisiones de los cultivos es casi exponencial y la ganaderia siguiria creciendo.

# Introducción



