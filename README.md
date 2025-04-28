# Machine-Learning-Models-for-Fraud-Detection-in-Transaction-Monitoring
Summary:
This study shows how to use logistic regression to identify financial transaction fraud. Using a highly unbalanced dataset of financial transactions, the objective is to create a machine learning model that can recognize suspicious (fraudulent) transactions. Both fraudulent and non-fraudulent transaction data are included in the synthetic dataset utilized in this research, which was created especially for Anti-Money Laundering (AML) purposes.
Key Points:
•	Logistic Regression:The main model for detecting fraud in this research is logistic regression, which uses class weights to correct for dataset imbalance.
•	SMOTE: By creating fictitious instances of the minority class (fraudulent transactions), SMOTE (Synthetic Minority Over-sampling Technique) is used to address class imbalance.
•	Data Preprocessing: Data preprocessing involves methods like one-hot encoding of categorical information and scaling numerical features.
•	Model Evaluation: ROC-AUC, precision, recall, F1-score, and confusion matrices are used to visualize the Logistic Regression model's performance.
Dataset
The Synthetic Transaction Monitoring Dataset for AML from Kaggle is used in this study. It includes a number of transaction attributes, including:
•	Information about the sender and recipient (such as account number and bank location)
•	Amount of Transaction
•	Type of Payment
•	Amount
Whether the transaction is valid (0) or fraudulent (1) is indicated by the target variable.
Project Objective:
•	The goal of the project is to use logistic regression to create a predictive model for fraud detection.
•	To utilize methods like SMOTE to balance the data and assess the model's performance on an unbalanced dataset.
•	To assess model performance using evaluation metrics such as ROC-AUC, F1-score, precision, and recall.
Important attributes:
•	Data preprocessing includes encoding category variables, scaling numerical characteristics, and handling missing data.
•	Class Imbalance Handling: To improve model performance for predicting fraudulent transactions, SMOTE is used to oversample the minority class.
•	Model Evaluation: Using ROC curves, classification reports, and confusion matrices, the model is evaluated.
Technologies Used:
•	Programming Language: Python
•	Libraries: Pandas, Matplotlib, Seaborn, Scikit-learn, Imbalanced-learn (SMOTE)
•	Machine Learning: Logistic Regression
•	Data Preprocessing: OneHotEncoder, StandardScaler, SMOTE
•	Model Evaluation: Classification Report, Confusion Matrix, ROC Curve, AUC
Logistic Regression Results: 
•	The model was successful in forecasting valid transactions, as evidenced by the extremely high precision for non-fraudulent transactions.
•	The model missed a lot of fraudulent transactions since its recall for fraudulent transactions was low.
•	The model was biased toward predicting non-fraudulent transactions, as evidenced by the extremely low F1-score for fraudulent transactions.
•	ROC Curve: The low AUC value suggested that the system did a poor job of differentiating between transactions that were fraudulent and those that weren't.
Random Forest Results:
•	Fraudulent transactions had higher precision and recall, indicating that the Random Forest model was more effective at spotting fraud.
•	In comparison to Logistic Regression, the F1-score for both classes was balanced, demonstrating a superior trade-off between precision and recall.
•	ROC Curve: The Random Forest model performed better in identifying fraudulent transactions, as evidenced by its higher AUC score.
Confusion Matrix Comparison: 
•	The high false positive rate of logistic regression was caused by several false positives, or transactions that were not fraudulent but were mistakenly labeled as such.
•	Random Forest produced fewer false positives and more accurate classifications of fraudulent transactions.
Conclusion:
•	Particularly on unbalanced datasets, Random Forest outperformed Logistic Regression in the identification of fraud. More fraudulent transactions were successfully detected while keeping a respectable balance between recall and precision.
•	Despite being computationally effective and simple to understand, logistic regression has trouble handling unbalanced data and tended to label the majority of transactions as legitimate.
