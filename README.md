# Car Price Prediction Project

## Overview
This project aims to build a machine learning model to predict car selling prices based on various features such as manufacturing year, present price, kilometers driven, fuel type, seller type, transmission, and owner count.

## Data Loading and Initial Exploration
The dataset `car data.csv` was loaded into a pandas DataFrame. Initial exploration included checking the shape, information (`.info()`), and null values (`.isnull().sum()`). The dataset contains 301 entries and 9 columns, with no missing values.

## Data Preprocessing
Categorical features such as `Fuel_Type`, `Seller_Type`, and `Transmission` were encoded into numerical representations:
- `Fuel_Type`: Petrol (0), Diesel (1), CNG (2)
- `Seller_Type`: Dealer (0), Individual (1)
- `Transmission`: Manual (0), Automatic (1)

The `Car_Name` column was dropped as it's not directly used for prediction, and `Selling_Price` was designated as the target variable (Y), with the remaining features forming the input (X).

## Model Training and Evaluation
### Model: Linear Regression
The data was split into training and testing sets (90% training, 10% testing) using `train_test_split` with `random_state=2`.
A Linear Regression model was trained on the preprocessed data.

#### Training Data Evaluation:
- **R-squared error**: 0.8799 (indicating a good fit on the training data)

#### Test Data Evaluation:
- **R-squared error**: 0.8366 (indicating good generalization to unseen data)

Visualizations were generated to compare actual vs. predicted prices for both training and test datasets.

## Prediction Example
A sample prediction was made for a car with the following features:
- Year: 2015
- Present Price: 8.12
- Kms Driven: 18796
- Fuel Type: Petrol (0)
- Seller Type: Dealer (0)
- Transmission: Manual (0)
- Owner: 0

The predicted selling price for this car is approximately **5.41 lakhs**.

## Libraries Used
- pandas
- numpy
- matplotlib
- seaborn
- scikit-learn (sklearn)
```
