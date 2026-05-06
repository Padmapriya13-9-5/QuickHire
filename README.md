This project is a production-style time series forecasting system designed to predict future sales for different states using historical data. It uses multiple machine learning and deep learning models, compares their performance, and automatically selects the best model for forecasting. The final output is served through a REST API.

 **Objective**
Build an end-to-end forecasting pipeline
Train multiple forecasting models
Compare model performance
Select the best model automatically
Forecast sales for next 8 weeks (56 days)
Deploy predictions using REST API

 **Dataset Description**
The dataset contains historical sales data
Main columns:
Date
State
Sales
Data is used to identify trend and seasonality

**Tools Used**
Python, Pandas, NumPy, Scikit-learn, XGBoost, Prophet, TensorFlow, FastAPI

 **Methodology**
1. Data Preprocessing
Converted date column to datetime format
Standardized column names
Handled missing values using forward fill
Sorted data by state and date
2. Feature Engineering
Lag features created:
lag1 (previous day)
lag7 (weekly pattern)
lag30 (monthly pattern)
Rolling features:
7-day rolling mean
Time-based features:
Day
Month
Day of week
3. Models Used
ARIMA (Statistical model)
Prophet (Trend + seasonality model)
XGBoost (Machine learning model)
LSTM (Deep learning model)
4. Model Evaluation
Models evaluated using:
MAE (Mean Absolute Error)
RMSE (Root Mean Squared Error)
MAPE (Mean Absolute Percentage Error)
Best model selected based on lowest error
5. Forecasting Process
Data split into train and test sets
Models trained per state
Performance compared
Best model selected automatically
Forecast generated for next 56 days

 **API Development**
1. Endpoint
GET /forecast/{state}
2. Example Requests
/forecast/Tamil Nadu
/forecast/Kerala
/forecast/Karnataka
3. Response Format
{
  "state": "Tamil Nadu",
  "forecast": [120.5, 130.2, 140.8]
}
 **Tech Stack**
Python
Pandas, NumPy
Scikit-learn
XGBoost
Prophet
TensorFlow / Keras
Statsmodels
FastAPI
Uvicorn

**Project Structure**
main.py → FastAPI backend
train.py → Model training & forecasting
utils.py → Feature engineering
data.xlsx → Dataset
forecast.json → Final predictions
requirements.txt → Dependencies
README.md → Documentation

 **Results**
Multiple forecasting models implemented
Best model selected automatically per state
Accurate 8-week sales forecasting achieved
REST API successfully deployed

 **Key Features**
End-to-end ML pipeline
Multi-model comparison
Automatic best model selection
Time series feature engineering
REST API integration
Production-ready structure

 **Conclusion**
This project demonstrates a complete real-world machine learning workflow
It includes data preprocessing, model building, evaluation, and deployment
It simulates an industrial forecasting system used in business applications
