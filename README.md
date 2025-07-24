# Modelling Above-Ground Biomass Using Remote Sensing and Machine Learning 
## Overview
This project focuses on estimating and predicting above-ground biomass (AGB) over India and Sri Lanka using remote sensing data from Google Earth Engine (GEE) and machine learning (XGBoost). The analysis begins in 2010, the only latest year biomass ground-truth data is available from NASA/ORNL, and applies the trained model to predict biomass for a later year (2015).

## Objectives
1. Estimate biomass using vegetation and climate variables derived from satellite imagery.
2. Train a machine learning regression model to capture the relationship between predictors and biomass.
3. Use the model to predict biomass for future using newly derived environmental features.
4. Visualize and compare observed and predicted biomass spatially.

### Actual Biomass (2010) vs Predicted Biomass (2010) 
<img width="998" height="526" alt="image" src="https://github.com/user-attachments/assets/24019294-05ec-4877-82a3-ac93769bc133" /> 

### Predicted Biomass (2015)
<img width="553" height="455" alt="image" src="https://github.com/user-attachments/assets/c809cbfe-5158-4bf3-a783-bedac8085051" />


## Data Sources
| Dataset                               | Description                            | Provider |
| ------------------------------------- | -------------------------------------- | -------- |
| `NASA/ORNL/biomass_carbon_density/v1` | Above-ground biomass (AGB) for 2010    | NASA     |
| `MODIS/061/MOD13A2`                   | NDVI and EVI (vegetation indices)      | MODIS    |
| `MODIS/061/MOD15A2H`                  | LAI and FPAR (vegetation productivity) | MODIS    |
| `MODIS/061/MYD11A2`                   | Land Surface Temperature (LST Day)     | MODIS    |
| `NASA/GPM_L3/IMERG_MONTHLY_V07`       | Monthly precipitation totals           | NASA GPM |
| `MODIS/061/MCD12Q1`                   | Land cover classification (LC\_Type1)  | MODIS    |



## Model Performance
- Root Mean Square Error (RMSE): 7.16
- R² Score: 0.85

The high R² value and relatively low RMSE indicate that the model is well-suited for estimating biomass using satellite-derived environmental predictors. It successfully captures the underlying patterns in the data, making it a reliable tool for predicting biomass in similar contexts and future time periods.

## Notes
- The model is trained using only 2010 as biomass data is not available for other latest years.
- The 2015 prediction depends solely on model generalization and quality of MODIS/GPM-derived inputs.
- Spatial resolution and interpretation depend on MODIS data resolution (~500m–1km).




