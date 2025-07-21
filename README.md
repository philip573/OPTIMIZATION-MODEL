# OPTIMIZATION-MODEL
COMPANY NAME: CODTECH IT SOLUTIONS
NAME: STALLAN N PHILOS
INTER ID:CT08DL10
DOMAIN: DATA SCIENCE
DURATION: 8 WEEKS
MENTOR: NEELA SANTHOSH
# Loan Default Prediction - Internship Project (Task 4)

This repository contains the complete implementation of a machine learning project aimed at predicting loan default using a classification model. This task was part of the CODTECH internship program and involved end-to-end data science workflow, including preprocessing, handling class imbalance, model training, evaluation, hyperparameter tuning, and threshold optimization.

---

## 🔍 Problem Statement

Financial institutions face losses due to borrowers defaulting on loans. The objective of this project is to build a model that accurately predicts whether a loan applicant is likely to default or not, helping lenders make informed decisions.

---

## 📁 Dataset

The dataset used contains anonymized information about borrowers and their loans, with the target variable `Default` indicating whether the borrower defaulted (1) or not (0).

**Features include:**
- Age
- Income
- Credit Score
- Employment Type
- Marital Status
- Education
- Loan Amount
- Loan Purpose
- Loan Term
- Debt-to-Income Ratio (DTI)
- Has Mortgage, Dependents, Co-Signer (binary features)

---

## 🧪 Workflow

### 1. **Data Preprocessing**
- Loaded CSV using `pandas`
- Handled missing values
- Encoded categorical variables using Label Encoding and One-Hot Encoding
- Feature scaling using `StandardScaler`
- Dropped irrelevant columns (`LoanID`)

### 2. **EDA (Exploratory Data Analysis)**
- Analyzed class distribution of `Default`
- Visualized distribution of categorical features

### 3. **Train-Test Split**
- Used `train_test_split` with `stratify=y` to maintain class balance

### 4. **Handling Imbalance**
- Applied **SMOTE** (Synthetic Minority Oversampling Technique) to balance the target classes

### 5. **Modeling**
- Base model: `RandomForestClassifier`
- Improved model with **Hyperparameter Tuning** using `GridSearchCV`
- Evaluated using classification report and confusion matrix

### 6. **Threshold Optimization**
- Calculated F1 scores for thresholds from 0.1 to 0.55
- Found optimal threshold = **0.40** for better recall on class 1

---

## 📈 Results

### ✅ **Best Parameters from Grid Search**
```python
{'max_depth': 20, 'min_samples_leaf': 1, 'min_samples_split': 2, 'n_estimators': 200}
| Metric    | Class 0 | Class 1 |
| --------- | ------- | ------- |
| Precision | 0.93    | 0.24    |
| Recall    | 0.78    | 0.54    |
| F1-Score  | 0.85    | 0.34    |
| Accuracy  | 0.75    |         |
🛠️ Tech Stack
Python

Pandas, NumPy

Scikit-learn

Matplotlib, Seaborn

Imbalanced-learn (SMOTE)
 Project Structure:
loan-default-prediction/
│
├── data/
│   └── Loan_default.csv
├── Loan_Default_Prediction.ipynb
├── README.md
└── saved_model.pkl  # (Optional, if saved)
 How to Run
Clone the repo

Install required libraries:
pip install -r requirements.txt
un the Jupyter Notebook:
jupyter notebook Loan_Default_Prediction.ipynb
 License
This project is for educational purposes as part of the internship program and is not intended for commercial use.

##output:

[Image](https://github.com/user-attachments/assets/0aac8eb3-6e0d-4076-a1d0-673ff50f84f5)
