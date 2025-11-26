# Alkaloid-ML-MCF7-Anticancer-Prediction
A machine learning project developed to predict the anticancer potency of alkaloid compounds against MCF-7 breast cancer cells. The workflow includes data extraction, preprocessing, molecular descriptor generation, feature engineering, model training, and performance evaluation to identify the most reliable predictive model for alkaloid activity



🔰 Shields.io Badges
<p> <img src="https://img.shields.io/badge/Python-3.9+-blue.svg" alt="Python"> <img src="https://img.shields.io/badge/ML-ScikitLearn-orange.svg" alt="ML"> <img src="https://img.shields.io/badge/License-MIT-green.svg" alt="License"> <img src="https://img.shields.io/badge/Status-Active-success.svg" alt="Status"> <img src="https://img.shields.io/badge/Cancer%20Type-MCF--7-red.svg" alt="MCF7"> <img src="https://img.shields.io/badge/Data-Alkaloids-yellow.svg" alt="Alkaloids"> </p>
📊 Sample Results Table

Below is an example showing the performance of different models on pIC50 prediction:

Model	Features Used	R² Score	RMSE	MAPE	MDAPE
Gradient Boosting Regressor	2D Descriptors	0.58	0.70	9.67%	6.64%
Random Forest Regressor	Fingerprints + 2D	0.51	0.75	11.2%	8.90%
SVR	2D Descriptors	0.47	0.79	12.8%	9.40%
Linear Regression	2D Descriptors	0.29	0.92	18.5%	15.2%
📈 Sample Visualization (Model Comparison Graph)

You can include this placeholder plot until you generate actual graphs:

┌───────────────────────────────────────────────┐
│          Model Performance Comparison          │
├───────────────┬───────────────┬───────────────┤
│    Model      │     R²        │     RMSE       │
├───────────────┼───────────────┼───────────────┤
│ GradientBoost │      ↑        │      ↓         │
│ RandomForest  │      →        │      →         │
│ SVR           │      ↓        │      ↑         │
│ LinearReg     │      ↓↓       │      ↑↑        │
└───────────────────────────────────────────────┘


If you want a real Matplotlib plot, I can generate the Python code for you.

🧬 Project Logo (ASCII Version)
        __    _      _       _     _     _ 
   /\  /__\  | | ___| |_ ___| |__ (_)___| |
  /  \/ \//  | |/ _ \ __/ __| '_ \| / __| |
 / /\  _  \  | |  __/ || (__| | | | \__ \_|
