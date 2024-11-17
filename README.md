# Imputation of Missing Monthly Precipitation Data Using Linear Regression: A Comprehensive Case Study of Lake Urmia Basin's Stations Based on Proximity, Data Coverage, and Correlation

This script is designed to impute missing precipitation data for weather stations using a machine learning approach based on linear regression. The primary goal is to fill missing values in the precipitation records by leveraging data from **geographically** and **statistically** similar stations.

### Methodology:
1. **Data Preparation:** 
   - The precipitation dataset is filtered for a 30-year period, with data from the Solar Hijri (Solar) calendar, where `136801` represents the first month of the year 1368 in the Solar calendar.
   - Stations with missing precipitation data are identified for imputation.

2. **Distance Calculation:** 
   - The Euclidean distance between stations is computed based on their UTM coordinates (latitude and longitude), and these distances are ranked for proximity.

3. **Imputation Using Linear Regression:** 
   - For each station with missing data, the script searches for the nearest station with data available for the same dates.
   - Linear regression models are trained using data from the nearest station to predict the missing precipitation values.
   
4. **Model Evaluation:** 
   - The performance of the imputation model is evaluated using R², RMSE, and MAE metrics, and the linear regression equation is computed for each station.

5. **Results:** 
   - The imputation results, including performance metrics and regression equations, are saved to a new Excel file for further analysis.

This approach helps fill missing precipitation values efficiently while considering both spatial proximity and statistical similarity, ensuring the imputed data is as accurate as possible.
