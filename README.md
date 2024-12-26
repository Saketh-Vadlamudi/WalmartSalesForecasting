# Walmart Sales Prediction using SARIMAX

This project focuses on predicting the weekly sales of different Walmart stores using SARIMAX (Seasonal AutoRegressive Integrated Moving Average with eXogenous factors). The model uses historical sales data from Walmart's stores to make predictions and evaluate the performance of the forecasting model.

## Overview

The dataset contains sales data from various Walmart stores, and the goal is to forecast future sales for a specific store. The project involves time series analysis, decomposition, SARIMAX modeling, and performance evaluation using metrics like Mean Squared Error (MSE) and Root Mean Squared Error (RMSE).

## Steps Involved

1. **Data Loading**:
   - Data is loaded from the `Walmart DataSet.csv` file, which contains weekly sales data for various Walmart stores.
   
2. **Data Preprocessing**:
   - The dataset is filtered to focus on a specific store.
   - The `Date` column is converted to a datetime type and set as the index for time series analysis.
   
3. **Time Series Decomposition**:
   - The time series data is decomposed into trend, seasonal, and residual components using `seasonal_decompose` from `statsmodels`.
   
4. **SARIMAX Model**:
   - A SARIMAX model is fitted to the data to forecast future sales.
   - Hyperparameters `p`, `d`, and `q` are optimized to find the best model for the sales data.
   
5. **Forecasting**:
   - The model is used to make one-step-ahead and dynamic forecasts.
   - Confidence intervals are plotted for the predicted values.

6. **Model Evaluation**:
   - Mean Squared Error (MSE) and Root Mean Squared Error (RMSE) are calculated to evaluate the model's performance.
   
7. **Residual Analysis**:
   - The residuals are analyzed to check the accuracy of the model's predictions.

## Requirements

- Python 3.x
- pandas
- numpy
- matplotlib
- seaborn
- statsmodels

## Installation

1. Clone the repository:
   ```bash
   git clone https://github.com/Saketh-Vadlamudi/WalmartSalesForecasting.git
   ```
2. Navigate to the project directory:
``` bash
cd WalmartSalesForecasting
```
3. Install the required dependencies:
``` bash
pip install -r requirements.txt
```

## Usage
``` bash
python walmart_Capstone.py
```

Evaluation Metrics
Mean Squared Error (MSE): Measures the average squared difference between the predicted and actual sales.
Root Mean Squared Error (RMSE): Provides the square root of the MSE, which gives an idea of the magnitude of error in the predictions.
Example Output
The output will show the predicted weekly sales for the selected store, along with a confidence interval, and evaluation metrics like MSE and RMSE.

Conclusion
This project demonstrates how SARIMAX can be used for sales forecasting, which can help businesses like Walmart plan inventory and optimize operations. The model can be further improved by tuning hyperparameters or incorporating additional external factors.

Acknowledgements
The dataset is provided by Walmart for the purpose of sales forecasting.
Special thanks to the statsmodels library for providing powerful tools for time series analysis.
