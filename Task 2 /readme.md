# Student Success Predictive Modeling

A machine learning project built to predict student academic outcomes (Pass/Fail) based on demographic, social, and academic features from the **Student Performance Dataset**.

## 🚀 Project Overview
This project explores supervised machine learning workflows, progressing from initial data cleaning to deploying tree-based classifiers. The primary objective is to identify key risk factors influencing student performance and evaluate model predictions using multiple classification metrics.

---

## 🛠️ Tech Stack & Libraries
* **Language:** Python
* **Environment:** Kaggle Notebooks
* **Libraries:** `pandas`, `numpy`, `scikit-learn`, `matplotlib`, `seaborn`

---

## 📊 Methodology & Key Features

### 1. Data Pipeline & Feature Engineering
* Checked for missing entries (`data.isnull().sum()`) to ensure absolute data integrity.
* Converted the final evaluation grade (`G3`) into a binary classification target: **Pass** ($G3 \ge 10$) or **Fail** ($G3 < 10$).
* Dropped original target columns to prevent data leakage and applied One-Hot Encoding (`pd.get_dummies(drop_first=True)`) to transform categorical variables smoothly.
* Partitioned data using an 80/20 train/test split strategy for model verification.

### 2. Evaluated Classifiers
* **Decision Tree Classifier:** Implemented as an interpretable baseline model.
* **Random Forest Classifier:** Deployed as a robust ensemble model to minimize variance and combat overfitting.

---

## 📉 Experiments & Performance Analysis

This project splits the analytical approach into two separate scenarios to capture different predictive signals:

### Scenario A: Including Academic Progress Indicators (With G1 & G2)
* **Objective:** Predict final outcomes utilizing early-term progress metrics.
* **Random Forest Accuracy:** **~92.4%**
* **Area Under Curve (AUC):** **0.95** (Indicating excellent discriminative power).
* **Key Finding:** Previous academic marks ($G1$ and $G2$) overwhelmingly dominate feature importance rankings.

### Scenario B: Purely Environmental & Lifestyle Predictors (Without G1 & G2)
* **Objective:** Gauge predictive accuracy using only demographic, home environment, and lifestyle data.
* **Random Forest Accuracy:** **~65.8%**
* **Key Finding:** Eliminating academic indicators revealed that **school absences**, **past class failures**, and **student age** represent the strongest behavioral markers impacting student outcomes.

---

## 🎨 Performance Visualizations Included
The pipeline generates three primary validation plots:
1. **Confusion Matrix (Random Forest):** Visualizes precise distributions of True Positives, True Negatives, False Positives, and False Negatives.
2. **ROC Curve:** Maps the False Positive Rate against the True Positive Rate, proving the overall classification strength (AUC = 0.95).
3. **Feature Importance Charts:** Graphically contrasts how feature impact shifts dramatically once direct academic history is extracted.

---

## 💡 Core Insights
* While early grades remain the most statistically accurate way to predict final outcomes, behavioral data holds distinct predictive utility. 
* Identifying features like elevated **absences** and prior **failures** can serve as an automated, early-intervention signaling system for educators to assist at-risk students before final terms conclude.
