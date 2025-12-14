
# 📌 Final Model Performance Summary

## ✅ 1. Class Imbalance
- The dataset is **highly imbalanced**:
  - **Non-Fraud (A)** ≈ 9,000+ claims
  - **Fraud (D)** ≈ 500 claims
- This imbalance significantly impacts model performance, especially recall for fraud detection.

---

## ✅ 2. Logistic Regression
- **Accuracy:** 69%
- **Fraud Detection (Class 1):**
  - Precision: **0.06** (very low)
  - Recall: **0.37** (better than other models)
  - F1-score: **0.11**
- **ROC-AUC:** **0.56**
- **Interpretation:**  
  Logistic Regression detects some fraud cases (recall = 37%) but misclassifies many, leading to poor precision.

---

## ✅ 3. RandomForest
- **Accuracy:** 95%
- **Fraud Detection (Class 1):**
  - Precision: **0.00**
  - Recall: **0.00**
  - F1-score: **0.00**
- **ROC-AUC:** **0.46**
- **Interpretation:**  
  RandomForest predicts almost all claims as non-fraud due to imbalance. High accuracy is misleading because it ignores minority class.

---

## ✅ 4. Gradient Boosting
- **Accuracy:** 95%
- **Fraud Detection (Class 1):**
  - Precision: **0.00**
  - Recall: **0.00**
  - F1-score: **0.00**
- **ROC-AUC:** **0.50**
- **Interpretation:**  
  Similar to RandomForest, Gradient Boosting fails to identify fraud cases.

---

## ✅ 5. ROC Curve Insights
- All models perform poorly on fraud detection:
  - Logistic Regression (Blue): **Best among three**, but still weak (AUC = 0.56).
  - RandomForest (Green): AUC = 0.46.
  - GradientBoosting (Orange): AUC = 0.50.
- **None of the models show strong discriminatory power**.

---

## ✅ Key Takeaways
- **Severe class imbalance** is the root cause of poor fraud detection.
- Accuracy is misleading; focus on **recall and AUC** for fraud class.
- Logistic Regression slightly outperforms tree-based models in this scenario.

---

### ✅ Next Steps
- Implement **advanced resampling techniques**.
- Add **hyperparameter tuning for GradientBoosting and XGBoost**.
- Explore **cost-sensitive learning** to penalize misclassification of fraud cases.

