# Fraud Detection Analysis

## 📌 Executive Summary

This project delivers a comprehensive data analytics and machine learning solution for detecting fraudulent transactions within heavily imbalanced financial datasets. By performing thorough Exploratory Data Analysis (EDA), applying advanced class imbalance mitigation techniques, and training robust classification algorithms, this workflow accurately flags potential fraud while minimizing false positives.

---

## 🛠️ Project Architecture & Tech Stack

* **Language:** Python 3.x
* **Environment:** Jupyter Notebook / Google Colab


* **Libraries & Frameworks:**
* **Data Manipulation:** `pandas`, `numpy`
* **Data Visualization:** `matplotlib`, `seaborn`
* **Imbalanced Learning:** `imbalanced-learn` (`SMOTE`, `RandomUnderSampler`)
* **Machine Learning:** `scikit-learn` (`RandomForestClassifier`, `LogisticRegression`, `StandardScaler`, `train_test_split`)
* **Model Evaluation:** `classification_report`, `confusion_matrix`, `precision_recall_curve`, `roc_auc_score`



---

## 📋 Feature Checklist

* [x] **Data Loading & Preprocessing:** Ingested the financial transaction dataset and examined data types, missing values, and missingness patterns.


* [x] **Exploratory Data Analysis (EDA):** Visualized severe class imbalance and analyzed feature distributions across legitimate vs. fraudulent transactions.


* [x] **Class Imbalance Strategy:** Applied oversampling (SMOTE) and undersampling techniques to prevent model bias towards majority class samples.


* [x] **Feature Scaling:** Normalized highly skewed transaction amounts and features using `StandardScaler` / `RobustScaler`.
* [x] **Model Implementation:** Trained classification algorithms including Logistic Regression and Random Forest.


* [x] **Comprehensive Evaluation:** Prioritized Precision, Recall, Precision-Recall AUC, and Confusion Matrix metrics over simple accuracy.


* [x] **Business Insights & Mitigation:** Outlined actionable recommendations to streamline fraud monitoring and minimize false alarm costs.

---

## 💡 Key Findings & Insights

* **Metric Selection:** Standard accuracy is misleading due to severe class imbalance; Precision-Recall AUC and Recall are critical for capturing actual fraud.


* **Feature Skew:** Transaction amounts and frequency exhibit high variance and extreme outliers between normal and fraudulent behavior.
* **Resampling Impact:** Applying SMOTE drastically improves model recall, ensuring the majority of fraudulent activities are flagged effectively.

---

## 🚀 How to Run

1. **Clone the repository:**

git clone https://github.com/YOUR_USERNAME/OIBSIP.git
cd OIBSIP/DataAnalytics-L2-FraudDetection

```


2. **Install required dependencies:**
pip install pandas numpy matplotlib seaborn scikit-learn imbalanced-learn

```


3. **Execute Notebook:**
Launch Jupyter Notebook or VS Code to run `Fraud_Detection.ipynb`.

jupyter notebook

```