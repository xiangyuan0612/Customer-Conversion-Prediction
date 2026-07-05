# 📊 Customer Subscription Prediction — Machine Learning Project

A machine learning project focused on predicting whether a customer will subscribe to a long-term deposit product using multiple classification models and probability threshold optimization.

> 🎯 Goal: Maximize business conversion while maintaining strong recall of potential customers.

---

## 🧠 Project Overview

This project evaluates and compares three machine learning models:

- K-Nearest Neighbors (KNN)
- Logistic Regression (LASSO)
- Decision Tree

The dataset is highly imbalanced:

- Deposit No: 89.41%
- Deposit Yes: 10.59%

To handle this, stratified sampling and threshold tuning were applied.

---

## 📊 Data Pipeline

### Dataset Split Strategy
- Total records: **3681**
- Train/Test split: **70% / 30%**
- Stratified sampling used to preserve class distribution

📌 Key challenge: class imbalance

---

## 📌 Feature Engineering

### Selected Features (Final Model Input)

**Numerical variables:**
- age
- duration
- pdays
- previous
- emp.var.rate
- cons.conf.idx
- cons.price.idx
- euribor3m
- nr.employed

**Categorical variables:**
- month
- poutcome (one-hot encoded)

---

## 🤖 Model 1 — KNN Classifier

### Model Tuning
- Optimal K = **14**

### Performance

| Metric | Value |
|--------|------|
| AUC | 0.877 |
| Sensitivity | 91.75% |
| Specificity | 79.44% |

### ROC Curve

![KNN ROC](assets/knn_roc.png)

### Confusion Matrix (Final)

![KNN CM](assets/knn_confusion.png)

---

## 🤖 Model 2 — Logistic Regression (LASSO)

### Feature Selection
- LASSO used for coefficient shrinkage and variable selection
- Optimal λ = **0.001128336**

### Performance

| Metric | Value |
|--------|------|
| AUC | **0.917 (Best)** |
| Sensitivity | 89.69% |
| Specificity | 81.14% |

### ROC Curve

![Logistic ROC](assets/logistic_roc.png)

### Confusion Matrix (Final)

![Logistic CM](assets/logistic_confusion.png)

---

## 🤖 Model 3 — Decision Tree

### Optimization
- Pruned using cross-validation
- Optimal tree size: **4 splits**

### Performance

| Metric | Value |
|--------|------|
| AUC | ~0.87 |
| Sensitivity | 74.22% |
| Specificity | 89.29% |

### Model Visualization

![Decision Tree](assets/decision_tree.png)

---

## 📈 Model Comparison Summary

| Model | AUC | Sensitivity | Specificity |
|------|-----|------------|------------|
| KNN | 0.877 | 91.75% | 79.44% |
| Logistic Regression | **0.917** | 89.69% | 81.14% |
| Decision Tree | ~0.87 | 74.22% | 89.29% |

---

## 🏆 Final Model Selection

### ✅ Winner: Logistic Regression (LASSO)

**Why it wins:**
- Highest AUC (0.917)
- Balanced sensitivity & specificity
- Strong generalization ability
- Robust under imbalanced data

---

## 📉 Key Insight (Business Value)

This model can:

- 🎯 Identify high-potential customers more accurately
- 📈 Increase marketing conversion rate
- 💰 Reduce cost of targeting low-value customers
- ⚖️ Balance recall vs precision using threshold tuning

---

## 📌 Key Techniques Used

- Stratified sampling (imbalanced data handling)
- ROC curve threshold optimization
- LASSO feature selection
- Cross-validation pruning (Decision Tree)
- Probability-based classification tuning

---

## 📷 Visual Results (From Report)

### KNN Performance
![KNN Results](assets/knn_full.png)

### Logistic Regression Performance
![Logistic Results](assets/logistic_full.png)

### Decision Tree Performance
![Tree Results](assets/tree_full.png)

---

## 📁 Project Structure (Suggested)
