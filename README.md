# Bad Loan Detection

This project focuses on identifying bad loans using machine learning techniques. The goal is to predict whether a loan is "bad" or "good" based on historical loan data, enabling financial institutions to manage risk more effectively.

## Project Overview

Loan defaults pose a significant risk to financial institutions. This project uses machine learning to classify loans into:

- **Good Loans**
- **Bad Loans**

The main challenges include:

- **Imbalanced Data**: Bad loans are far fewer than good loans.
- **Generalization**: Ensuring the model performs well on unseen test data.

## Dataset

The dataset includes:

- **Features**: Information about loans (e.g., loan amount, interest rate).
- **Target**: Binary column indicating:
  - `0 = Good Loan`
  - `1 = Bad Loan`

### Imbalance Issue

- **Majority Class**: Good loans (~93%)
- **Minority Class**: Bad loans (~7%)

## Approach

The project workflow includes:

### Data Preprocessing

- Handling missing values.
- Encoding categorical variables.
- Feature scaling and normalization.

### Class Imbalance Handling

- Applied **SMOTE** (Synthetic Minority Oversampling Technique).
- Subsample
- Weighted loss function.

### Model Development

- Built a **Feedforward Neural Network** for binary classification.
- Used a weighted loss function to address class imbalance.

### Hyperparameter Tuning

- Adjusted learning rates, thresholds, and regularization parameters.

### Evaluation

- Monitored **F1-score**, **Precision**, **Recall**, and **Validation Loss**.

## Model Architecture

The neural network has the following architecture:

- **Input Layer**: Accepts preprocessed loan features.
- **Hidden Layers**:
  - Dense layers with ReLU activation.
  - Dropout layers and L2 for regularization.
- **Output Layer**:
  - Single neuron with Sigmoid activation for binary classification.

## Installation

To replicate this project, follow these steps:

### Clone the Repository

```bash
git clone https://github.com/LvSophia/bad_loan_detection.git
cd bad_loan_detection
```

### Create a Virtual Environment

```bash
python3 -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate
```

### Install Dependencies

```bash
pip install -r requirements.txt
```
Note: I use Google colab, you might do not need some lines in the code

## Usage

To train and evaluate the model:

1. **Run EAD in `JP_project.ipynb`**:
   - This step will produce a cleaned training dataset.

2. **Run training and inference in `model_training.ipynb`**:
   - The model will be trained, and the best model weights will be saved.
   - Use the saved model to predict the test dataset.

3. **Output**:
   - Generates a CSV file with predictions for the target column.

## Future Improvements

### Explore XGBoost for Improved Performance

### Feature Importance Analysis
- Utilize **XGBoost's built-in feature importance analysis** to identify the most critical features in the dataset.
- Visualize feature importance to gain deeper insights into loan-related attributes and their impact on outcomes.

### Additional Techniques
- Experiment with **ensemble methods** to combine the strengths of Neural Networks and XGBoost.
  - For example, use Neural Networks for feature extraction and XGBoost for final classification.
- Apply **SHAP (SHapley Additive exPlanations)** to:
  - Explain individual predictions for better interpretability.
  - Assess the contribution of each feature to the model's decision-making process.
  - Provide stakeholders with actionable insights into loan outcomes.

These improvements can enhance the overall performance, interpretability, and applicability of the model, enabling better decision-making for bad loan detection.
