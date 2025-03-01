# Internship Report: Predictive Modeling

**Prepared by:** Primesh Kumar Patel  
**Internship Organization:** Cognifyz  
**Task:** Predictive Modeling  
**Date:** 25-02-2025  

## Introduction
As part of my internship at Cognifyz, I was assigned the task of building a **predictive model** to estimate the **aggregate rating of a restaurant** based on available features. This report summarizes the steps taken, methodologies used, evaluation of models, and final recommendations.

## Dataset Overview
The dataset contains multiple features related to restaurants, such as:
- **Restaurant Name**: Name of the restaurant
- **City**: Location of the restaurant
- **Cuisines**: Types of cuisines offered
- **Average Cost for Two**: Approximate cost for two people
- **Has Table Booking**: Whether the restaurant offers table reservations
- **Has Online Delivery**: Availability of online ordering
- **Aggregate Rating**: Overall rating given to the restaurant (Target Variable)

## Steps Performed

### 1. Data Preprocessing
- **Dropped Irrelevant Columns**: Removed columns such as `Restaurant Name`, `Address`, `Currency`, which are not useful for prediction.
- **Handled Missing Values**: Rows with missing values were removed to ensure data integrity.
- **Encoded Categorical Variables**: Used **Label Encoding** for categorical features (`Cuisines`, `Has Table Booking`, `Has Online Delivery`, `City`).
- **Feature Selection**: Selected relevant numerical and categorical features for training.
- **Train-Test Split**: Divided the dataset into **80% training** and **20% testing**.

### 2. Model Selection & Training
I trained the following regression models:
- **Linear Regression**: Assumes a linear relationship between input features and ratings.
- **Decision Tree Regressor**: Uses decision rules to predict restaurant ratings.
- **Random Forest Regressor**: An ensemble method that improves accuracy and reduces overfitting.

### 3. Model Evaluation
Each model was evaluated using:
- **Root Mean Squared Error (RMSE)**: Measures prediction error.
- **R² Score**: Indicates how well the model explains rating variations.

#### Results:
| Model               | RMSE (Lower is better) | R² Score (Higher is better) |
|---------------------|----------------------|-------------------|
| **Linear Regression**  | 1.23                   | 0.34              |
| **Decision Tree**      | 0.43                   | 0.92              |
| **Random Forest**      | **0.30**               | **0.96**          |

### 4. Conclusion & Recommendation
- **Random Forest Regressor performed the best**, achieving **lowest RMSE (0.30)** and **highest R² score (0.96)**.
- **Linear Regression was not suitable**, as the relationship between features and ratings is **non-linear**.
- **Decision Tree was a good alternative**, but slightly less robust than Random Forest.

### 5. Future Improvements
- **Hyperparameter Tuning**: Optimizing the Random Forest model further.
- **Feature Engineering**: Creating new features for better predictions.
- **Ensemble Methods**: Trying Gradient Boosting for further improvements.

## Final Recommendation
The **Random Forest Regressor** should be used for predicting restaurant ratings due to its high accuracy and low error. Further fine-tuning can be performed to enhance model performance.
