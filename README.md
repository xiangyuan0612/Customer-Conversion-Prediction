# 📊 Customer Conversion Prediction — Machine Learning Project

A machine learning project focused on predicting whether a customer will subscribe to a long-term deposit product using classification models and ROC-based threshold optimization.

> 🎯 Objective: Maximize customer conversion while maintaining strong sensitivity and specificity.

# 🧠 1. Project Overview

This project builds and compares three classification models:

- KNN (K-Nearest Neighbors)
- Logistic Regression (LASSO)
- Decision Tree

Dataset is highly imbalanced:

- Deposit No: 89.41%
- Deposit Yes: 10.59%

# 📊 2. Data Split Strategy

- Total observations: 3681
- Train/Test split: 70% / 30%
- Stratified sampling used to maintain class distribution

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

# 🤖 4. KNN Model

## 4.1 Impact of K

📌 Optimal K selection analysis

<img width="511" height="399" alt="image" src="https://github.com/user-attachments/assets/d8ff7d2f-4bf9-4f70-9334-115a0aebc133" />


## 4.2 Initial Confusion Matrix

<img width="329" height="103" alt="image" src="https://github.com/user-attachments/assets/822a2e04-a913-4912-a0a2-5e539e21e116" />


## 4.3 Optimal Threshold

📌 ROC-based threshold tuning

![Figure 3 - KNN threshold](assets/figure_03_knn_threshold.png)

---

## 4.4 Improved Confusion Matrix

<img width="405" height="148" alt="image" src="https://github.com/user-attachments/assets/88061d8a-0c78-4ee7-a64a-1b9714ad7633" />


## 4.5 ROC Curve

<img width="560" height="448" alt="image" src="https://github.com/user-attachments/assets/4e6aed75-ca17-498a-a048-80366cb5c684" />

## 📊 KNN Performance Summary

- AUC: 0.877  
- Sensitivity: 91.75%  
- Specificity: 79.44%


# 🤖 5. Logistic Regression (LASSO)

## 5.1 Coefficient Path

📌 Effect of λ on coefficients

<img width="550" height="448" alt="image" src="https://github.com/user-attachments/assets/b7f6d1fb-7585-4444-9a45-fcf4a5b28628" />


## 5.2 Initial Confusion Matrix

<img width="559" height="159" alt="image" src="https://github.com/user-attachments/assets/0b75aa0a-66cf-4321-8de7-bd10f9a3335f" />


## 5.3 Optimal Threshold

<img width="660" height="155" alt="image" src="https://github.com/user-attachments/assets/1bd577ee-f847-416f-8d6b-27189b735934" />


## 5.4 Improved Confusion Matrix

<img width="527" height="162" alt="image" src="https://github.com/user-attachments/assets/6db8ff59-e089-4068-b3e7-e6c30c77121c" />


## 5.5 ROC Curve

<img width="533" height="425" alt="image" src="https://github.com/user-attachments/assets/5c4e1fb6-3c96-4273-80ce-7a618f1c40b4" />


## 📊 Logistic Regression Performance

- AUC: **0.917 (Best Model)**
- Sensitivity: 89.69%
- Specificity: 81.14%


# 🌳 6. Decision Tree

## 6.1 Model Selection Curve

<img width="575" height="465" alt="image" src="https://github.com/user-attachments/assets/b176b170-e46b-498d-85ff-83b8be504474" />


## 6.2 Complexity Table and Decision tree model with minimum relative error(cv)
<img width="783" height="387" alt="image" src="https://github.com/user-attachments/assets/5efac5db-4ce7-46de-aff5-4d490b8d4b5b" />


## 6.3 Confusion Matrix

<img width="641" height="203" alt="image" src="https://github.com/user-attachments/assets/968a1ecd-f40c-4b5d-93e8-e79750a3e7a4" />


## 📊 Decision Tree Performance

- AUC: ~0.87  
- Sensitivity: 74.22%  
- Specificity: 89.29%


# 📈 7. Final Model Comparison

<img width="893" height="485" alt="image" src="https://github.com/user-attachments/assets/01c42bec-d3f6-47f7-abbf-6a2e443363ea" />


| Model | AUC | Sensitivity | Specificity |
|------|-----|------------|------------|
| KNN | 0.877 | 91.75% | 79.44% |
| Logistic Regression | **0.917** | 89.69% | 81.14% |
| Decision Tree | ~0.87 | 74.22% | 89.29% |


# 🏆 8. Final Conclusion

✔ Logistic Regression (LASSO) is the best model due to:

- Highest AUC (0.917)
- Balanced sensitivity & specificity
- Strong generalization ability
- Robust performance on imbalanced dataset


# 💡 9. Business Impact

This model helps:

- 🎯 Identify high-value customers
- 📈 Improve marketing conversion rate
- 💰 Reduce marketing cost
- ⚖️ Optimize targeting strategy


# ⚙️ 10. Key Techniques

- Stratified sampling
- ROC curve threshold tuning
- LASSO feature selection
- Cross-validation pruning
- AUC-based model selection

---

# 📁 11. Project Structure
