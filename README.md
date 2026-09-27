# Loan Default Risk Modeling for Professional Lending

## Project overview
This project tackles a credit risk challenge for the local bank Crelan seeking to build a risk tool to assess the credit quality of newly originated professional loans in the independent segment.

The objective is to develop a predictive machine learning model that estimates the probability that a borrower will default on a loan, helping the bank better manage approval decisions and portfolio risk.

## Business goal
The challenge aims to build an application scoring model for professional loans, with the final goal of identifying customers with a higher likelihood of default and flagging them appropriately for credit risk monitoring.

The model supports two related use cases:
- Application scoring: determining whether a loan request should be accepted based on the applicant's creditworthiness
- Behavioural scoring: monitoring the likelihood of default for an existing credit, which may also be used as an input in regulatory capital calculations

## Target variable
The target variable is a binary classification:
- Class 0: Non-default
- Class 1: Default = credit obligations defaulted over a period of 24 months

This is a classic credit risk classification problem, where the objective is to distinguish between low-risk and high-risk borrowers using historical lending information.

## Dataset description
The dataset contains around 15,000 professional loans and includes approximately 180 features.

The data combines multiple types of information:
- Company information (e.g. years in business, business profile)
- Financial data (e.g. cash flow, monthly income, average positive savings)
- Socio-demographic information (e.g. marital status, age, group)
- Behavioural features (e.g. historical credit behaviour)

The repository does not include the raw dataset publicly because of a non-disclosure agreement (NDA). However, the project workflow, preprocessing logic, feature engineering choices, and model evaluation steps are documented here.

## Data files
This challenge contains the following key datasets:
- `DSC_training`: training dataset used to build and validate the model
- `DSC_scoring`: scoring dataset used to generate predictions for new cases without known labels

The final model is intended to output probability scores for Class 1 (default), which can then be used for class assignment and risk ranking.

## Methodology
The analysis follows a standard credit risk modeling workflow:
1. Exploratory data analysis (EDA)
2. Data cleaning and missing-value treatment
3. Feature engineering and transformation
4. Categorical and numerical preprocessing
5. Feature selection and dimensionality reduction
6. Model comparison and tuning
7. Evaluation using probability-based ranking metrics

## Modeling approach
Several machine learning models were evaluated to identify the most suitable approach for default prediction, including:
- Logistic Regression
- Random Forest
- Gradient boosting methods
- HistGradientBoostingClassifier

The final model was selected based on performance in identifying defaulted borrowers while maintaining a reasonable trade-off between false positives and false negatives.

## Expected business value
A robust application score can help the bank:
- reduce credit losses
- improve underwriting quality
- prioritise risk review for high-risk applicants
- make more consistent lending decisions based on objective evidence

## Notes on reproducibility
The original dataset is intentionally excluded from this GitHub repository due to NDA restrictions. To keep the project transparent and portfolio-ready, the work focuses on:
- clearly documented methodology
- explainable preprocessing decisions
- model comparison and evaluation logic
- business interpretation of the final results

## Conclusion
This project demonstrates the practical workflow of building a credit risk model for loan default prediction using real-world banking data. Even without sharing the raw data publicly, the project reflects a realistic machine learning pipeline for a financial risk use case.