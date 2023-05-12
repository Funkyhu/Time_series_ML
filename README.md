# Time_series_ML
Analysis and prediction of time-series data of temperature and heating demand


# Data
1. when2heat_DE (column: DE_heat_demand_total): 
    - Type: number
    - Description: Heat demand in Germany in MW for space and water heating

2. weather data??


# Goal
Predict heating demand.
-> with this information local electricity provider can better stabilise their grid.
-> with more heatpumps used, heating demand will be more important for electricity grid than ever

### Forecast Horizon: 
???
the smaller the easier: 24 hours, 7 days
-> multiseasonality: daily, weekly, yearly

bigger horizon: 
-> probably need to aggregate hourly data to daily data
-> would lead to less trainig data -> complex models more difficult

### Loss:
Mean Squared Error or Absolute Error?

# Models

### Simple: 
Only use heating demand as input data:
- (S)ARIMA
- MLPerceptron

### Intermediate:
- RNN
- CNN
- LSTM

### Complex:
Also use weather data. Maybe even use weather forecast.
- Prophet -> could integrate holidays, too
- RNN, CNN, LSTM
- Transformers