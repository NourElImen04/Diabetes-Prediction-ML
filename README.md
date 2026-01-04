# 🩸 Diabetes Prediction System

### 🧠 First AI Project | GDG Club
**Supervised by:** Tesnime Ellabou Ellabou

---

## 🔬 Project Overview
This repository hosts my first Machine Learning project: a **Diabetes Prediction Application**. 
Using **Python** and **Scikit-Learn**, I built a model that analyzes medical features (Glucose, BMI, Age, etc.) from the *Pima Indians Diabetes Dataset* to predict whether a patient is at risk.

## 🎯 Goal
The objective was to design an AI-powered tool that could support medical decision-making, prioritizing **patient safety** by minimizing false negatives (missed diagnoses).

## 🛠 Technical Stack
* **Language:** Python 🐍
* **Libraries:** Scikit-Learn, Pandas, NumPy, Matplotlib, Seaborn.
* **Models:** Random Forest Classifier & Logistic Regression.

## ⚙️ Methodology & Key Learnings

### 1. Data Preprocessing
* **Cleaning:** Handled missing values (zeros in biological columns) using Mean Imputation.
* **Normalization:** Applied `StandardScaler` to put all features on the same scale.
* **Leakage Prevention:** Strictly fit the scaler on *Training* data only, then transformed *Test* data.

### 2. Model Optimization
* **Handling Imbalance:** The dataset had far more healthy patients than diabetic ones. I used `class_weight='balanced'` and Stratified Splitting to address this.
* **Recall Priority:** Instead of chasing "Accuracy", I optimized the model for **Recall** (Sensitivity). By adjusting the decision threshold to **0.30**, I ensured the model catches more positive cases.
* **Overfitting Correction:** Initially, the Random Forest model was overfitting (100% Train vs 74% Test). I regularized it by limiting tree depth (`max_depth=5`), resulting in a much more robust model.

## 📊 Results
* **ROC-AUC Score:** 0.81 (Excellent discrimination capability).
* **Recall:** Optimized to ~0.80 to ensure safety.
* **Key Insight:** The model identified **Glucose Level** and **BMI** as the most critical risk factors.

---

### 🚀 Future Improvements
* Testing more advanced imputation methods (KNN Imputer).
* Deploying the model via a web interface (Streamlit).

_This project marks the beginning of my journey in AI & Machine Learning!_ 🚀
