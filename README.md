# Precipitation Data Imputation

This repository contains Python code for imputing missing precipitation data using two machine learning techniques: **Linear Regression** and **HistGradientBoostingRegressor**. The project uses meteorological data, including precipitation values from multiple weather stations, and leverages spatial relationships between stations for accurate data imputation.

## Techniques Used

1. **Linear Regression**:
   - Linear regression models are trained on precipitation data from nearby stations to predict missing values based on the correlation between stations.
   
2. **HistGradientBoostingRegressor**:
   - A powerful gradient boosting algorithm that is used to impute missing precipitation data by fitting the model to nearby station data, optimizing for regression tasks using **cross-validation**.

## Features

- **Data Preprocessing**: Loads and processes precipitation data, with stations as columns and dates as the index.
- **Spatial Analysis**: Calculates Euclidean distances between stations to group them by proximity and use nearby stations for imputation.
- **Model Evaluation**: Evaluates model performance with metrics like **R²**, **MSE**, **RMSE**, and **MAE**.
- **Cross-Validation**: Implements cross-validation to assess model performance on imputed data.
- **Distance-based Grouping**: Dynamically groups stations by their distance to create more accurate imputation models.

## Files

- `linear_regression_imputation.py`: Implements the linear regression-based imputation model.
- `histgradientboosting_imputation.py`: Implements the HistGradientBoostingRegressor-based imputation model.
