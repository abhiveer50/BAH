# PM Concentration Estimation using Gradient Boosting

This project estimates surface-level Particulate Matter (PM) concentrations using satellite-derived Aerosol Optical Depth (AOD) and atmospheric reanalysis data with Gradient Boosting Regressor from Scikit-learn.

## 📌 Objective

To build a machine learning pipeline that predicts PM concentration levels using:
- Satellite AOD data (e.g., INSAT-3D/3DR/3DS)
- Ground-based CPCB data
- Meteorological variables from reanalysis datasets (e.g., MERRA-2)

## 🚀 Features

- Gradient Boosting Regressor for PM prediction  
- Train-test split and evaluation using RMSE and R²  
- Easily extendable to other ensemble models (XGBoost, LightGBM, etc.)  
- Minimal and modular code for rapid experimentation  

## 🛠️ Requirements

Install dependencies using:

```bash
pip install pandas scikit-learn numpy
