# Time-Series-Analysis-of-UK-air-pollution 🏭
Time Series Analysis and forecasting of Nitrogen dioxide levels in the atmosphere  involving a spatial analysis of Hillington and Greenwich. An examination is also done to find the impact of weather parameters on Nitrogen dioxide levels.





## Aim 🔍
The primary aim of this project is to utilize time series analysis to gain deeper insights into the dynamics of nitrogen dioxide (NO2) air pollution in the UK, specifically focusing on the areas of Greenwich and Hillington. The study aims to analyze the trends, seasonal patterns, and the impact of weather parameters on NO2 levels to develop effective strategies for improving air quality.

## Objectives 🎯
1. **Analyze Historical NO2 Data**: Examine the historical NO2 levels in Greenwich and Hillington to identify trends, seasonal patterns, and anomalies.
2. **Model NO2 Levels**: Apply time series models, including SARIMA, VAR, and VECM, to forecast future NO2 levels and understand the impact of weather parameters.
3. **Spatial Analysis**: Conduct spatial analysis to explore the geographical distribution of NO2 within Greenwich and Hillington.
4. **Impact of Weather Parameters**: Investigate the influence of various weather parameters on NO2 levels using multivariate time series models.
5. **Develop Forecasting Models**: Create accurate forecasting models to predict future NO2 levels and provide insights for policy-making and air quality management.

## Libraries and Packages Used 📦

- **Python Libraries**:
  - `pandas`: For data manipulation and analysis.
  - `numpy`: For numerical computations.
  - `matplotlib`: For data visualization.
  - `seaborn`: For statistical data visualization.
  - `statsmodels`: For statistical modeling and time series analysis.
  - `scipy`: For scientific computations.
  - `sklearn`: For machine learning and statistical modeling.
  - `itertools`: For creating iterators for efficient looping.

## Data Sets and Sources 📊

### NO2 Levels Data
- **Source**: Department for Environment, Food & Rural Affairs
- **Description**: Daily monitored levels of NO2 in Greenwich and Hillington from 2014 to 2024.
- **Link**: Department for Environment, Food & Rural Affairs

### Weather Data
- **Source**: Visual Crossing Weather
- **Description**: Historical weather data for Greenwich from 2014 to 2024.
- **Link**: Visual Crossing Weather

## Exploratory Data Analysis (EDA) 🧹

### Data Cleaning
- Removed columns with non-significant data.
- Handled missing values and 'No data' entries.
- Converted date columns to datetime format.
- Calculated mean monthly NO2 levels for better trend analysis.

### Descriptive Statistics
- Calculated summary statistics for NO2 levels in Greenwich and Hillington.
- Plotted time series graphs to visualize daily and monthly NO2 levels.

### Stationarity Analysis
- Conducted Augmented Dickey-Fuller (ADF) test to check for stationarity.
- Applied differencing techniques to achieve stationarity.

### Seasonal and Trend Decomposition
- Used STL decomposition to separate the time series into seasonal, trend, and residual components.

## Methodology 📈

### Stationarity Analysis
- **Augmented Dickey-Fuller Test**: Used to test for unit roots and stationarity.
- **STL Decomposition**: Applied to decompose the time series into seasonal, trend, and residual components.
- **Differencing**: Normal and seasonal differencing applied to achieve stationarity.

### Univariate Time Series Models
- **SARIMA Model**: Seasonal AutoRegressive Integrated Moving Average model used for forecasting NO2 levels.
  - Parameter selection based on ACF and PACF plots.
  - Hyperparameter tuning using AIC, BIC, RMSE, and MAPE.

### Multivariate Time Series Models
- **Vector Autoregression (VAR) Model**: Used to analyze the impact of weather parameters on NO2 levels.
  - Optimal lag selection based on AIC.
  - Granger-causality test to determine predictive relationships.
  - Impulse Response Function (IRF) to assess the impact of shocks.

- **Vector Error Correction Model (VECM)**: Applied to cointegrated variables to analyze long-term relationships.
  - Engle-Granger test for cointegration.
  - Ljung-Box test for autocorrelation in residuals.

## Implementation Steps ✅

1. **Data Collection**: Gathered NO2 and weather data from respective sources.
2. **Data Cleaning**: Processed and cleaned the data to remove inconsistencies and missing values.
3. **EDA**: Conducted exploratory data analysis to understand data distribution and trends.
4. **Stationarity Analysis**: Performed ADF test and differencing to achieve stationarity.
5. **Modeling**:
   - Applied SARIMA model for univariate time series analysis.
   - Implemented VAR model to study the impact of weather parameters.
   - Used VECM for analyzing long-term relationships between NO2 and weather parameters.
6. **Forecasting**: Generated forecasts for NO2 levels using the best-fit models.
7. **Validation**: Validated the models using RMSE, MAPE, and other statistical metrics.

## Results 🔑

### Univariate Analysis
- **SARIMA Model**:
  - Best model for Greenwich: SARIMA(1, 1, 1)(1, 1, 1, 12)
  - Best model for Hillington: SARIMA(5, 1, 1)(2, 2, 2, 12)
  - Forecasted NO2 levels show a general decline, with Hillington having higher levels than Greenwich.

### Multivariate Analysis
- **VAR Model**:
  - Humidity showed a significant short-term impact on NO2 levels.
  - Other weather parameters had minimal and transient effects.

- **VECM Model**:
  - No long-term equilibrium relationship found between NO2 levels and weather parameters like temperature and sea level pressure.

## Conclusion 🏆

The study reveals a significant decline in NO2 levels in both Greenwich and Hillington, particularly after 2019, likely due to the COVID-19 lockdowns. The SARIMA model effectively forecasts future NO2 levels, indicating continued improvement in air quality. While humidity impacts NO2 levels in the short term, no long-term relationship with weather parameters was found. These findings can inform policy-making and targeted interventions to further reduce air pollution.

## Future Scope 🤔

- **Policy Implementation**: Support for Ultra Low Emission Vehicles (ULEVs) and Clean Air Zones (CAZs).
- **Public Transport and Infrastructure**: Investments in low-carbon buses and cycling infrastructure.
- **Further Research**: Explore additional weather parameters and their impact on air quality.


