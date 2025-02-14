# PriceProphet-House-Price-Prediction


Project Overview

This project aims to predict house prices using Linear Regression and Gradient Boosting Regressor models. The dataset used is the King County House Sales dataset. The analysis involves feature engineering, data visualization, model evaluation, and dimensionality reduction using PCA (Principal Component Analysis).

Dataset

The dataset includes various features such as:

Number of bedrooms

Square footage of living area

Year built

Renovation year

Location details

Price (target variable)

Libraries Used

numpy

pandas

matplotlib

seaborn

sklearn (LinearRegression, GradientBoostingRegressor, StandardScaler, PCA, train_test_split, mean_squared_error)

Key Steps

1. Data Loading

The dataset is read using pandas:

pd.read_csv("kc_house_data.csv")

2. Feature Engineering

House Age: Age of the house.

Recent Renovation: Whether the house was renovated after 2000.

Square Feet per Room: Living area divided by bedrooms (handled division by zero).

Luxury House Flag: Marked houses with more than 4000 sqft as luxury.

Date Conversion: Extracted the year from the date column.

3. Data Visualization

Bedrooms Count Bar Plot

Price vs Square Feet Scatter Plot

Bedrooms vs Price Scatter Plot

4. Data Preprocessing

Dropped id and price from input features.

Target variable is price.

Train-Test Split: 90% training, 10% testing.

5. Models

Linear Regression

A simple linear model assuming a linear relationship between features and price.

Gradient Boosting Regressor

An ensemble learning method that builds multiple decision trees:

n_estimators=400

max_depth=5

learning_rate=0.1

loss='squared_error'

6. Evaluation

R² Score:

Linear Regression: Indicates how well the linear model fits the data.

Gradient Boosting: Typically achieves higher accuracy due to its complexity.

7. Training vs Testing Error Plot

Plots the MSE for each estimator to diagnose overfitting or underfitting.

8. PCA (Principal Component Analysis)

Standardized features.

Reduced dimensionality to 5 components.

Explained variance ratio plotted.

Expected Results

Linear Regression R² ~ 0.7-0.75

Gradient Boosting R² ~ 0.85+ (depending on data and tuning)

Key Takeaways

Step

Purpose

Feature Engineering

Create better features to improve prediction accuracy.

EDA

Visualize relationships between features and price.

Linear Regression

Simple baseline model.

Gradient Boosting

Advanced model; handles complex patterns.

PCA

Reduce features; find the most important patterns.

Training vs Test Error

Check model performance and diagnose overfitting.



Conclusion

This project demonstrates the power of Gradient Boosting in predicting house prices compared to a simple Linear Regression model. Feature engineering and visualization play a crucial role in understanding the data and improving model performance.
