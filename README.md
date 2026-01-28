# kaggle_credit_risk_data_pd_model_and_scoring
### Credit Risk – Probability of Default (PD) Model

Overview
This repository contains an interpretable Probability of Default (PD) model built using logistic regression in Python. The model estimates borrower-level default probabilities using demographic, financial, and credit-related features, with a focus on explainability and business applicability.

Problem Statement  
The objective is to estimate the probability that a borrower will default based on information available at loan origination. Such PD estimates are commonly used for credit approval, risk-based pricing, and portfolio risk monitoring.

Data and Features  
The model uses borrower-level features including age, income, employment length, loan amount, interest rate, loan-to-income ratio, credit history length, housing status, and loan purpose. Categorical variables are one-hot encoded and numeric variables are scaled.

Methodology  
- Performed a stratified train-test split to preserve default rates  
- Built a logistic regression model to estimate default probabilities  
- Handled class imbalance using class weights (no synthetic oversampling)  
- Generated probability outputs rather than binary predictions  

Model Evaluation  
The model is evaluated using standard credit risk metrics:
- ROC-AUC: 0.85  
- KS Statistic: 0.54  
- Gini Coefficient: 0.70  

These metrics measure the model’s ability to distinguish between defaulters and non-defaulters.

Business Application  
The predicted probabilities are used to segment borrowers into risk buckets and support lending decisions such as approval, pricing, and rejection. Model coefficients are used to explain key drivers of default risk at the borrower level.

Tools and Technologies  
Python, pandas, NumPy, scikit-learn, Matplotlib

Notes  
This project demonstrates a baseline PD modeling approach commonly used in credit risk analytics. It is intended for learning and portfolio demonstration purposes. Future extensions could include WoE/IV binning, stability analysis, and calibration.
