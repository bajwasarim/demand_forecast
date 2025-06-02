# Demand Forecasting with Traditional and Machine Learning Models

This notebook explores demand forecasting techniques using two distinct datasets: the NASA Commercial Modular Aero-Propulsion System Simulation (C-MAPSS) dataset (simulated remaining useful life data for turbofan engines, converted to spare parts demand) and the UCI Daily Demand Forecasting Orders dataset.

The notebook covers the following steps:

1.  **Dataset Download and Setup**: Downloading the NASA C-MAPSS dataset using `kagglehub` and the UCI Daily Demand dataset from a URL to a writable directory in the Colab environment. Setting up input and output directories.
2.  **Data Preparation**:
    *   For the NASA C-MAPSS data: Reading and processing the raw text files, calculating Remaining Useful Life (RUL), normalizing sensor and operational setting data, and converting RUL into a simulated spare parts demand time series based on a defined threshold and aggregation window.
    *   For the UCI Daily Demand data: Loading the CSV file, handling potential parsing issues (decimal separators), renaming columns for clarity, converting data types, and splitting the data into training and testing sets.
3.  **Traditional Forecasting Models**: Applying and evaluating traditional time series forecasting methods (Simple Moving Average, Simple Exponential Smoothing, Holt's Exponential Smoothing, ARIMA) and intermittent demand forecasting methods (Croston's, Syntetos-Boylan Approximation (SBA), Teunter-Syntetos-Babai (TSB)) on both the prepared UCI daily demand data and the NASA simulated spare parts demand data.
4.  **Machine Learning Models**: Implementing feature engineering (creating lag features and date-based features) for both datasets and applying various machine learning models (Random Forest, XGBoost, LightGBM, MLP Regressor) to forecast demand.
5.  **Evaluation and Visualization**: Evaluating the performance of all applied models using metrics such as RMSE, MAE, MAPE, Bias, and MASE, and visualizing the actual vs. forecasted demand for each dataset and model type.

This notebook serves as a comparative study demonstrating the application of both traditional statistical and modern machine learning approaches to demand forecasting problems, including those with intermittent characteristics.
