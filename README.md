Bad Loan Detection
This project focuses on identifying bad loans (loans that are unlikely to be repaid) using machine learning techniques. The goal is to predict whether a loan is "bad" or "good" based on historical loan data, enabling financial institutions to manage risk more effectively.

Project Overview
Loan defaults pose a significant risk to financial institutions. This project uses machine learning to classify loans into:
Good Loans (likely to be repaid)
Bad Loans (likely to default)
The main challenges include:
Imbalanced Data: Bad loans are far fewer than good loans.
Generalization: Ensuring the model performs well on unseen test data.

Dataset
The dataset includes:

Features: Information about loans (e.g., loan amount, interest rate, payment history).
Target: Binary column indicating:
0 = Good Loan
1 = Bad Loan
Imbalance Issue:
Majority Class: Good loans (~93%)
Minority Class: Bad loans (~7%)


Approach
The project workflow includes:

Data Preprocessing:
Handling missing values.
Encoding categorical variables.
Feature scaling and normalization.
Class Imbalance Handling:
Applied SMOTE (Synthetic Minority Oversampling Technique).
Combined SMOTE with undersampling using SMOTEENN for cleaner resampling.
Model Development:
Built a Feedforward Neural Network for binary classification.
Used a weighted loss function to address class imbalance.
Hyperparameter Tuning:
Adjusted learning rates, thresholds, and regularization parameters.
Evaluation:
Monitored F1-score, Precision, Recall, and Validation Loss.
