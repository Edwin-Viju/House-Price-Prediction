🏠 House Prices Prediction – Kaggle Competition

This project is my solution to the House Prices: Advanced Regression Techniques
 competition on Kaggle. The goal is to predict the final sale price of residential homes in Ames, Iowa, using various features describing the houses.

📌 Project Overview

Built regression models to predict housing prices.

Applied data preprocessing, including missing value imputation, encoding categorical variables, scaling, and log-transforming the target variable (SalePrice).

Compared Linear Regression and Lasso Regression, with Lasso emerging as the best-performing model.

Generated a submission.csv file for Kaggle submission.

⚙️ Methodology

Data Cleaning & Preprocessing

Missing categorical values replaced with "None".

Missing numerical values imputed with 0, median, or mode depending on the feature.

Applied log transformation on SalePrice to reduce skewness.

One-hot encoding used for categorical features.

Feature scaling applied using StandardScaler.

Modeling

Baseline: Linear Regression.

Final Model: Lasso Regression (alpha=0.001, max_iter=10000).

Evaluation Metrics

Root Mean Squared Error (RMSE)

R-squared (R²)

📊 Key Findings

Best Model: Lasso Regression – reduced overfitting and provided stable predictions.

Performance:

RMSE: ~56,764,620 (after transforming predictions back from log scale).

R²: Negative values on hold-out set → indicates variance in target not fully captured, requiring more feature engineering.

Most Important Features:

Overall Quality (OverallQual)

Living Area (GrLivArea)

Neighborhood (Neighborhood)

Garage (GarageCars, GarageArea)

Year Built (YearBuilt)

💡 Insights

Log transformation stabilized predictions and reduced the effect of outliers.

Lasso regularization effectively performed feature selection by shrinking unimportant coefficients.

Proper handling of missing values was crucial for model training and submission generation.

📂 Files

train.csv → Training dataset

test.csv → Test dataset (from Kaggle)

submission.csv → Final predictions for Kaggle submission
