# Monitoring Air Pollution from Space Using Satellite Observations, Ground-Based Measurements, Reanalysis Data, and AI/ML Techniques

## Overview

This project aims to estimate surface-level PM2.5 concentrations across India by leveraging a fusion of satellite-based aerosol data, ground-based monitoring, and meteorological reanalysis datasets. Machine learning models are employed to understand the spatiotemporal variability of PM2.5 and to decouple the effects of emissions and meteorological factors. The study particularly focuses on Delhi and presents the first ML-based PM2.5 estimation model for the region using INSAT satellite data.

---

## Objectives

- Predict surface-level **PM2.5 concentrations** using remote sensing and meteorological inputs.
- Analyze the contribution of meteorology and emissions in observed PM2.5 trends.
- Evaluate the effectiveness of existing environmental policies in urban areas.
- Provide a framework for **data-driven air quality forecasting**.

---

## Data Sources

| Source | Parameters Used |:-

| **MERRA-2** | AOD (Aerosol Optical Depth) |
| **CPCB** | Ground-based Air Quality Monitoring | PM2.5 (target variable) |
| **ERA-2** | Reanalysis Data | T2M, WS10, WD10, PS, BLH, RH, Cloud Cover, Precipitation |

---

## Features Used

- **Meteorological:**  
  - Temperature at 2m (T2M)  
  - Wind Speed (WS10), Wind Direction (WD10)  
  - Surface Pressure (PS)  
  - Boundary Layer Height (BLH)  
  - Relative Humidity (RH)  
  - Cloud Cover (CC)  
  - Precipitation

- **Remote Sensing:**  
  - Aerosol Optical Depth (AOD) from MERRA-2

- **Geospatial:**  
  - Latitude, Longitude

---

## Methodology

1. **Data Preprocessing**
   - Data cleaning, temporal and spatial alignment
   - Merging datasets on common timestamps and grid coordinates

2. **Feature Engineering**
   - Extraction of meaningful meteorological patterns
   - Normalization/standardization of features

3. **Modeling**
   - Supervised regression models trained on historical data:
     - **Random Forest** (best performance)
     - AdaBoost
     - Gradient Boosting
     - **XGBoost** (good performance+ fast : with tuned hyper parameters gave better results than RF)
     - LightGBM
     - CatBoost

4. **Evaluation Metrics**
   - Mean Absolute Error (MAE)
   - Root Mean Squared Error (RMSE)
   - Coefficient of Determination (R²)

5. **Analysis**
   - Comparison of model performances
   - Estimation of emission-related vs meteorology-related contributions
   - SHAP was used to visualize key feature impacts on PM2.5 predictions

---

## Key Findings and Results

- **XG Boost** outperformed Random Forest after tuning in estimating PM2.5.
- | Metric | Score |
|--------|-------|
| **MSE** | 523.73 |
| **RMSE** | 22.88 |
| **R²** | 0.8634 |
- **Meteorology alone** explains a substantial portion of PM2.5 variability.
- A **PM2.5 heatmap** was generated across India using model predictions to visualize spatial pollution patterns
- The methodology enables policymakers to **assess the impact of emission control measures** independently of weather effects.


