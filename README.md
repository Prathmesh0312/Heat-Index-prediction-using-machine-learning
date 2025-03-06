# Heat-Index-prediction-using-machine-learning
# Heat Island Index Prediction Using machine learning- EY Open Science AI & Data Challenge 2025

## Project Overview
This project aims to develop a machine learning model to predict **Urban Heat Island (UHI) Index** values for locations across the **Bronx** and **Manhattan** regions in **New York City**. The prediction is based on data collected on **24 July 2021**, leveraging features derived from:

- Satellite imagery (Sentinel-2 and Landsat)
- Local weather data from the New York State Mesonet
- Building footprint data

The target variable is the **UHI Index**, which quantifies the relative near-surface air temperature at a given location compared to the average temperature across all locations recorded during the collection window (3:00 pm - 4:00 pm).

---

## Objective
The primary objective is to build an **open-source machine learning model** capable of accurately predicting UHI Index values at high spatial resolution (meter scale). This model will help urban planners, climate scientists, and local governments better understand the severity and spatial distribution of urban heat islands.

**Note:** The use of latitude and longitude as predictive features is strictly prohibited in this challenge.

---

## Data Sources
The model will be trained on and can leverage the following datasets:

### 1. Ground-Based Temperature Data (Target Variable)
- 11,229 UHI index values collected via vehicle traverses across Bronx and Manhattan.
- Data collected by **CAPA Strategies** as part of the **Heat Watch** program.
- Collection date: **24 July 2021** (3:00 pm - 4:00 pm).

### 2. Building Footprint Data
- Provided by the **Cornell University Geospatial Information Repository (CUGIR)**.
- Captures building density, which influences heat retention and airflow.

### 3. Sentinel-2 Satellite Data
- Optical multispectral data, 10-meter resolution.
- Provides vegetation indices (NDVI), surface reflectance, and urban density information.
- Processed using cloud-free mosaics (June-August 2021).

### 4. Landsat Land Surface Temperature (LST)
- Thermal infrared data from **NASA's Landsat** mission.
- Resolution: 100 meters.
- Captures surface temperatures of buildings, roads, vegetation, and water.
- Closest available scene: **16 June 2021**.

### 5. Local Weather Data
- Sourced from the **New York State Mesonet**.
- Parameters: Temperature, Relative Humidity, Wind Speed, Wind Direction, and Solar Flux.
- Data captured every 5 minutes at two weather stations within the study area.

---

## Modeling Guidelines
- **Prohibited Feature:** Latitude and longitude must not be used directly as features in the model.
- **Target Variable:** UHI Index.
- **Training Data Split:** Standard 70/30 train-test split.
- **Model Type:** Open choice — regression models, ensemble techniques, or neural networks are all allowed.
- **Evaluation Metric:** R-squared (coefficient of determination).

---

## Expected Outcomes
- Accurate prediction of UHI Index values across the Bronx and Manhattan.
- Identification of **key drivers** of urban heat, such as:
    - Building density
    - Vegetation cover
    - Proximity to water
    - Local weather conditions (wind, humidity, solar flux)

---

## Repository Structure
```text
├── data/                    # Processed and raw data files
├── notebooks/                # Jupyter Notebooks for EDA, modeling, and visualization
├── models/                    # Trained models and performance reports
├── src/                       # Scripts for data preprocessing, feature engineering, and modeling
├── README.md                  # Project documentation (this file)
└── requirements.txt           # Environment dependencies
