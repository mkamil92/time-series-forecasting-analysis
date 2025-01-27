# Time Series Forecasting: Air Passengers and Weather History

This repository contains an analysis of time series forecasting using two datasets:
1. **Air Passengers Data**: A univariate time series with time and one key performance indicator (KPI) - the number of passengers.
2. **Weather History Data**: A multivariate time series with time, a KPI (e.g., temperature), and additional variables like humidity, wind speed, etc.

The goal of this project is to apply and compare various forecasting models on these datasets to evaluate their performance and effectiveness in predicting future values.

---

## Datasets Used

### 1. Air Passengers Dataset
- **Description**: Monthly total of international airline passengers from 1949 to 1960.
- **Columns**:
  - **Time**: Monthly timestamps.
  - **Passengers**: Total number of passengers.

### 2. Weather History Dataset
- **Description**: Hourly weather data containing temperature, humidity, wind speed, and other variables over a specific period.
- **Columns**:
  - **Time**: Hourly timestamps.
  - **Temperature**: Primary KPI (in °C or °F).
  - **Humidity**: Relative humidity as a percentage.
  - **Wind Speed**: Speed of the wind 
  - Other weather-related features.

---

## Methods and Models Applied

### 1. Exponential Smoothing
- A simple yet powerful technique to capture trends and seasonality in time series data.
- Applied to both datasets to generate smoothed forecasts.

### 2. AR (Autoregressive) Model
- Captures the relationship between an observation and a number of lagged observations (previous time steps).
- Evaluated on both univariate and multivariate time series.

### 3. MA (Moving Average) Model
- Models the error term as a linear combination of past error terms.
- Used to analyze short-term patterns in the data.

### 4. ARIMA (Autoregressive Integrated Moving Average)
- Combines AR, MA, and differencing to make the data stationary.
- Tuned parameters (p, d, q) for both datasets to identify optimal configurations.

### 5. SARIMA (Seasonal ARIMA)
- Extends ARIMA by incorporating seasonal components.
- Captured seasonal trends effectively in datasets with recurring patterns (e.g., monthly passenger counts).

---

## Results and Comparison

### Air Passengers Dataset:
- Models like **SARIMA** outperformed others due to the strong seasonal pattern in the data.
- **Exponential Smoothing** captured trends effectively but lacked precision in forecasting.
- **ARIMA** was well-suited for short-term forecasting.

### Weather History Dataset:
- **ARIMA** and **SARIMA** provided accurate predictions by considering both trends and seasonality.
- **Exponential Smoothing** worked reasonably well for forecasting temperature.
- **AR** and **MA** models performed better when multivariate features were included.

---

   The forecasting results show that ARIMA and SARIMA models perform best for given data. ARIMA captures short-term trends effectively while SARIMA handles both trend and seasonality well. ETS provides stable but limited predictions and both AR and MA models fail to adapt to dynamic patterns, producing static forecasts. 
ARIMA is ideal for capturing trends and SARIMA excels when seasonality is present making them the most reliable choices for weather forecasting.
