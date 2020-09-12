# Producción de carne vs Producción de 4 cultivos base de la alimentación basada en plantas. Exploración sus emisiones históricas y predicción.

# Tabla de contenido

* [0_Resumen](#0_Resumen)
* [1_Introducción](#1_Introducción)
* [2_Descripción de los datos](#2_Descripción_de_los_datos)
* [3_Metodología](#3_Metodología)
* [6_References](#6_References)

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

El análisis se realizó, teniendo en cuenta 2 variables: las emisiones de gases de efecto invernadero generadas en el Paraguay por la ganadería vacuna y las emisiones de gases de efecto invernadero producidas por 4 cultivos primarios en la alimentacion basada en plantas.

# 3_2_Procesamiento_de_datos
```python jsdfkaslkjdfwñlsf

```






