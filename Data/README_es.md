# Fuentes de datos

Esta carpeta contiene los conjuntos de datos utilizados para los modelos de análisis y previsión de este proyecto.

Los datos combinan **datos de producción de petróleo y gas de Colombia** con **datos internacionales sobre los precios de las materias primas**.

---

# Datos de producción

Los conjuntos de datos de producción se obtuvieron del **Portal de Datos Abiertos de Colombia** y de la **Agencia Nacional de Hidrocarburos (ANH)**.

Fuente:
https://www.datos.gov.co/

La ANH publica estadísticas oficiales sobre la producción de hidrocarburos en Colombia.

### Archivos

**Produccion_Crudo.csv**

Producción mensual de petróleo crudo por yacimiento y operador.

**Produccion_Gas.csv**

Producción mensual de gas natural por yacimiento y operador.

### Variables (principales)

Las variables típicas que contienen los conjuntos de datos incluyen:

* fecha
* departamento
* municipio
* operador
* contrato
* yacimiento
* volumen_de_producción

Estos conjuntos de datos proporcionan información histórica sobre la producción que se utiliza para análisis exploratorios y modelos de pronóstico.

---

# Datos sobre precios de materias primas

Los conjuntos de datos sobre precios se obtuvieron de la plataforma **Federal Reserve Economic Data (FRED)**.

Fuente:
https://fred.stlouisfed.org/

FRED proporciona series temporales económicas y financieras de acceso público.

### Archivos

**precio_crudo.csv**

Precio mensual del **petróleo crudo Brent**, expresado en USD por barril.

Serie FRED:
Precio del petróleo crudo Brent

**precio_gas.csv**

Precio mensual del **gas natural Henry Hub**, expresado en USD por MMBtu.

Serie FRED:
Precio al contado del gas natural Henry Hub

---

# Período de tiempo

Los conjuntos de datos combinados abarcan el período:

2014 – 2025

Este intervalo de tiempo permite el análisis de:

* tendencias de producción
* patrones estacionales
* dinámica de los precios de las materias primas
* escenarios de pronóstico

---

# Finalidad de los datos

Estos conjuntos de datos se utilizan para:

* analizar la producción histórica de petróleo y gas en Colombia
* explorar la relación entre la producción y los precios internacionales
* construir modelos de pronóstico utilizando técnicas de aprendizaje automático y de series temporales
* generar proyecciones de producción y precios

Traducción realizada con la versión gratuita del traductor DeepL.com
