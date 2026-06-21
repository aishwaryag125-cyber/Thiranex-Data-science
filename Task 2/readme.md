# Student Success Predictive Modeling

A machine learning project designed to predict student academic outcomes (Pass/Fail) using demographic, social, and academic characteristics from the Student Performance Dataset.

## 🚀 Project Overview

This project demonstrates a complete supervised machine learning workflow, including data preprocessing, exploratory data analysis (EDA), feature engineering, model training, and performance evaluation. The goal is to identify factors that influence student success and build predictive models capable of classifying students as Pass or Fail.

---

## 🛠️ Tech Stack & Libraries

**Language:** Python

**Environment:** Jupyter Notebook / Kaggle Notebook

**Libraries Used:**

* Pandas
* NumPy
* Scikit-learn
* Matplotlib
* Seaborn

---

## 📊 Methodology & Key Features

### 1. Data Preparation & Feature Engineering

* Checked for missing values and duplicate records.
* Performed data cleaning and preprocessing.
* Converted the final grade (G3) into a binary target variable:

  * Pass (G3 ≥ 10)
  * Fail (G3 < 10)
* Applied One-Hot Encoding to categorical features.
* Split the dataset into training and testing sets using an 80:20 ratio.

### 2. Exploratory Data Analysis (EDA)

Conducted visual analysis to understand student behavior and performance patterns:

* Distribution of Final Grades
* Gender Distribution
* Study Time vs Final Grade
* Absences vs Final Grade
* Correlation Analysis

These visualizations helped identify important relationships between academic performance and student characteristics.

### 3. Machine Learning Models

The following classification algorithms were implemented:

#### Decision Tree Classifier

* Simple and interpretable baseline model.
* Useful for understanding decision paths.

#### Random Forest Classifier

* Ensemble learning algorithm.
* Reduces overfitting by combining multiple decision trees.
* Achieved the best overall performance.

---

## 📉 Model Performance

| Model         | Accuracy |
| ------------- | -------- |
| Decision Tree | 88.61%   |
| Random Forest | 92.41%   |

### Best Performing Model

**Random Forest Classifier**

* Accuracy: **92.41%**
* Demonstrated superior generalization and prediction capability.

---

## 🎨 Performance Visualizations

The project includes several evaluation plots:

### Confusion Matrix

Visualizes:

* True Positives
* True Negatives
* False Positives
* False Negatives

### ROC Curve

Measures classification performance across different thresholds.

### Feature Importance Analysis

Highlights the most influential variables affecting student outcomes.

---

## 💡 Key Insights

* Academic performance indicators significantly influence final outcomes.
* Students with higher study time generally achieve better grades.
* Increased absences tend to correlate with lower academic performance.
* Random Forest outperformed the Decision Tree model due to its ensemble learning capability.
* Early identification of at-risk students can help educators provide timely interventions.

---

## 📚 Learning Outcomes

Through this project, I gained hands-on experience in:

* Data Cleaning & Preprocessing
* Exploratory Data Analysis (EDA)
* Feature Engineering
* Supervised Machine Learning
* Model Evaluation & Validation
* Data Visualization
* Predictive Analytics
