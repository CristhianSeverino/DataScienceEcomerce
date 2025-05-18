# DataScienceEcomerce
Aplicacion de Kmeans para la optimizacion comercial y operativa de una empresa cuyo principal modelod e comercializacion es a traves de su E-Comerce
# Proyecto de Segmentación de Clientes con K-Means

## Descripción del Proyecto

Este proyecto se enfoca en la segmentación de clientes de una empresa de comercio electrónico utilizando el algoritmo de clustering K-means. El objetivo es identificar grupos de clientes con comportamientos similares para permitir un análisis posterior más detallado y la generación de estrategias de marketing personalizadas. El análisis incluye un Análisis Exploratorio de Datos (EDA) para comprender mejor los datos y preparar las variables para el modelado.

## Objetivos Específicos

1.  **Análisis Exploratorio de Datos (EDA):**
    * Importación y limpieza de datos.
    * Creación de variables de comportamiento del cliente (Frecuencia de Compra, Valor Total, Recencia, Variedad de Productos, Cantidad Total).
    * Análisis de la distribución de las variables y detección de valores atípicos.
    * Visualización de correlaciones entre las variables.

2.  **Modelado con K-Means:**
    * Escalado de variables para el algoritmo K-means.
    * Determinación del número óptimo de clusters utilizando el método del codo y el análisis de silueta.
    * Aplicación del algoritmo K-means para segmentar a los clientes.
    * Visualización de los clusters en 2D y 3D utilizando PCA.
    * Análisis de las características de cada segmento de clientes.

3.  **Generación de Descargables para Análisis Posterior:**
    * Creación de archivos CSV con el conteo de clientes por segmento, el promedio de las características por segmento y el DataFrame completo con la segmentación.

## Estructura del Código

El código se organiza de la siguiente manera:

1.  **Importación de Librerías:** Se importan las librerías necesarias para el análisis de datos, el modelado y la visualización.
2.  **Importación de Datos:** Se carga el conjunto de datos de comercio electrónico desde un archivo CSV.
3.  **Limpieza de Datos:** Se eliminan los valores faltantes en la columna `CustomerID` y se imputan los valores faltantes en la columna `Description`.
4.  **Creación de Variables de Comportamiento del Cliente:** Se calculan las siguientes métricas para cada cliente:
    * Frecuencia de Compra
    * Valor Total Gastado
    * Recencia (días desde la última compra)
    * Variedad de Productos Comprados
    * Cantidad Total de Artículos Comprados
5.  **Modelado con K-Means:**
    * Se escalan las variables de segmentación utilizando `StandardScaler`.
    * Se aplica el algoritmo K-means para diferentes valores de k (número de clusters) y se grafica la inercia para determinar el número óptimo de clusters (método del codo).
    * Se realiza un análisis de silueta para evaluar la calidad del clustering para diferentes valores de k.
    * Se aplica K-means con el número óptimo de clusters y se asigna cada cliente a un segmento.
6.  **Análisis y Visualización de Segmentos:**
    * Se realizan análisis gráficos para visualizar las características de los segmentos de clientes, incluyendo:
        * Matriz de correlación de las variables de segmentación.
        * Gráficos de dispersión de las variables de segmentación por segmento.
        * Boxplots de las variables de segmentación por segmento.
        * Gráfico de coordenadas paralelas de los clusters.
        * Conteo de clientes por segmento.
        * Visualización de los clusters en 2D y 3D utilizando PCA.
7.  **Generación de Descargables:** Se generan archivos CSV con el conteo de clientes por segmento, el promedio de las características por segmento y el DataFrame con la segmentación para facilitar el análisis posterior.

## Librerías Utilizadas

* pandas
* numpy
* matplotlib
* seaborn
* scikit-learn (KMeans, StandardScaler, PCA, silhouette\_score, silhouette\_samples)
* plotly
* google.colab (para descargar archivos)

## Resultados

El proyecto genera como resultado una segmentación de los clientes en grupos con comportamientos similares. Esta segmentación puede utilizarse para:

* Comprender mejor a los clientes de la empresa.
* Identificar oportunidades de marketing personalizadas.
* Mejorar la retención de clientes.
* Optimizar la asignación de recursos.

Los resultados del clustering se visualizan a través de diferentes gráficos, incluyendo gráficos de dispersión, boxplots y gráficos de coordenadas paralelas. Además, se generan archivos CSV con información detallada sobre los segmentos de clientes.

## Conclusiones

Este proyecto proporciona un análisis completo de la segmentación de clientes utilizando K-means. El EDA permite comprender los datos y seleccionar las variables relevantes para el modelado. El análisis de silueta ayuda a determinar el número óptimo de clusters, y las visualizaciones permiten interpretar los resultados del clustering de manera efectiva. Los archivos CSV generados facilitan el análisis posterior de los segmentos de clientes.
