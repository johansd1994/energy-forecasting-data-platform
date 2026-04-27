# Data Sources

This folder contains the datasets used for the analysis and forecasting models in this project.

The data combines **oil and gas production data from Colombia** with **international commodity price data**.

---

# Production Data

The production datasets were obtained from the **Open Data Portal of Colombia** and the **Agencia Nacional de Hidrocarburos (ANH)**.

Source:
https://www.datos.gov.co/

The ANH publishes official statistics about hydrocarbon production in Colombia.

### Files

**Produccion_Crudo.csv**

Monthly crude oil production by field and operator.

**Produccion_Gas.csv**

Monthly natural gas production by field and operator.

### Variables (main)

Typical variables contained in the datasets include:

* date
* department
* municipality
* operator
* contract
* field
* production_volume

These datasets provide historical production information used for exploratory analysis and forecasting models.

---

# Commodity Price Data

The price datasets were obtained from the **Federal Reserve Economic Data (FRED)** platform.

Source:
https://fred.stlouisfed.org/

FRED provides publicly available economic and financial time series.

### Files

**precio_crudo.csv**

Monthly price of **Brent crude oil**, expressed in USD per barrel.

FRED Series:
Brent Crude Oil Price

**precio_gas.csv**

Monthly price of **Henry Hub Natural Gas**, expressed in USD per MMBtu.

FRED Series:
Henry Hub Natural Gas Spot Price

---

# Time Period

The combined datasets cover the period:

2014 – 2025

This time range allows the analysis of:

* production trends
* seasonal patterns
* commodity price dynamics
* forecasting scenarios

---

# Purpose of the Data

These datasets are used to:

* analyze historical production of oil and gas in Colombia
* explore the relationship between production and international prices
* build forecasting models using machine learning and time series techniques
* generate production and price projections

