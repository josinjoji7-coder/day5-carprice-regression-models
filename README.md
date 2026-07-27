# CarDekho Used Car Price Prediction using Machine Learning

## 1. Business Objective

The main objective of this project is to develop a regression model that can accurately predict the selling price of a used car.
This type of prediction can be useful for car sellers to estimate a suitable price for their vehicles and for buyers to understand whether a car is priced fairly based on its features.

## 2. Dataset Overview

Dataset Name: CarDekho Used Car Dataset

The dataset contains information about used cars along with their selling prices. It includes different features related to cars such as brand, model, vehicle age, kilometers driven, fuel type, transmission type, engine, mileage, and other specifications.

After preprocessing, the dataset contained:
- Number of records: 15,411
- Type of problem: Regression
- Target variable: selling_price
- 
## 3. Features and Target Variable

Target Variable:
selling_price

The model predicts the selling price of the used car.
Features Used
Numerical Features:
- vehicle_age
- km_driven
- mileage
- engine
- max_power
- seats
Categorical Features:
- car_name
- brand
- model
- seller_type
- fuel_type
- transmission_type

## 4. Data Preprocessing

Before training the models, the dataset was prepared using the following steps:

- Removed the unnecessary `Unnamed: 0` column because it was only an index column.
- Checked for missing values and duplicate records.
- Used One-Hot Encoding to convert categorical features into numerical format.
- Split the dataset into training and testing data using an 80:20 ratio.
- Applied feature scaling for Linear Regression because it performs better when features have similar ranges.

## 5. Regression Models Implemented

I trained and compared three different regression models:

1. Linear Regression

Linear Regression is a basic regression algorithm that is used to find relationships between input features and the target value.

2. Decision Tree Regressor

Decision Tree Regressor is a tree-based algorithm that can handle non-linear relationships between features.

3. Random Forest Regressor

Random Forest Regressor is an ensemble learning algorithm that combines multiple decision trees to improve prediction accuracy and reduce overfitting.

## 6. Model Performance Comparison

The models were evaluated using the following metrics:

- Mean Absolute Error (MAE)
- Mean Squared Error (MSE)
- Root Mean Squared Error (RMSE)
- R² Score


| Model | MAE | MSE | RMSE | R² Score |
|---|---|---|---|---|
| Linear Regression | 179670.54 | 1.58e+11 | 397974.01 | 0.7896 |
| Decision Tree Regressor | 126287.34 | 9.43e+10 | 307069.02 | 0.8747 |
| Random Forest Regressor | 95647.88 | 4.91e+10 | 221537.82 | 0.9348 |

## 7. Final Model Selection

Based on the evaluation results, **Random Forest Regressor** was selected as the best-performing model.

The reasons for selecting Random Forest are:

- It achieved the highest R² score of 0.9348.
- It had the lowest MAE value 95647.88, which means the prediction errors were lower compared to other models.
- It achieved the lowest RMSE value 221537.82.

## 8. Key Observations

- Random Forest performed better than Linear Regression and Decision Tree models.
- Tree-based models were able to understand the relationship between car features and selling prices better.
- Linear Regression had lower performance because car prices depend on many complex factors and are not completely linear.
- Features such as vehicle age, brand, mileage, engine specifications, and kilometers driven have an impact on car prices.

## 9. Future Improvements

The model performance can be improved further by:

1. Applying hyperparameter tuning techniques like GridSearchCV or RandomizedSearchCV to find the best model parameters.

2. Testing advanced machine learning algorithms such as XGBoost, LightGBM, or Gradient Boosting.

3. Performing more feature engineering to create additional useful features.

4. Using cross-validation techniques for better model evaluation.

