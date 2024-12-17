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

Model Architecture
The neural network has the following architecture:
Input Layer: Accepts preprocessed loan features.
Hidden Layers:
Dense layers with ReLU activation.
Dropout layers for regularization.
Output Layer:
Single neuron with Sigmoid activation for binary classification.

Installation
To replicate this project, follow these steps:
Clone the repository:
git clone https://github.com/yourusername/bad_loan_detection.git
cd bad_loan_detection
Create a virtual environment:
python3 -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate
Install dependencies:
pip install -r requirements.txt

Usage
To train and evaluate the model:

Run Training:
python train.py
The model will be trained, and the best model weights will be saved.
Run Inference on Test Data:
python predict.py --test_data path_to_test_file.csv
Outputs a CSV with predictions for the target column.

