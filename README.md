

---

#  Credit Card Fraud Detection using Support Vector Machines (SVM)

## Overview

This repository contains a complete workflow for detecting fraudulent credit card transactions using **Support Vector Machines (SVM)**. The project demonstrates essential steps in a machine learning pipeline—including data exploration, preprocessing, model building, and evaluation—applied to a highly imbalanced real-world dataset.

The dataset used is the popular **Credit Card Fraud Detection** dataset from Kaggle, consisting of anonymized features derived from PCA transformations for privacy protection.

---

##  Project Structure

```
├── Credit Card Fraud Detection.ipynb   # Main analysis and modeling notebook
├── README.md                            # Project documentation
└── /data (optional)                     # Dataset (if included)
```

---

##  Dataset Description

* **Source:** Kaggle – Credit Card Fraud Detection
* **Records:** 284,807 transactions
* **Timeframe:** Two days of credit card transactions from European cardholders
* **Fraud Ratio:** Fraudulent transactions = **0.172%** (highly imbalanced)
* **Features:**

  * `V1`–`V28`: PCA-transformed features for confidentiality
  * `Time`: Seconds elapsed between transactions
  * `Amount`: Transaction amount
  * `Class`: Target variable (1 = fraud, 0 = legitimate)

---

##  Data Preprocessing

Steps performed in the notebook include:

* Removing the `Time` feature to reduce noise
* Standardizing numerical features for SVM performance
* Handling imbalanced data through:

  * Evaluation metrics robust to imbalance (Precision, Recall, F1-score)
  * Use of probability outputs from the SVM model
* Train/test split for model validation

---

##  Model Development

The project uses **Support Vector Machines (SVM)** for binary classification due to its effectiveness at handling high-dimensional data.

Key steps:

* Model training using the RBF kernel
* Hyperparameter selection (C, gamma)
* Class probability computation using `probability=True`

---

##  Model Evaluation

Metrics and evaluations include:


* **ROC Curve & AUC Score**
* Probability analysis of fraudulent cases

The model demonstrates how SVMs can identify rare fraudulent activity despite extreme class imbalance.

---




---

## Key Takeaways

* Fraud detection requires careful handling of imbalanced datasets.
* PCA-transformed features can still yield strong predictive results.
* SVMs provide solid baseline performance for fraud detection tasks.
* Evaluation metrics beyond accuracy are essential for skewed datasets.

---

## Future Improvements

* Implement SMOTE or other oversampling techniques
* Experiment with alternative models (Random Forest, XGBoost)
* Tune hyperparameters using GridSearchCV
* Deploy as an API for real-time fraud detection

---



---

