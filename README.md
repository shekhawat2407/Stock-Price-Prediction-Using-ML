# Stock-Price-Prediction-Using-ML

## Objective 

The objective of the project is to predict stock price returns in financial markets based on the  application of machine learning models.
Part I of the project caters to the evaluation of model performance on 10 sampled stocks. While  Part II evaluates the model performance on a larger sample (current S&P stocks used as a  reference)


### Libraries Used:
1. Basic data loading/storing/manipulation libraries
- pandas, numpy,datetime, pandas_datareader ,sklearn.preprocessing 
2. Plotting Library
- seaborn
3. Web scrapping S&P data
- bs4, requests, pickle
4.For feature creation & testing: 
- statsmodels.stats.outliers_influence, ta.momentum 
5. For implementing the models used 
sklearn.linear_model, sklearn.metrics, sklearn.model_selection, sklearn.neighbors 

 
Functions Used: 
1.Function for fetching the S&P ticker lists (used as large Universe)
- save_sp500_tickers()
2.Functions for Stock Data Loading & Data Wrangling (Filling, Scaling, Binary Return Conversion)
- load_stock_data(ticker),scale_data(dataframe),calculate_binary_returns(ticker_data)
3. Functions for creating the dataset for explanatory variables (Both fundamental & Technical Indicators)
- create_macro_feature_data(), technical_indicators(ticker_data), check_multicollinearity(feature_data)
4. Functions for Model Predictions & Evaluation Metrics
- KNN (X_train, X_test, y_train, y_test,params,tuning), LR (X_train, X_test, y_train, y_test,params,tuning)
5. Functions for Hyperparameter Tuning
- knn_hyper_parameter_tuning(X_train,y_train), lr_hyper_parameter_tuning(X_train,y_train)
6. Main Function to generate the output dataframe
- generate_output (ticker_list,feature_data_scaled,tuning)
