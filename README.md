# CarDekho Used Car Price Prediction using Regression Models

## Business Objective

The main objective of this project is to develop a machine learning model that can accurately predict the selling price of used cars based on various features such as vehicle age, kilometers driven, fuel type, transmission type, engine specifications, and other vehicle details.

Accurate price prediction can help:
- Sellers estimate a reasonable selling price.
- Buyers make better purchasing decisions.
- Businesses improve used car pricing strategies.

# Dataset Overview

Dataset Name: CarDekho Used Car Dataset

The dataset contains information about used cars including their specifications, usage details, and selling prices.

Number of records: 15,411

Number of features after preprocessing: 284

The dataset contains both numerical and categorical features.

## Features and Target Variable

Target Variable

| Feature | Description |

| selling_price | The price at which the used car is sold |

Input Features

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

## Data Preprocessing

The following preprocessing techniques were applied:

- Removed the `Unnamed: 0` column as it was only an index column.
- Checked and handled missing values.
- Removed duplicate records.
- Used One-Hot Encoding for categorical variables.
- Split the dataset into training and testing sets using an 80:20 ratio.
- Applied Standard Scaling for Linear Regression.

## Regression Models Implemented

Three regression models were implemented and evaluated:

 1. Linear Regression
- A simple regression algorithm used to model linear relationships between features and target values.

 2. Decision Tree Regressor
- A tree-based model capable of capturing non-linear relationships in data.

 3. Random Forest Regressor
- An ensemble learning method that combines multiple decision trees to improve accuracy and reduce overfitting.

Model Performance Comparison

| Model | MAE | MSE | RMSE | R² Score |

| Linear Regression | 179670.54 | 1.58 × 10¹¹ | 397974.01 | 0.7896 |
| Decision Tree Regressor | 126287.34 | 9.43 × 10¹⁰ | 307069.02 | 0.8747 |
| Random Forest Regressor | 95647.88 | 4.91 × 10¹⁰ | 221537.82 | 0.9348 |


## Best Performing Model

Random Forest Regressor

Based on the evaluation results, **Random Forest Regressor** was selected as the best-performing model.

Justification:

- Achieved the highest R² score of **0.9348**, meaning it explains approximately 93.48% of the variation in selling prices.
- Obtained the lowest MAE value (**95,647.88**), indicating lower average prediction errors.
- Achieved the lowest RMSE value (**221,537.82**), showing better performance in handling large prediction errors.

Random Forest performed better because it can capture complex relationships between car features and prices by combining multiple decision trees.


## Key Observations

- Random Forest significantly outperformed Linear Regression and Decision Tree models.
- Tree-based algorithms performed better because used car prices depend on complex relationships between multiple features.
- Vehicle characteristics such as age, mileage, engine specifications, and brand information strongly influence selling prices.
- Linear Regression showed lower performance because it assumes a linear relationship between input features and target price.
- One-Hot Encoding helped convert categorical vehicle information into a format suitable for machine learning models.

---

##  Future Improvements

The model performance can be improved further by:

1. Hyperparameter Optimization
   - Use GridSearchCV or RandomizedSearchCV to find the optimal parameters for Random Forest and other models.

2. Testing Advanced Algorithms
   - Experiment with advanced regression algorithms such as:
     - XGBoost
     - LightGBM
     - Gradient Boosting Regressor

3. Improved Feature Engineering
   - Create additional features based on car specifications.
   - Analyze feature importance and remove less useful features.

4. Outlier Detection
   - Identify and handle extreme values in numerical features to improve prediction accuracy.

5. Cross Validation
   - Use cross-validation techniques for more reliable model evaluation.
