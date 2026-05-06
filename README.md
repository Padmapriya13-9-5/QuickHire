TThis project is an end-to-end time series forecasting system designed to predict future sales based on historical data. The system begins with data preprocessing, where missing dates and values are handled to ensure data consistency. Feature engineering is performed by creating lag features, rolling statistics, and date-based features such as day of the week and month to capture temporal patterns.

Multiple forecasting models are implemented, including ARIMA, Prophet, XGBoost, and LSTM. Each model is trained on the processed dataset and evaluated using Mean Absolute Error (MAE) to measure prediction accuracy. The system automatically compares the performance of these models and selects the best-performing model for forecasting.

The final model is used to generate predictions for the next eight weeks of sales, capturing both trend and seasonality in the data. To make the system practical and production-ready, the trained model is deployed using FastAPI, which exposes the predictions through a REST API endpoint.

This project is structured like a real backend service with modular components, making it scalable, reusable, and easy to maintain. It demonstrates the complete machine learning lifecycle from data preparation to deployment.

Tools Used

Python, Pandas, NumPy, Scikit-learn, XGBoost, Prophet, TensorFlow, FastAPI
