# aqi-forecasting-delhi-ncr
Leakage-aware AQI forecasting using scenario-based and time-series models

# Air Quality Forecasting in Delhi–NCR
Leakage-aware AQI forecasting under realistic forecasting constraints

---

## Overview
This project investigates **6-hourly Air Quality Index (AQI) prediction** for the Delhi–NCR region  
(06:00, 12:00, 18:00, and 23:00).

The study examines AQI prediction under **different information constraints**, ranging from full data availability to realistic forecasting setups where only past and known information is available. The goal is to understand how predictive performance changes when models are designed to avoid data leakage.

---

## Dataset
The analysis uses data collected from multiple monitoring stations across Delhi–NCR, including:
- 6-hourly AQI values  
- Meteorological variables (temperature, humidity, wind speed, etc.)  
- Temporal and calendar features  
- Pollutant concentrations (used only for baseline reconstruction)
- ## Dataset Information

The raw dataset used in this project exceeds GitHub’s file size limit.

Due to size constraints, the data file is not included in the repository.

Source:
- Central Pollution Control Board (CPCB) / official AQI monitoring sources

The dataset contains:
- 6-hourly AQI values (06, 12, 18, 23)
- Pollutant concentrations
- Meteorological variables
- Multiple monitoring stations across Delhi–NCR

Preprocessing steps are documented inside the notebooks.


---

## Modeling Framework
AQI prediction is evaluated under three distinct scenarios:

1. **Baseline AQI reconstruction (upper bound)**  
   Uses pollutant indicators that directly contribute to AQI calculation. Target leakage is intentionally allowed to establish a reference performance ceiling.

2. **Sensor-free early warning model**  
   Predicts AQI using only meteorological and temporal information, without relying on pollutant measurements.

3. **Lag-based time-series forecasting model**  
   A realistic forecasting setup that uses only historical AQI values and calendar features known at prediction time.

---

## Results Summary
The results highlight the **trade-off between information availability and predictive performance**.  
Models with more information achieve higher accuracy, while leakage-safe forecasting models provide more realistic and reliable performance estimates.

---

## Repository Structure
The repository is organized into four notebooks:

- `01-eda.ipynb` — Exploratory data analysis  
- `02-baseline-reconstruction.ipynb` — Upper-bound AQI reconstruction (leakage allowed)  
- `03-early-warning-model.ipynb` — Sensor-free AQI prediction  
- `04-lag-based-aqi-forecasting.ipynb` — Final leakage-safe forecasting model  
