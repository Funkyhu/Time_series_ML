# Time_series_ML
Analysis and prediction of time-series data of temperature and heating demand

# Corresponding Presentation
https://docs.google.com/presentation/d/1eMNVJstHoVfn2XtqSaIOQUNjUOtHGVVfSz-riOgJmCM/edit?usp=sharing

# Content
- EDA Notebook: eda.ipynb + Project_Notebook_EDA.IPYNB
- LSTM Notebook: Project_Notebook_LSTM.IPYNB + Project_Notebook_LSTM_Attention.IPYNB
- Prophet + SARIMAX Notebook: ALLExperiments.ipynb
  
# Data
1. when2heat_DE (column: DE_heat_demand_total): 
    - Type: int
    - Description: Heat demand in Germany in MW for space and water heating

2. weather data
     - from 2004 to 2022
     - hourly data
     - two values per timestamp: TT_TU & RF_TU

# Goal
Predict heating demand.
-> with this information local electricity provider can better stabilise their grid.
-> with more heatpumps used, heating demand will be more important for electricity grid than ever

### Forecast Horizon: 48 hours
### Input sequence length of 14days*24hours and 30days*24hours

### Loss:
Mean Squared Error on MinMax scaled data range 0 - 1

# Models

### Univariate Models
Only use heating demand as input data:
- SARIMAX
- LSTM

### Multivariate Models
- Prophet (+ Holidays)
- Prophet (+ Holidays + Temperature)


## Model Comparison
Always compare 2day forecast-horizon and use mean of all predictions done in 2014.
Use Min-Max Scaler(0,1).

| Model Name        | Hyperparameter     | Additional features | MSE         |
|-------------------|--------------------|---------------------|-------------|
| SARIMAX           | SARIMAX_v1         | nothing added       | 0.000869    |
| Prophet           | Default-Values     | holidays            | 0.007121    |
| Prophet           | prophet_v1         | holidays            | 0.0029120   |
| Prophet_with_temp | prophet_v2         | holidays, temp      | 0.0025222   |
| LSTM   8 units    | lr=1e-2/Restart    | N/A                 | 0.001879228 |

### Hyperparameter
To decide on the Hyperparameters mentioned in the below tables a gridsearch was executed. See the grid search in the AllExperiments.ipynb notebook.

SARIMAX_v1:
|order | seasonal_order |
|--|--|
|(1, 0, 1) | (1, 1, 1, 24) |

prophet_v1:
|holidays_bool| weekly_seasonality| daily_seasonality_bool| changepoint_prior_scale| holidays_prior_scale| daily_fourier|
|-------|-----|---|----|-----|----|
|True|           50|                 False|                  0.3|                    0.3|                    5|

prophet_v2: 
|holidays_bool| daily_seas| daily_seasonality_bool| changepoint_prior_scale| holidays_prior_scale| daily_fourier|
|-------|-----|---|----|-----|----|
|True|         10|         False|                      0.3|                    0.1|                        5|
