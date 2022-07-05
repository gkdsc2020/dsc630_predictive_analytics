# Wlamart Sales Forecasting

**What is Sales Forecasting** - It is the process of using a company’s sales records over the past few years to predict the short-term or long-term sales performance of the company in the future. 
**Why is Sales Forecasting Required** – Sales Forecasting is one of the pillars of proper financial planning. It is a globally conducted corporate practice where number of objectives are identified, action-plans are chalked out as well as budgets and resources are allotted to them to improve sales. With an accurate sales forecast in hand, companies can plan wisely and if the varying factors are not predicted correctly, then there could be staffing issues at stores, financial implications, and the business could become obsolete.
**Who and how would it benefit** - Business Sales Executives often find themselves scrambling for answers when it comes to sales forecasting during business reviews with their leaderships team. The Sales Forecasting will help sales executives to find such answers upfront and be ready with numbers and predictions to share with leaderships team. 
With help of sales forecasting, the individual stores can upscale their customer satisfaction by stocking the right products at right time and decrease overstocking and wastage of food products.
**How to solve this problem** – The sales forecast can be predicted by building the predictive model using statistical algorithms and machine learning techniques and such techniques are used to identify the likelihood of future outcomes based on historical data. The Sales Forecast Model that learns from the past sales records, events, demographic details, and predict the accurate sales so company is ready to source appropriate resources before the actual event happens.
**Explanation of Solution** – To build the sales forecast model, historical data from 45 Walmart stores located in different regions are collected for past 3 years (2010 to 2012). The gathered for this were having store ids, department ids, weekly sales, and date, the week was having any holidays, average temperature in that region, fuel price, unemployment rate and consumer price index etc. The exploratory analysis was performed to understand what are the factors that influence weekly sales and would help predict sales values. With the help of analysis, we figured out that stores type A is having highest median weekly sales than other stores, the thanksgiving week and Christmas weeks were having highest weekly sales for all three years, the median weekly sales for holiday weeks and non-holiday weeks are almost same but max weekly sales during holidays are quite higher than non-holiday weeks. Also performed correlation test to understand what the factors are those strongly correlated with sales value and departments and store size are the top ones. This analysis also helped to remove unwanted features that would not contribute sales prediction.
To build the model, several machine learning algorithms are used. The ML regressors are used to predict the continuous values based on multiple predictor variables, here weekly sales value is predicted using predictor variables such as store, department, size, temperature, isHoliday etc. 
These different models are then tested with test data and evaluated the model’s accuracy and the model which have best accuracy which is 97.7% and least errors are baselined as Sales Forecast Model. 
How would model benefit – The baselined model which produced best accuracy score can be used to predict the sales forecast for any given store and its departments. The model can be deployed to production system and simple application can be built to predict sales. 
The Application would accept values such store number, department number, week of the year, size of the store, is holiday in the week, average temperature, unemployment rate in that week, fuel price etc. and based on these values it would predict the sales value for that store and departments.

**METHODS**: 
The goal of the project is to predict Sales value based on different features, here we used Walmart sales records from different stores for different year. To understand the factors impacting Sales Value we followed different methodologies such as understanding the features correlating with sales value, machine learning algorithms to understand what percentage of features account for sale value and Time Series forecasting. We have explained below each of the methods used to achieve the result in detail.
Feature Correlations:
To understand the features driving the sales value, we should understand first are there any correlation with features and target variable, here target variable is Sales Value. Each feature from the data is compared with Sales value using different visualizations such as bar chart, line chart and heat maps chart and evaluated for any potential impact if sales value. Also created and visualized correlation matrix of all the key features to see correlation among them and with the target value. The higher correlation coefficient value signifies stronger correlation.


**ML Algorithms:**
There are several machine learning algorithms that can be used to predict the value based on historical data. These ML algorithms are used to train the model and evaluated using Weighted mean absolute error. The model with lowest RMSE score and best accuracy score is baselined. Following are the list of ML algorithms are used to train the model – 
•	KNN Regression	
•	Decision Tree
•	Random Forest
•	Gradient Boosting Machine
•	ARIMA - Auto Regressive Integrated Moving Average

**Time Series Forecasting**:   
The data here we are dealing with is sales history records by date, it is a time series data because it is a series of data points measured at consistent time intervals. We used Auto ARIMA model on this time series to predict the sales values.
Brief about ARIMA model – it is a very popular statistical method for time series forecasting. ARIMA stands for Auto-Regressive Integrated Moving Averages. ARIMA models work on the following assumptions –
•	The data series is stationary, which means that the mean and variance should not vary with time. A series can be made stationary by using log transformation or differencing the series.
•	The data provided as input must be a univariate series, since arima uses the past values to predict the future values.


