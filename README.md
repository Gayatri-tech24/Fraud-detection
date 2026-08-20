# Fraud Detection Using Machine Learning

## 📌 Overview

This project focuses on detecting fraudulent credit card transactions using machine learning. Since fraudulent transactions are significantly rarer than legitimate transactions, the project focuses not only on model performance but also on handling **class imbalance** and evaluating the model using appropriate classification metrics.

The project covers the complete machine learning workflow, from data preprocessing and exploratory analysis to model comparison, evaluation, threshold analysis, and explainable AI.

## 🎯 Problem Statement

Credit card fraud detection is a highly imbalanced classification problem where correctly identifying fraudulent transactions is more important than simply achieving high overall accuracy.

The objective of this project is to build a machine learning model that can effectively distinguish between:

* **Legitimate transactions**
* **Fraudulent transactions**

## 📊 Dataset

The project uses the **Credit Card Fraud Detection dataset**.

The dataset contains anonymized transaction features along with a `Class` target variable:

* `0` → Legitimate transaction
* `1` → Fraudulent transaction

The dataset is not included in this repository because of its large file size.

## 🔧 Project Workflow

### 1. Data Exploration

* Examined dataset structure and feature distributions
* Checked for missing values
* Analyzed the target-class distribution
* Identified the severe class imbalance between legitimate and fraudulent transactions

### 2. Data Preprocessing

* Checked and handled data quality issues
* Separated features and target variable
* Applied appropriate feature scaling
* Prepared the data for machine learning models

### 3. Handling Class Imbalance

Because fraudulent transactions represent only a small portion of the dataset, accuracy alone is not a reliable metric.

The project explores techniques for dealing with class imbalance and evaluates their effect on model performance.

### 4. Model Training

Multiple machine learning approaches were evaluated and compared to identify a suitable model for fraud detection.

### 5. Model Evaluation

The models were evaluated using:

* Precision
* Recall
* F1-score
* ROC-AUC
* Confusion Matrix

Special attention was given to **Recall**, since failing to detect an actual fraudulent transaction can be costly.

### 6. Threshold Analysis

Different classification thresholds were evaluated to understand the trade-off between precision and recall.

This helps determine a threshold that provides a practical balance between:

* Detecting more fraudulent transactions
* Avoiding excessive false positives

### 7. Explainable AI

SHAP-based analysis was used to investigate feature contributions and improve the interpretability of the model's predictions.

This helps answer:

> **Why did the model classify this transaction as potentially fraudulent?**

## 📈 Results

The final model was selected based on its ability to detect fraudulent transactions while maintaining a reasonable balance between precision and recall.

### Key Evaluation Metrics

| Metric    |          Result |
| --------- | --------------: |
| Precision | Add final value |
| Recall    | Add final value |
| F1-Score  | Add final value |
| ROC-AUC   | Add final value |

## 🧠 Key Learnings

Through this project, I explored:

* Imbalanced classification problems
* Data preprocessing and feature scaling
* Precision vs. recall trade-offs
* Classification threshold optimization
* Model comparison
* Confusion matrix analysis
* Explainable AI using SHAP
* Practical considerations in fraud detection

## 🛠️ Technologies Used

* Python
* Pandas
* NumPy
* Matplotlib
* Seaborn
* Scikit-learn
* XGBoost
* Imbalanced-learn
* SHAP
* Jupyter Notebook

## 📁 Repository Structure

```text
Fraud-detection/
│
├── fraud_detection.ipynb
├── README.md
└── .gitignore
```

The dataset is intentionally excluded from the repository because of its size.

## 🚀 Future Improvements

Possible future improvements include:

* Hyperparameter optimization
* More extensive imbalance-handling experiments
* Cost-sensitive learning
* Real-time fraud detection pipeline
* Model monitoring and drift detection
* Deployment through an API or web application

## 👩‍💻 Author

**Gayatri Arvind Gundad**

CSE Student | Machine Learning & Data Analytics Enthusiast
