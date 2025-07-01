# Airbnb-NYC-Listings-Data-Analysis

This project analyzes a dataset of Airbnb listings in NYC to identify popular neighborhoods, busiest hosts, and predict rental prices using various regression models.

Project Goals
Analyze Popular Neighborhoods: Identify the busiest hosts and their top neighborhood groups in terms of listings and price.
Predict Rental Prices: Build and compare regression models to predict Airbnb rental prices.
Data Analysis and Key Findings
The dataset contains information about Airbnb listings in NYC, including details about the host, location, room type, price, and availability.
Data Cleaning: Missing values in 'name', 'host_name', and 'reviews_per_month' were handled, and the 'last_review' column was dropped due to a large number of missing values.
Outlier Treatment: Extreme values in numerical columns such as 'price', 'minimum_nights', 'number_of_reviews', 'reviews_per_month', 'calculated_host_listings_count', and 'availability_365' were capped using the Interquartile Range (IQR) method.
Busiest Host: The host with the most listings is "Sonder (NYC)" with 327 listings, primarily in Manhattan.
Popular Neighborhoods: Manhattan and Brooklyn have the highest number of listings, which correlates with higher rental prices in Manhattan, likely due to its popularity as a tourist destination.
Price Prediction
The project explored several regression models to predict the price of Airbnb listings:

Linear Regression: A baseline model was trained, and its performance was evaluated using cross-validation with different numbers of folds (k=3, 5, and 10).
Other Regression Models: Support Vector Regressor (SVR), Random Forest Regressor, and Gradient Boosting Regressor were trained and compared.
Model Performance Comparison (Mean Squared Error - MSE)
Random Forest Regressor: MSE: 2964.89, RMSE: 54.45
Gradient Boosting Regressor: MSE: 3098.93, RMSE: 55.67
Support Vector Regressor: MSE: 7287.29, RMSE: 85.37
Conclusion
The Random Forest Regressor performed best among the evaluated models, achieving the lowest MSE and RMSE. This suggests that tree-based ensemble methods are well-suited for this price prediction task. Further improvements could potentially be made by hyperparameter tuning the Random Forest model.

Files
AB_NYC_2019.csv: The dataset used for this analysis.
This Notebook: Contains the code for data loading, analysis, visualization, and model training/evaluation.
