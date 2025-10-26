#  Medical Equipment Transport Cost Prediction

This project aims to predict the **transportation cost** of delivering medical equipment to hospitals using machine learning techniques. It involves detailed **data preprocessing**, **feature engineering**, and training multiple regression models to identify the best-performing one based on **Mean Squared Error (MSE)**.

---

## Overview
The dataset contains both **numerical** and **categorical** features, such as equipment specifications, hospital details, and delivery information.  
The objective is to build a model that can generalize well to unseen data and minimize prediction errors on the test set.

---

##  Workflow

### 1. EDA and Preprocessing
- Handled missing values:
  - **Numerical columns** → replaced with median values.  
  - **Categorical columns** → filled with a new category `"Missing"`.  
- Created new derived features:
  - `Equipment_Density = Equipment_Weight / (Equipment_Height * Equipment_Width)`
  - `Equipment_Volume = Equipment_Height * Equipment_Width`
- Applied one-hot encoding for categorical variables.
- Scaled numerical features using **StandardScaler** for better model convergence.

### 2. Model Training
- Trained multiple models:
  - Linear Regression  
  - Lasso Regression  
  - ElasticNet  
  - Random Forest  
  - Gradient Boosting  
  - AdaBoost  
  - XGBoost  
- Used **GridSearchCV** for hyperparameter tuning and **KFold cross-validation** for reliable performance estimation.

### 3. Evaluation
- Compared models based on **Mean Squared Error (MSE)** and **R² score**.
- Generated predictions for the Kaggle test data using the best model.

---

## Files

| File Name | Description |
|------------|-------------|
| `train (1).csv` | Used for model training and cross-validation |
| `test.csv` | Used for generating predictions for Kaggle submission |

---

## Results
Among all models, **AdaBoost** achieved the **lowest Mean Squared Error** on the Kaggle test set, demonstrating the best generalization performance.


