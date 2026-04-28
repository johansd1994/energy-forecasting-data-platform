# Predicción de Producción Energética

## Análisis y Forecasting de Producción de Petróleo y Gas en Colombia

![banner del proyecto](Images/Portada.png)

---

# Descripción del Proyecto

Los mercados energéticos son altamente dinámicos y están influenciados por múltiples factores económicos, geopolíticos y técnicos.

Este proyecto analiza y predice la **producción de petróleo y gas en Colombia**, así como su relación con **los precios internacionales de commodities energéticos**.

El proyecto integra varias áreas del análisis de datos:

* Ingeniería de datos
* Análisis exploratorio de datos
* Modelos de Machine Learning
* Modelos de series temporales
* Forecasting

El objetivo es construir modelos capaces de **predecir la evolución futura de la producción energética y analizar su relación con los precios internacionales**.

---

# Fuentes de Datos

Los datos utilizados provienen de fuentes públicas oficiales.

## Producción de Hidrocarburos

Fuente:

Portal de Datos Abiertos de Colombia
Agencia Nacional de Hidrocarburos (ANH)

Los datasets contienen información mensual sobre:

* Producción de petróleo (crudo)
* Producción de gas natural
* Campos petroleros
* Operadoras
* Ubicación geográfica

---

## Precios de Commodities

Fuente:

Federal Reserve Economic Data (**FRED**)

Series utilizadas:

* Precio del petróleo Brent
* Precio del gas natural Henry Hub

---

## Periodo Analizado

Los datos cubren el periodo:

**2014 – 2025**

Este rango permite analizar:

* tendencias de producción
* estacionalidad
* volatilidad de precios
* escenarios de predicción

---

# Arquitectura de Datos

El proyecto sigue una arquitectura moderna basada en el enfoque **Medallion Architecture**.

![arquitectura del proyecto](Images/ArquitecturaAWS.png)

La arquitectura se divide en tres capas principales.

### Capa Bronze

Contiene los datos originales descargados desde las fuentes externas sin modificaciones.

### Capa Silver

En esta capa se realizan procesos de limpieza, estandarización y transformación de los datos.

### Capa Gold

Se construye el modelo dimensional y las tablas analíticas utilizadas para análisis, visualización y modelos predictivos.

Esta arquitectura permite:

* mejorar la calidad de los datos
* asegurar trazabilidad
* facilitar el análisis analítico y predictivo

---

# Análisis Exploratorio de Datos

El análisis exploratorio permite entender el comportamiento histórico de la producción y los precios.

Los principales objetivos del EDA fueron:

* identificar tendencias de producción
* detectar estacionalidad
* analizar volatilidad
* explorar relaciones entre variables

Ejemplo de evolución de producción:

![producción histórica Crudo](Images/ProduccionTotalCrudo.png)
![producción histórica Gas](Images/Images/ProduccionTotalGas.png)
![producción histórica Precios](Images/PrecioMensualRecurso.png)

Principales hallazgos:

* La producción de petróleo muestra una tendencia descendente en el largo plazo.
* La producción de gas presenta patrones estacionales.
* Los precios internacionales presentan alta volatilidad.

El análisis de correlación muestra que **la relación entre producción y precio es muy baja**, por lo que ambos deben modelarse de forma independiente.

---

# Análisis de Series Temporales

Para comprender mejor la dinámica de la producción, se realizó una descomposición de las series temporales en:

* Tendencia
* Estacionalidad
* Componente residual

![descomposición de serie temporal Crudo](Images/SeriesComponentesCrudo.png)
![descomposición de serie temporal Gas](Images/SeriesComponentesGas.png)

Esta técnica permite entender la estructura subyacente de los datos y diseñar modelos predictivos más robustos.

Tambien se analizo los retornos mensuales de los precios 

![retornos mensuales de Precios](Images/RetornorMensualesPrecios.png)

---

# Modelos Predictivos

Se evaluaron diferentes enfoques para el forecasting.

## Modelos Estadísticos

* SARIMA
* Prophet

## Modelos de Machine Learning

* XGBoost

## Modelos de Deep Learning

* LSTM
* GRU

Los modelos fueron entrenados utilizando:

* variables rezagadas (lag features)
* variables temporales
* ingeniería de características

Ejemplos de predicción:

![predicción Produccion Crudo](Images/XGBoostProduccionCrudo.png)
![predicción Produccion Gas](Images/XGBoostProduccionGas.png)

---

# Evaluación de Modelos

El desempeño de los modelos fue evaluado utilizando métricas estándar de forecasting:

* MAE
* MAPE
* R²

Los resultados muestran que **los modelos de Machine Learning obtuvieron el mejor desempeño**, superando tanto a los modelos estadísticos tradicionales como a los modelos de deep learning.

Esto se debe principalmente al tamaño del dataset y a la efectividad del feature engineering aplicado.

---

# Escenarios de Predicción

Los mejores modelos fueron utilizados para generar **predicciones a 12 meses** para:

* producción de petróleo
* producción de gas
* precios de commodities

![predicciones futuras Crudo](Images/escenariosCrudo.png)

Y Se creo una matriz de sensibilidad economica por Commoditie debio a las diferentes posibilidades 

![matriz de Sensibilidad Crudo](Images/SensibilidadEconomicaCrudo.png)

Estas predicciones permiten analizar posibles escenarios futuros y apoyar procesos de toma de decisiones en el sector energético.

Para mas Información del proyecto, puede leer el documento adjunto con toda la linea de investigación

![Trabajo Fin de Master](PredicciónProducciónPrecios.pdf)

---

# Tecnologías Utilizadas

Python
Pandas
NumPy
Matplotlib
Seaborn

Scikit-learn
XGBoost
TensorFlow
Keras

Prophet
Statsmodels

Jupyter Notebook

---

# Estructura del Repositorio

```id="repo_struct_es"

proyecto
│
├── Data
│   ├── Produccion_Crudo.csv
│   ├── Produccion_Gas.csv
│   ├── precio_crudo.csv
│   ├── precio_gas.csv
│   └── README.md
│
├── notebook_forecasting.ipynb
│
├── requirements.txt
│
└── README.md

```

---

# Autor

Johan Mauricio Suarez Daza

Data Engineer | Data Scientist

Máster en Análisis de Datos Masivos (Big Data)
Universidad Europea de Madrid

