# Loan-Default-Prediction
Predicting loan defaults using machine learning
# Loan Default Prediction Model

## Overview
This project aims to predict the likelihood of borrowers defaulting on loans for a financial institution. By leveraging machine learning, the model identifies high-risk borrowers, enabling targeted interventions to reduce defaults. The solution achieved **Top 13% performance** on Coursera's leaderboard with an AUC of 0.756.

## Dataset
- **Train Data**: 255,347 loans with 17 features (e.g., `Income`, `CreditScore`, `LoanPurpose`) and a binary `Default` target.
- **Test Data**: 109,435 loans for prediction submission.
- **Features**: Include numerical (e.g., `Age`, `LoanAmount`) and categorical (e.g., `Education`, `EmploymentType`) variables.

## Approach
1. **Data Exploration**: Analyzed class imbalance (11.6% default rate) and feature correlations.
2. **Feature Engineering**:
   - Created `Loan-to-Income Ratio`, `Interest Cost Burden`, and `Loan-to-Credit Score` to capture financial strain.
   - Encoded categorical variables (e.g., `Education`, `EmploymentType`).
3. **Modeling**:
   - Used **Random Forest** for handling non-linear patterns and class imbalance (`class_weight='balanced'`).
   - Optimized hyperparameters via `GridSearchCV` (e.g., `max_depth=12`, `n_estimators=300`).
4. **Evaluation**: Achieved **75% recall** (identifies 75% of true defaults) and **AUC 0.756**.

## Results
| Metric          | Score  |
|-----------------|--------|
| ROC AUC         | 0.756  |
| Recall (0.4 threshold) | 75%    |
| Precision       | 21%    |

## Business Impact
- Targets **65,000 high-risk borrowers** for interventions (e.g., payment plans).
- **Estimated savings**: $150M annually (assuming $2k cost per prevented default).

## Installation
1. Clone the repository:
   ```bash
   git clone https://github.com/yourusername/loan-default-prediction.git
