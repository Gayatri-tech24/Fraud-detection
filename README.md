# Fraud Detection Using Machine Learning

## 📌 Overview

This project builds a machine learning system for detecting fraudulent credit card transactions.

The main challenge in fraud detection is **class imbalance**, where legitimate transactions greatly outnumber fraudulent transactions. Because of this, accuracy alone is not a reliable measure of model performance.

The project focuses on comparing multiple machine learning models, evaluating them using fraud-relevant metrics, optimizing the classification threshold, and selecting a final model based on the trade-off between detecting fraud and minimizing false positives.

## 🎯 Problem Statement

The objective is to classify credit card transactions as either:

* **0 → Legitimate**
* **1 → Fraudulent**

The model should identify as many fraudulent transactions as possible while keeping false fraud alerts at a reasonable level.

## 📊 Dataset

The project uses the **Credit Card Fraud Detection dataset**, containing anonymized transaction features and a binary `Class` target.

The dataset contains a highly imbalanced distribution, making **Precision, Recall, F1-score and PR-AUC** particularly important evaluation metrics.

The dataset is not included in this repository because the file size exceeds GitHub's 100 MB limit.

## 🔧 Project Workflow

### 1. Data Exploration

* Examined the structure and distribution of the dataset
* Checked for missing values
* Analyzed the target variable
* Investigated the severe class imbalance
* Examined feature distributions

### 2. Data Preprocessing

* Separated features and target variable
* Prepared the data for machine learning
* Applied feature scaling where required
* Split the dataset into training and testing sets

### 3. Model Training

Four models were evaluated:

* Logistic Regression
* Random Forest
* XGBoost
* Isolation Forest

Both supervised and unsupervised approaches were considered for fraud detection.

## 📈 Model Comparison

| Model               |  Precision |     Recall |         F1 |    ROC-AUC |     PR-AUC |
| ------------------- | ---------: | ---------: | ---------: | ---------: | ---------: |
| Logistic Regression |     0.8507 |     0.6000 |     0.7037 |     0.9586 |     0.6975 |
| **Random Forest**   | **0.9571** | **0.7053** | **0.8121** | **0.9547** | **0.7898** |
| XGBoost             |     0.7273 |     0.6737 |     0.6995 |     0.8572 |     0.6171 |
| Isolation Forest    |     0.2097 |     0.2737 |     0.2374 |     0.9350 |     0.1092 |

### 🏆 Final Model: Random Forest

Random Forest was selected as the final model because it achieved the **highest F1-score (0.8121)** and **highest PR-AUC (0.7898)** among the evaluated models.

It also achieved a strong **precision of 0.9571**, meaning that most transactions predicted as fraudulent were actually fraudulent.

Its recall of **0.7053** means the model successfully detected approximately 70.5% of the fraudulent transactions in the evaluated dataset.

## 🎚️ Threshold Optimization

Instead of relying only on the default classification threshold of 0.5, different thresholds were investigated to understand the relationship between precision and recall.

A threshold of **0.4** was evaluated for the Random Forest model.

### Confusion Matrix at Threshold 0.4

|                       | Predicted Legitimate | Predicted Fraud |
| --------------------- | -------------------: | --------------: |
| **Actual Legitimate** |               56,646 |               5 |
| **Actual Fraud**      |                   26 |              69 |

This resulted in:

* **56,646 True Negatives**
* **5 False Positives**
* **26 False Negatives**
* **69 True Positives**

At this threshold, the model identifies a large proportion of fraudulent transactions while producing very few false fraud alerts.

## 🧠 Key Learnings

This project provided practical experience with:

* Highly imbalanced classification
* Fraud detection
* Data preprocessing
* Feature scaling
* Model comparison
* Precision vs. Recall trade-offs
* F1-score and PR-AUC
* ROC-AUC evaluation
* Confusion matrix analysis
* Classification threshold optimization
* Supervised vs. unsupervised fraud detection

## 🛠️ Technologies Used

* Python
* Pandas
* NumPy
* Matplotlib
* Seaborn
* Scikit-learn
* XGBoost
* Jupyter Notebook

## 📁 Repository Structure

```text
Fraud-detection/
│
├── fraud_detection.ipynb
├── README.md
└── .gitignore
```

The dataset is excluded from the repository because of its size.

## 🚀 Future Improvements

* Hyperparameter tuning of the Random Forest model
* Further threshold optimization based on business costs
* Cost-sensitive learning
* Additional imbalance-handling techniques
* Model monitoring and drift detection
* Deployment as a real-time fraud detection API

## 👩‍💻 Author

**Gayatri Arvind Gundad**

CSE Student | Machine Learning & Data Analytics Enthusiast
