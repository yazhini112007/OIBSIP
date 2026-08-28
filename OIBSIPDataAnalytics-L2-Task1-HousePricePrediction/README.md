# OIBSIP Task 1: House Price Prediction with Machine Learning

This project is part of the **Oasis Infobyte Internship (OIBSIP)** under the **Data Analytics Track (Level 2, Task 1)**[cite: 1, 2]. It focuses on building and evaluating regression models to predict housing prices using the Ames Housing dataset[cite: 1].

---

## 📌 Task Overview

* **Task Name:** Level 2 - Task 1: Predicting House Prices with Linear Regression[cite: 1]
* **Track:** Data Analytics[cite: 1, 2]
* **Objective:** Predict residential property prices based on various structural and locational features using regularized and unregularized linear regression models[cite: 1].

---

## 🛠 Tech Stack

* **Language:** Python 3.14+[cite: 1]
* **Environment:** Jupyter Notebook / IPykernel[cite: 1]
* **Libraries:** `scikit-learn`, `pandas`, `numpy`, `matplotlib`, `seaborn`[cite: 1]

---

## 📊 Model Evaluation & Results

We evaluated three regression models using **Root Mean Squared Error (RMSE)** and **R² Score** to analyze the effect of regularization on performance:

| Model | Root Mean Squared Error (RMSE) | R² Score |
| :--- | :--- | :--- |
| **Linear Regression** | \$83,088.77 | 0.0999 |
| **Ridge Regression** | **\$32,654.34** | **0.8610** |
| **Lasso Regression** | \$35,009.33 | 0.8402 |

### Key Takeaways
* **Linear Regression:** Suffers from severe overfitting/multicollinearity issues, achieving a poor $R^2$ score of ~0.10.
* **Ridge Regression ($L_2$ Regularization):** Delivered the best performance, significantly reducing RMSE to **\$32,654.34** and explaining **86.1%** of variance ($R^2 = 0.8610$).
* **Lasso Regression ($L_1$ Regularization):** Performed comparably ($R^2 = 0.8402$) while automatically setting non-essential feature weights to zero.

---

## 📂 Repository Structure

```text
OIBSIP/
└── DataAnalytics-L2-Task1-HousePricePrediction/
    ├── OIBSIPDataAnalytics-L2-Task1-HousePricePrediction.ipynb
    └── README.md 

How to Run
Clone the repository:

git clone [https://github.com/your-username/OIBSIP.git](https://github.com/your-username/OIBSIP.git)
cd OIBSIP/DataAnalytics-L2-Task1-HousePricePrediction

Install required packages:
pip install pandas numpy scikit-learn matplotlib seaborn jupyter

Launch the Jupyter Notebook:jupyter notebook OIBSIPDataAnalytics-L2-Task1-HousePricePrediction.ipynb