# customer-churn-prediction
End-to-end customer churn prediction project using Python, sql, and ML
# Churn Prediction System

## Project Overview
Brief description of the project.

## Day 1: Project Setup
- Repository initialized
- Folder structure created
- Dataset added
- Initial README created

## Day 2: Data Exploration and Understanding
### Objective
The goal of Day 2 was to explore and understand the dataset before applying any preprocessing or machine learning models. This step ensures data quality, identifies the target variable, and highlights potential issues early.

### Dataset Overview
- Total records: 7,043 customers
- Total features: 21 columns
- Target variable: `Churn`

### Target Variable Analysis
- The `Churn` column is categorical (`Yes` / `No`) with no missing values.
- Churn distribution:
  - No: ~5,000 customers (~70%)
  - Yes: ~2,000 customers (~30%)
- The dataset is moderately imbalanced, which will be considered during model evaluation using metrics such as Recall, F1-score, and ROC-AUC instead of accuracy alone.

### Missing Values
- No missing values were found across any columns in the dataset.
- This indicates high data quality and removes the need for imputation.

### Feature Analysis
- Binary categorical features: `gender`, `Partner`, `Dependents`, `PhoneService`, `PaperlessBilling`
- Multi-class categorical features: `MultipleLines`, `InternetService`, `OnlineSecurity`, `OnlineBackup`, `DeviceProtection`, `TechSupport`, `StreamingTV`, `StreamingMovies`, `Contract`, `PaymentMethod`
- Identifier column: `customerID` (unique for every record, will be removed before modeling)
- Numeric features include `MonthlyCharges` and `tenure`
- The `TotalCharges` column is stored as an object despite representing numeric values and will be converted during preprocessing

### Key Observations
- The dataset is clean with no missing values
- The target variable is moderately imbalanced
- Several categorical features require encoding
- One identifier column (`customerID`) has no predictive value
