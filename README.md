# 🩺 Diabetes Prediction System

A Machine Learning project that predicts whether a patient is diabetic or non-diabetic based on 8 medical diagnostic measurements, using a Support Vector Machine (SVM) classifier.

---

## 📌 Project Overview

Early detection of diabetes can significantly improve patient outcomes. This project trains an SVM model on the PIMA Indian Diabetes dataset and builds a simple prediction system that classifies a new patient as **Diabetic** or **Not Diabetic** based on their medical data.

**Key improvement over basic ML projects:** This model applies `StandardScaler` before training — which is essential for SVM performance since the algorithm is sensitive to feature magnitude.

---

## 📊 Dataset

**File:** `diabetes.csv`  
**Source:** PIMA Indian Diabetes Dataset — National Institute of Diabetes and Digestive and Kidney Diseases

| Property | Value |
|---|---|
| Total Samples | 768 |
| Non-Diabetic (0) | 500 patients |
| Diabetic (1) | 268 patients |
| Features | 8 medical measurements |
| Train / Test Split | 80% / 20% (stratified) |

### Features

| Feature | Description |
|---|---|
| Pregnancies | Number of times pregnant |
| Glucose | Plasma glucose concentration |
| BloodPressure | Diastolic blood pressure (mm Hg) |
| SkinThickness | Triceps skinfold thickness (mm) |
| Insulin | 2-hour serum insulin |
| BMI | Body mass index |
| DiabetesPedigreeFunction | Diabetes likelihood based on family history |
| Age | Age of the patient |

---

## 📈 Results

| Metric | Score |
|---|---|
| Training Accuracy | 79.64% |
| Test Accuracy | 75.32% |

The ~4% gap between training and test accuracy indicates the model generalizes well without significant overfitting.

---

## 🛠️ Tech Stack

- Python 3.x
- NumPy
- Pandas
- Scikit-learn (SVM, StandardScaler, train_test_split, accuracy_score)

---

## 🚀 How to Run

1. **Clone the repository**
   ```bash
   git clone https://github.com/AliSufyaan/diabetes-prediction.git
   cd diabetes-prediction
   ```

2. **Install dependencies**
   ```bash
   pip install numpy pandas scikit-learn jupyter
   ```

3. **Run the notebook**
   ```bash
   jupyter notebook Diabatic_Prediction.ipynb
   ```

---

## 📁 Project Structure

```
diabetes-prediction/
├── Diabatic_Prediction.ipynb    # Main notebook
├── diabetes.csv                 # Dataset
└── README.md                    # You are here
```

---

## ⚠️ Limitations

- Dataset limited to female Pima Indian patients — may not generalize broadly
- Several features contain 0 values (e.g. Glucose=0, BMI=0) which are medically impossible — no imputation applied
- Only accuracy reported — precision, recall and F1-score would give a fuller picture for a medical use case

---

## 🧠 What I Learned

- Why feature scaling (StandardScaler) is essential before training SVM models
- How SVM finds an optimal decision boundary in high-dimensional feature space
- Stratified train-test splitting to handle class imbalance
- Building an end-to-end prediction pipeline from raw input to classification output

---

## 📚 Reference

- Dataset: [Kaggle PIMA Indian Diabetes Dataset](https://www.kaggle.com/datasets/uciml/pima-indians-diabetes-database)
- Originally from the UCI Machine Learning Repository
