Credit Delinquency Prediction
Overview
       This project focuses on predicting credit delinquency using machine learning.  
Credit delinquency occurs when borrowers fail to make timely payments, which can result in significant financial losses for lenders.  
By analyzing financial and behavioral data, this project aims to help institutions assess risk, improve lending strategies, and reduce losses.  

Business and Data Understanding
Business Understanding
•	Lenders face challenges in identifying high-risk customers early.  
•	Accurate prediction of delinquency enables better credit decisions and proactive risk management.  
•	Key business goals:
o	Reduce default rates  
o	Protect profit margins  
o	Improve financial inclusion  

Data Understanding
Dataset: `Delinquency_prediction_dataset.csv`  
•	Key features include:
o	Customer demographics (Age, Employment Status)  
o	Financial metrics (Income, Loan Balance, Debt-to-Income Ratio, Credit Score)  
o	Behavioral patterns(Missed Payments, Credit Utilization, Account Tenure, Monthly records)  
o	Target variable: `Delinquent_Account` (Yes/No)  

Modelling
Preprocessing
•	Cleaned categorical labels (e.g., Employment Status inconsistencies)  
•	Imputed missing values:
•	`Income`, `Loan_Balance` → Median  
•	`Credit_Score` → Mean  
•	Detected strong **class imbalance** (very few delinquent cases)

Exploratory Data Analysis
•	Generated profiling report (`ydata_profiling`)  
•	Visualized correlations & distributions  
•	Identified strong risk factors: Credit Utilization, Payment History, Credit Score

Model Training
•	Used PyCaret AutoML for rapid prototyping  
•	Initial models had high accuracy but poor recall (due to imbalance)  
•	Applied SMOTE to oversample minority class  
•	Tuned and calibrated  KNN  with isotonic regression  

Model Output Analysis
Results
Before SMOTE
•	Accuracy: High
•	Recall: 0 (models ignored minority class)
After SMOTE
•	Significant recall improvement
•	Best performing model: KNN with calibration
Feature Importance
•	Credit Utilization
•	Missed Payments
•	Credit Score

Conclusion
The project successfully demonstrates how data preprocessing, class balancing, and calibration can improve delinquency prediction.  
