# Experiment 3: Regression Analysis (Loan Amount Prediction)

## 🎯 Objective

The primary goal of this experiment is to predict the **Loan Sanction Amount (USD)** for applicants based on various features such as income, credit score, employment type, and property details. We explore different linear regression models and the impact of regularization (L1 and L2).

## 📊 Dataset

- **Source**: Predict Loan Amount Data
- **Target Variable**: `Loan Sanction Amount (USD)`
- **Key Features**:
  - `Loan Amount Request (USD)`
  - `Income (USD)`
  - `Credit Score`
  - `Property Age`
  - `Profession`
  - `Income Stability`

## 🛠️ Methodology

1. **Preprocessing**:
   - Imputed missing values (Mean for numerical, Most Frequent for categorical).
   - Standardized numerical features.
   - One-Hot Encoding for categorical features.
   - Handled column name mismatches (stripping whitespaces and handling symbols).
2. **Exploratory Data Analysis (EDA)**:
   - Visualized target distribution (skewness check).
   - Correlation heatmap to identify strong predictors.
3. **Modeling**:
   - **Linear Regression**: Baseline model.
   - **Ridge Regression (L2)**: To handle multicollinearity and prevent overfitting.
   - **Lasso Regression (L1)**: For feature selection and simplicity.
   - **Elastic Net**: Combining both L1 and L2 penalties.
4. **Hyperparameter Tuning**:
   - Used `GridSearchCV` to optimize `alpha` and `l1_ratio`.

## 📈 Results

| Model                   | MAE        | RMSE       | R2 Score   |
| :---------------------- | :--------- | :--------- | :--------- |
| **Linear Regression**   | 21,588     | 31,925     | 0.5510     |
| **Ridge (Tuned)**       | 21,582     | 31,897     | 0.5517     |
| **Lasso (Tuned)**       | 21,564     | 31,905     | 0.5515     |
| **Elastic Net (Tuned)** | **21,642** | **31,882** | **0.5522** |

### Top 3 Predictors:

1. **Loan Amount Request (USD)**
2. **Income (USD)**
3. **Credit Score**

## 🖼️ Visualizations

- **Actual vs Predicted Plot**: Shows how well the model captures the variations.
- **Residual Plot**: Checks for patterns in errors (homoscedasticity).
- **Learning Curves**: Diagnostics for Bias-Variance trade-off.
- **Coefficients Comparison**: Visualizes how regularization shrinks different feature weights.

## 🚀 How to Run

1. Ensure the dataset is in `../dataset/Predict Loan Amount Data/`.
2. Activate your environment (`.\venv\Scripts\Activate.ps1`).
3. Run the notebook: `jupyter notebook notebooks/experiment3.ipynb`.
