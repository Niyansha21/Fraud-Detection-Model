# 💳 Financial Fraud Detection System

This project implements a proactive fraud detection system using the PaySim synthetic dataset. It uses advanced feature engineering and machine learning to detect fraudulent mobile money transactions with high accuracy and sensitivity.

---

## 🚀 Key Achievements

- Recall: **89%** (Detected 1,468 out of 1,643 fraud cases)
- ROC-AUC: **0.94** (Excellent class separation)
- Feature Innovation: "Accounting Logic" features contributed **57%** of total predictive power

---

## 🛠️ Project Workflow

### 1. Data Cleaning & Feature Engineering

#### Outlier Handling
- Used IQR Capping (Upper Bound)
- Preserved high-value fraud cases
- Removed mathematical noise

#### Feature Engineering
- Created:
  - Orig_Balance_Error
  - Dest_Balance_Error

#### Accounting Logic
In a valid transaction:

OldBalance - NewBalance - Amount = 0

Deviations from zero indicate possible fraud or account manipulation.

---

### 2. Machine Learning Model

#### Algorithm
- Random Forest Classifier

#### Class Imbalance Handling
- class_weight = "balanced"
- Stratified train-test split

This helps the model learn rare fraud patterns (only ~0.1%).

#### Feature Selection
- Based on domain knowledge
- Verified using feature importance

---

## 📊 Performance Summary

| Metric          | Result  | Description                              |
|-----------------|---------|------------------------------------------|
| Recall          | 89%     | Detects most fraud cases                 |
| Precision       | 5%      | High sensitivity, more alerts            |
| True Positives  | 1,468   | Correctly detected fraud                |
| False Positives | 29,695  | False alarms                             |

---

## 📈 Top Predictive Features

| Feature            | Importance |
|--------------------|------------|
| Orig_Balance_Error | 57.1%      |
| Transaction Amount | 21.0%      |
| Time Step          | 12.3%      |

Key Insights:
- Accounting errors are the strongest fraud indicator
- High-value transfers have higher risk
- Fraud shows time-based patterns

---

## 🛡️ Future Recommendations

### Infrastructure Improvement
- Add real-time velocity checks
- Validate balances at API level

### Threshold Optimization
- Increase decision threshold from 0.5 to 0.8+
- Reduce false positives by ~50%

### Security Enhancement
- Enable Multi-Factor Authentication (2FA/MFA)
- Trigger for high Orig_Balance_Error cases

---

## 📂 Tech Stack

- Python  
- Pandas, NumPy  
- Scikit-learn  
- Matplotlib / Seaborn  
- Jupyter Notebook  

---

## 📌 Dataset

- PaySim: Financial Mobile Money Simulator
- Synthetic dataset based on real-world transactions

---

## 📜 Conclusion

This project shows how domain-based feature engineering combined with machine learning can improve fraud detection systems. Accounting logic plays a key role in detecting fraudulent behavior early.

---

## 👨‍💻 Author

Developed by [Niyansha Dubey]
