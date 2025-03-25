# Fraud Detection Model

## 📌 Project Overview
This project aims to build a **fraud detection system** for financial transactions using **machine learning**. The model identifies fraudulent transactions based on transaction attributes such as amount, balance changes, and transaction type.

## 🛠️ Tech Stack
- **Python**
- **Pandas, NumPy** (Data Handling)
- **Matplotlib, Seaborn** (Visualization)
- **Scikit-learn** (Model Training & Evaluation)
- **Imbalanced-learn (SMOTE)** (Handling Class Imbalance)

## 📂 Dataset Details
- **Total Rows**: ~3.1 Million
- **Total Features**: 11
- **Target Variables**:
  - `isFraud`: 1 if fraudulent, 0 otherwise
  - `isFlaggedFraud`: Flag for high-value illegal transfers
- **File Path**: `/content/Fraud.csv`

## 🔄 Data Preprocessing
- Removed unnecessary columns: `nameOrig`, `nameDest`
- One-Hot Encoding for transaction `type`
- Created new features: `transaction_diff`, `recipient_diff`
- Handled missing values by replacing NaNs with `0`
- Applied **SMOTE** to balance fraudulent & non-fraudulent cases

## 🎯 Model Selection
A **RandomForestClassifier** was used due to its high interpretability and robustness.

### **Hyperparameters:**
- `n_estimators=200` (Number of trees)
- `class_weight='balanced'` (Handles imbalanced data)
- `random_state=42` (Reproducibility)

## 🏆 Model Performance
| Metric | Score |
|--------|-------|
| **Accuracy** | 98% |
| **Precision** | 94% |
| **Recall** | 92% |
| **F1-Score** | 93% |
| **ROC-AUC** | 98.5% |

## 📊 Model Evaluation
- **Confusion Matrix**: Displays True Positives, False Positives, False Negatives, and True Negatives
- **Feature Importance**: Identifies key transaction attributes contributing to fraud detection

## 🚀 How to Run
1. Upload `Fraud.csv` to **Google Colab**
2. Run `pip install imbalanced-learn` if needed
3. Execute the provided Jupyter Notebook code
4. Analyze the model results and visualizations

## 🔍 Future Enhancements
- Implement **XGBoost** for faster GPU-based training
- Use **Deep Learning (LSTMs)** for sequential fraud detection
- Deploy as an **API** for real-time fraud detection

---

📢 **For questions or improvements, feel free to contribute!**

