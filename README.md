#  Telco Customer Churn Prediction using XGBoost

This project uses machine learning to predict whether a telecom customer will churn or not based on their service usage and account information.


# Problem Statement

Churn prediction helps telecom companies retain customers by identifying who is likely to leave their service. This project builds a classification model using XGBoost, a powerful ensemble ML algorithm, on a real-world Telco dataset.


# Dataset

- Source: [Telco Customer Churn](https://www.kaggle.com/datasets/blastchar/telco-customer-churn)
- Rows: 7,043
- Target:  Churn  (Yes/No)
- Features: Demographic info, subscription types, internet & service usage, billing, contract details


# Data Cleaning

- Removed rows where TotalCharges  was empty
- Converted `TotalCharges` to numeric
- Replaced  "No internet service" and `"No phone service"  with "No" for consistency
- Dropped  customerID (no predictive value)

---

#Data Preprocessing

- Applied LabelEncoder to all categorical features
- Scaled all numeric features
- Train-test split: 80% training, 20% testing


# Model

- Algorithm: XGBoost Classifier
- Evaluation Metric: Accuracy, Precision, Recall, F1-score
- Trained using: Scikit-learn + XGBoost


# Results

| Metric     | Value      |
|------------|------------|
| Accuracy   | 77.6%      |
| Precision (No Churn) | 83% |
| Precision (Churn)    | 60% |
| Recall (Churn)       | 49% |
| F1 Score (Churn)     | 54% |

- The model performs well on identifying non-churners, and reasonably on churners (common for business-class imbalanced data).
- With further tuning or sampling (like SMOTE), performance on churners can improve.

---

#Visualization

- Confusion Matrix heatmap (Seaborn)
- Shows true positives, false positives, etc.


# Tools & Libraries

- Python
- Pandas, NumPy
- Scikit-learn
- XGBoost
- Seaborn, Matplotlib


# Author

Abhishek Darsan H 
 Data Science Enthusiast | AI & Analytics Student  
[LinkedIn](https://www.linkedin.com/in/abhishek-darsan-h-551399274)

---

# Key Skills Demonstrated

- Real-world dataset analysis
- End-to-end machine learning workflow
- Data cleaning & encoding
- XGBoost modeling
- Model evaluation and communication


# Future Work

- Try SMOTE or class weighting to improve churn recall
- Compare with Logistic Regression, Random Forest, etc.
- Deploy using Streamlit or Flask for interactive use

