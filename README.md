# credit-risk-prediction-lightgbm
End-to-end machine learning pipeline for credit default risk prediction, including data preprocessing, feature aggregation, feature engineering, and LightGBM model training with stratified cross-validation.

Credit Risk Prediction with LightGBM
📌 Overview
This project explores the prediction of customer default risk using the Home Credit Default Risk dataset.

The objective is to estimate the probability of loan default by combining customer profile information, financial data, previous applications, bureau records, payment history, and behavioral indicators.

The project covers the complete machine learning workflow, including data preparation, feature engineering, model development, hyperparameter tuning, performance evaluation, and model interpretation.

🎯 Business Problem
Financial institutions need to evaluate the risk associated with granting credit to customers.

Traditional approaches often rely on a limited set of variables, while machine learning models can leverage large volumes of structured data to identify complex patterns associated with default behavior.

The goal of this study is to build a predictive model capable of supporting credit risk assessment through data-driven insights.

📊 Dataset
Source:

Home Credit Default Risk (Kaggle)

Data sources include:

Application data

Bureau credit history

Previous loan applications

Credit card balances

POS cash balances

Installment payments

The final modeling dataset combines information from multiple tables through feature aggregation techniques.

🛠️ Methodology
Data Preparation
Missing value handling

Memory optimization

Feature aggregation across multiple datasets

Dataset merging

Feature Engineering
Creation of business-oriented variables such as:

Credit-to-income ratio

Credit-to-annuity ratio

Income-per-family-member ratio

Employment-related indicators

Historical behavioral metrics

Additional aggregated features were generated from:

Bureau records

Previous applications

Installment payments

Credit card balances

POS cash balances

🤖 Models Evaluated
Baseline
Logistic Regression

Advanced Model
LightGBM Classifier

The LightGBM model was selected due to its strong performance on structured/tabular datasets, ability to capture non-linear relationships, robustness to missing values, and computational efficiency.

⚙️ Hyperparameter Tuning
A controlled hyperparameter tuning process was performed to evaluate potential performance gains.

Parameters explored included:

Learning rate

Number of trees

Number of leaves

Regularization parameters

Sampling strategies

Although some configurations produced slight improvements, the performance gains were marginal compared to the increase in computational cost.

This reinforced an important practical lesson: model complexity does not always translate into meaningful business value.

📈 Evaluation Metric
The primary evaluation metric was:

ROC AUC (Receiver Operating Characteristic Area Under the Curve)

This metric is widely used in credit risk modeling because it measures the model's ability to distinguish between default and non-default customers across different decision thresholds.

🏆 Results
Model	ROC AUC
Logistic Regression	Baseline
LightGBM	~0.782
Key findings:

LightGBM significantly outperformed the baseline model.

Feature engineering contributed substantially to performance improvements.

Hyperparameter tuning generated limited gains relative to execution time.

Data quality and feature design proved as important as algorithm selection.

🔍 Feature Importance
Among the most relevant predictors identified by the model were:

CREDIT_ANNUITY_RATIO

EXT_SOURCE_1

EXT_SOURCE_2

EXT_SOURCE_3

DAYS_BIRTH

Bureau-derived aggregated features

Previous application indicators

Payment history metrics

These results highlight the importance of combining financial, behavioral, and historical information when assessing credit risk.

📚 Key Learnings
Some of the main lessons from this project were:

Feature engineering often has greater impact than model tuning.

Gradient Boosting models remain highly effective for tabular data.

Validation strategy is critical to obtaining reliable performance estimates.

Small metric improvements should always be weighed against computational costs.

Model interpretability remains essential in regulated domains such as credit risk.

🧰 Technologies
Python

Pandas

NumPy

Scikit-learn

LightGBM

Matplotlib

Seaborn

Jupyter Notebook

🚀 Future Improvements
Potential next steps include:

CatBoost implementation and comparison

Ensemble methods (LightGBM + CatBoost + XGBoost)

SHAP explainability analysis

Automated hyperparameter optimization

Feature selection techniques

Model deployment pipeline

📄 Author
Luis Felipe

Data Analytics | Machine Learning | Procurement Analytics | Business Intelligence

Feel free to connect, provide feedback, or discuss ideas related to machine learning and credit risk modeling.