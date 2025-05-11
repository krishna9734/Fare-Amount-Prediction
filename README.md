# Fare-Amount-Prediction

Objective: To develop a machine learning model that accurately estimates taxi fare prices in USD.

Dataset:
Initial size: 200,000 rows, 9 columns (key, fare_amount, pickup_datetime, passenger_count, pickup/dropoff longitudes/latitudes).
Processed size: 193,902 rows, 12 columns (after cleaning and feature engineering).
Target variable: fare_amount (USD).
Data Preprocessing and Feature Engineering:
Converted `pickup_datetime` to datetime format and extracted hour, day, month, year, and day of week.
Calculated `distance_in_kms` using geographical coordinates.
Filtered out invalid data (fare amounts <= 0 or >250, passenger count >= 7, out-of-range coordinates).
Removed unnecessary columns (key, index, pickup_datetime).

Exploratory Data Analysis (EDA):
Visualized relationships between fare_amount and hour, year, passenger_count, distance_in_kms.
Identified peak hours on weekdays and weekends.
Observed distribution of fare_amount and distance_in_kms.
Analyzed correlations between features; found a strong positive correlation between `distance_in_kms` and `fare_amount`.

Data Modeling:
Split data into training (155,120 samples) and testing (38,781 samples) sets.
Implemented and evaluated three regression models:
Linear Regression
Decision Tree Regression
Random Forest Regression

Model Evaluation Metrics:
Root Mean Squared Error (RMSE)
R-squared (R²)
Adjusted R-squared

Conclusion:
The Random Forest model achieved the lowest RMSE (3.531733) and the highest R-squared (0.978859) and Adjusted R-squared (0.978858) values, indicating it performed the best in predicting taxi fare amounts compared to the other models.
Distance is a significant factor affecting fare amount, as shown by the high correlation and model performance.
