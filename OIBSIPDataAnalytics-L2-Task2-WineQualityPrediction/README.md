An optimized, professional **`README.md`** tailored specifically for **Data Analytics Level 2 - Task 2: Wine Quality Prediction**.

---

# Wine Quality Prediction Analysis

## 📌 Executive Summary

This project performs an end-to-end data analytics workflow on the **Wine Quality Dataset** to analyze chemical characteristics and build predictive machine learning models for wine classification. By exploring red and white wine attributes (such as acidity, residual sugar, and alcohol levels), this project identifies key chemical drivers of quality and evaluates multiple classification models to accurately forecast wine ratings.

---

## 🛠️ Project Architecture & Tech Stack

* **Language:** Python 3.x
* **Environment:** Jupyter Notebook / Google Colab
* **Libraries & Frameworks:**
* **Data Manipulation:** `pandas`, `numpy`
* **Data Visualization:** `matplotlib`, `seaborn`
* **Machine Learning:** `scikit-learn` (`RandomForestClassifier`, `DecisionTreeClassifier`, `LogisticRegression`, `StandardScaler`, `train_test_split`)
* **Model Evaluation:** `classification_report`, `confusion_matrix`, `accuracy_score`, `roc_auc_score`



---

## 📋 Feature Checklist

* [x] **Data Ingestion & Cleaning:** Loaded raw dataset, handled missing/null values, and removed duplicate rows.
* [x] **Exploratory Data Analysis (EDA):** Evaluated distributions, feature correlations, and summary statistics across physicochemical properties.
* [x] **Feature Engineering:** Normalization/scaling of continuous attributes and encoding quality into binary/multi-class target variables.
* [x] **Model Training:** Implemented multiple machine learning algorithms including Random Forest, Decision Tree, and Logistic Regression.
* [x] **Performance Evaluation:** Evaluated models using Precision, Recall, F1-Score, Confusion Matrices, and ROC curves.
* [x] **Insights & Conclusion:** Summary of the top chemical predictors determining high vs. low wine quality.

---

## 💡 Key Findings & Insights

* **Alcohol Content:** Displays the strongest positive correlation with higher quality ratings.
* **Volatile Acidity:** Shows a distinct negative correlation; higher volatile acidity is strongly linked to lower quality ratings.
* **Sulphates & Citric Acid:** Play a crucial role in enhancing flavor balance and stability in top-tier wines.

---

## 🚀 How to Run

1. **Clone the repository:**

git clone https://github.com/YOUR_USERNAME/OIBSIP.git
cd OIBSIP/DataAnalytics-L2-WineQualityPrediction

```


2. **Install required dependencies:**
pip install pandas numpy matplotlib seaborn scikit-learn

```


3. **Execute Notebook:**
Launch Jupyter Notebook or VS Code to run `Wine_Quality_Prediction.ipynb`.

jupyter notebook