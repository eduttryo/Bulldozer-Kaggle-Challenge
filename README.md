🚜 Bulldozer Sale Price Prediction (Kaggle)

This project explores a machine learning approach to predict bulldozer sale prices using historical auction data from the Kaggle Bluebook for Bulldozers competition.

📌 Problem Statement

The goal is to build a regression model capable of predicting the SalePrice of bulldozers based on their characteristics and past sales information.

📊 Dataset

The dataset comes from Kaggle’s Bluebook for Bulldozers competition:

TrainAndValid.csv – Training + validation data

Test.csv – Test data for final predictions

Key features include equipment attributes, usage details, and sale dates.

⚙️ Approach
1. Data Preprocessing & Feature Engineering

Parsed the saledate column into:

saleYear

saleMonth

saleDay

saleDayOfWeek

saleDayOfYear

Removed original saledate

2. Handling Missing Values

Numeric features:

Missing values filled with median

Added _is_missing indicator columns

Categorical features:

Converted to numerical codes

Missing values tracked via _is_missing columns

3. Model

A RandomForestRegressor was used due to its robustness with tabular data and minimal preprocessing requirements.

4. Hyperparameter Tuning

Applied RandomizedSearchCV to optimize:

n_estimators

max_depth

min_samples_split

min_samples_leaf

max_features

5. Evaluation Metrics

Models were evaluated using:

RMSLE (Root Mean Squared Log Error)

MAE (Mean Absolute Error)

R² Score

📈 Results

After tuning, the optimized Random Forest model provided improved validation performance and was used to generate predictions on the test set.

🧪 How to Run

Clone the repository

Install dependencies:

pip install -r requirements.txt

Open the notebook:

jupyter notebook

Run:

Bulldozer sale price prediction - Kaggle.ipynb
📦 Dependencies

See requirements.txt

🔗 Reference

Kaggle Competition:
https://www.kaggle.com/competitions/bluebook-for-bulldozers