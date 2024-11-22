# Predicting Used Car Sale Prices

## Overview
The primary objective was to predict car prices based on their characteristics by leveraging advanced data analysis and regression techniques.

---

## Project Details

### Goals
1. **Predict Used Car Prices**: Develop accurate regression models to predict car prices based on the dataset provided.
2. **Explore and Engineer Data**: Perform exploratory data analysis (EDA), clean the data, handle missing values, and engineer new features to enhance model accuracy.
3. **Build and Tune Models**: Fit and optimize machine learning models to produce the best forecast results.

### Dataset
The dataset was provided in two parts:
- **Training Dataset**: Contains 39 features and the target variable (`price`).
- **Testing Dataset**: Contains 38 features without the target variable for prediction.

Key features include:
- **Numeric Features**: Mileage, engine displacement, horsepower, etc.
- **Categorical Features**: Make, model, fuel type, transmission, etc.

---

## Methodology

### Task 1: Problem Description and Initial Data Analysis
1. **Problem Definition**:
   - Forecasting car prices based on vehicle features to support pricing strategies in the automotive industry.
   - **Evaluation Metric**: Mean Squared Error (MSE).
2. **Exploratory Data Analysis**:
   - Analyzed key features and their distributions.
   - Identified correlations between features and the target variable.

### Task 2: Data Cleaning, Missing Observations, and Feature Engineering
- **Data Cleaning**:
  - Converted object columns (e.g., `back_legroom`) to numeric.
  - Removed irrelevant features like `vin`.
- **Handling Missing Values**:
  - Imputed missing values using mean/mode as appropriate.
- **Feature Engineering**:
  - Created new features such as `maximum_torque`, `torque_rpm`, and `no_of_gears`.
  - Mapped high-cardinality categorical variables to the top 5 categories + "Other".
  - Encoded categorical variables using one-hot encoding and label encoding.

### Task 3: Forecasting Models
- Built and tuned the following models:
  1. **XGBoost Regressor**:
     - Used GridSearchCV for hyperparameter tuning.
     - Achieved the best performance with RMSE = 1,360.33.
  2. **Lasso Regression**:
     - Explored feature selection and regularization.
     - RMSE = 7,463.96.
  3. **K-Nearest Neighbors (KNN)**:
     - Optimized hyperparameters for neighbors and distance metrics.
     - RMSE = 8,526.55.
  4. **AdaBoost Regressor**:
     - Combined with a Random Forest base estimator for better accuracy.
  5. **Ridge Regression**:
     - Offered robust regularization and improved model performance.

- **Feature Importance**:
  - Analyzed feature importance using XGBoost to determine the most impactful predictors of price, such as `year`, `horsepower`, and `maximum_torque`.

### Kaggle Results
- **Score**: RMSE = 5,152.31.

---

## Files in the Repository

- **`notebooks/`**:
  - Contains the Jupyter notebook for the entire analysis.
- **`data/`**:
  - Training and testing datasets.
- **`results/`**:
  - Predictions and feature importance results.
- **`README.md`**:
  - This file.

---

## How to Run the Code
1. Clone the repository:
   ```bash
   git clone https://github.com/yourusername/used-car-prices.git

