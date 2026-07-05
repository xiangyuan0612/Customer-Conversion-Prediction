# 📊 Customer Subscription Prediction — Machine Learning Project

A machine learning project focused on predicting whether a customer will subscribe to a long-term deposit product using classification models and ROC-based threshold optimization.

> 🎯 Objective: Maximize customer conversion while maintaining strong sensitivity and specificity.

---

# 🧠 1. Project Overview

This project builds and compares three classification models:

- KNN (K-Nearest Neighbors)
- Logistic Regression (LASSO)
- Decision Tree

Dataset is highly imbalanced:

- Deposit No: 89.41%
- Deposit Yes: 10.59%

---

# 📊 2. Data Split Strategy

- Total observations: 3681
- Train/Test split: 70% / 30%
- Stratified sampling used to maintain class distribution

---

# 📌 3. Feature Selection

### Numerical features
- age
- duration
- pdays
- previous
- emp.var.rate
- cons.conf.idx
- cons.price.idx
- euribor3m
- nr.employed

### Categorical features
- month
- poutcome (one-hot encoded)

---

# 🤖 4. KNN Model

## 4.1 Impact of K

📌 Optimal K selection analysis

![Figure 1 - KNN K selection](assets/figure_01_knn_k_selection.png)

---

## 4.2 Initial Confusion Matrix

![Figure 2 - KNN confusion matrix](assets/figure_02_knn_confusion.png)

---

## 4.3 Optimal Threshold

📌 ROC-based threshold tuning

![Figure 3 - KNN threshold](assets/figure_03_knn_threshold.png)

---

## 4.4 Improved Confusion Matrix

![Figure 4 - KNN improved confusion matrix](assets/figure_04_knn_improved_cm.png)

---

## 4.5 ROC Curve

![Figure 5 - KNN ROC](assets/figure_05_knn_roc.png)

---

## 📊 KNN Performance Summary

- AUC: 0.877  
- Sensitivity: 91.75%  
- Specificity: 79.44%

---

# 🤖 5. Logistic Regression (LASSO)

## 5.1 Coefficient Path

📌 Effect of λ on coefficients

![Figure 6 - LASSO coefficients](assets/figure_06_lasso_coefficients.png)

---

## 5.2 Initial Confusion Matrix

![Figure 7 - Logistic initial CM](assets/figure_07_logistic_confusion.png)

---

## 5.3 Optimal Threshold

![Figure 8 - Logistic threshold](assets/figure_08_logistic_threshold.png)

---

## 5.4 Improved Confusion Matrix

![Figure 9 - Logistic improved CM](assets/figure_09_logistic_improved_cm.png)

---

## 5.5 ROC Curve

![Figure 10 - Logistic ROC](assets/figure_10_logistic_roc.png)

---

## 📊 Logistic Regression Performance

- AUC: **0.917 (Best Model)**
- Sensitivity: 89.69%
- Specificity: 81.14%

---

# 🌳 6. Decision Tree

## 6.1 Model Selection Curve

![Figure 11 - Tree error curve](assets/figure_11_tree_error_curve.png)

---

## 6.2 Complexity Table

![Figure 12 - Tree complexity table](assets/figure_12_tree_complexity_table.png)

---

## 6.3 Final Tree Structure

![Figure 12b - Decision tree](assets/decision_tree_structure.png)

---

## 6.4 Confusion Matrix

![Figure 13 - Tree confusion matrix](assets/figure_13_tree_confusion_matrix.png)

---

## 📊 Decision Tree Performance

- AUC: ~0.87  
- Sensitivity: 74.22%  
- Specificity: 89.29%

---

# 📈 7. Final Model Comparison

![Figure 14 - Model comparison ROC](assets/figure_14_model_comparison_roc.png)

---

| Model | AUC | Sensitivity | Specificity |
|------|-----|------------|------------|
| KNN | 0.877 | 91.75% | 79.44% |
| Logistic Regression | **0.917** | 89.69% | 81.14% |
| Decision Tree | ~0.87 | 74.22% | 89.29% |

---

# 🏆 8. Final Conclusion

✔ Logistic Regression (LASSO) is the best model due to:

- Highest AUC (0.917)
- Balanced sensitivity & specificity
- Strong generalization ability
- Robust performance on imbalanced dataset

---

# 💡 9. Business Impact

This model helps:

- 🎯 Identify high-value customers
- 📈 Improve marketing conversion rate
- 💰 Reduce marketing cost
- ⚖️ Optimize targeting strategy

---

# ⚙️ 10. Key Techniques

- Stratified sampling
- ROC curve threshold tuning
- LASSO feature selection
- Cross-validation pruning
- AUC-based model selection

---

# 📁 11. Project Structure
