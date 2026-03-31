# ❤️ AI/ML Engineering Internship — Task 3: Heart Disease Prediction

![Python](https://img.shields.io/badge/Python-3.8+-blue?logo=python)
![Scikit-Learn](https://img.shields.io/badge/Scikit--Learn-1.0+-orange?logo=scikit-learn)
![Jupyter](https://img.shields.io/badge/Jupyter-Notebook-orange?logo=jupyter)
![Status](https://img.shields.io/badge/Status-Completed-brightgreen)

---

## 📌 Task Objective

The goal of this task is to **predict whether a patient has heart disease or not** using clinical medical data.  
This is a **binary classification problem** where the model predicts:
- `0` → No Heart Disease
- `1` → Heart Disease Present

The task involves complete ML pipeline: data loading, EDA, preprocessing, model training, and evaluation.

---

## 📊 Dataset Used

| Property        | Details                                      |
|-----------------|----------------------------------------------|
| **Source**      | Kaggle — `data855/heart-disease`             |
| **Loaded via**  | `kagglehub` library                          |
| **Format**      | CSV                                          |
| **Target**      | `target` (0 = No Disease, 1 = Heart Disease) |
| **Split**       | 80% Train / 20% Test (stratified)            |
| **Preprocessing**| Missing values filled with median, duplicates removed, StandardScaler applied |

### Key Features Used

| Feature   | Description                        |
|-----------|------------------------------------|
| `age`     | Age of the patient                 |
| `cp`      | Chest pain type (0–3)              |
| `thalach` | Maximum heart rate achieved        |
| `chol`    | Serum cholesterol (mg/dl)          |
| `trestbps`| Resting blood pressure             |
| `fbs`     | Fasting blood sugar > 120 mg/dl    |
| `restecg` | Resting ECG results                |
| `exang`   | Exercise induced angina            |
| `oldpeak` | ST depression induced by exercise  |
| `slope`   | Slope of peak exercise ST segment  |
| `ca`      | Number of major vessels (0–3)      |
| `thal`    | Thalassemia type                   |

---

## 🧠 Models Applied

### 1. 📈 Logistic Regression
- Max iterations: `1000`
- Features scaled with `StandardScaler`
- Outputs probability scores for ROC-AUC calculation

### 2. 🌳 Decision Tree Classifier
- Max depth: `5` (to avoid overfitting)
- Uses raw (unscaled) features
- Provides Gini-based feature importance

---

## 📈 Key Results and Findings

### Model Performance Summary

| Model               | Accuracy | ROC-AUC |
|---------------------|----------|---------|
| Logistic Regression | ~85%+    | ~0.90+  |
| Decision Tree       | ~80%+    | ~0.85+  |

> 📝 *Exact values depend on dataset version — run the notebook to see precise metrics.*

### Key Findings

- ✅ **Logistic Regression** outperformed Decision Tree on both Accuracy and ROC-AUC
- ✅ **Top predictive features**: `thalach` (max heart rate), `cp` (chest pain type), `ca` (major vessels)
- ✅ **Chest pain type** showed strong correlation with heart disease presence
- ✅ **Higher max heart rate** was associated with higher risk of heart disease
- 📊 **Correlation heatmap** revealed meaningful relationships between features and target
- ⚠️ **Decision Tree** tends to overfit without depth limiting — `max_depth=5` helped generalize

---

## 📊 Visualizations Included

| Plot | Description |
|------|-------------|
| 🍩 Target Distribution (Donut) | Class balance between disease / no disease |
| 📊 Age Distribution | Age spread by heart disease status |
| 🔵 Max Heart Rate vs Age | Scatter plot grouped by target |
| 📊 Chest Pain Type vs Target | Bar chart of chest pain types |
| 🌡️ Correlation Heatmap | Feature-to-feature correlation matrix |
| 📦 Cholesterol Boxplot | Cholesterol levels by disease status |
| 🔲 Confusion Matrices | LR & DT prediction accuracy breakdown |
| 📈 ROC Curve Comparison | AUC comparison of both models |
| 📊 Feature Importance | LR coefficients & DT Gini importance |

---

## 🗂️ Project Structure

```
📦 AI-ML-Internship-Tasks/
├── 📓 AI_ML_Engineering_Internship_Tasks_3.ipynb   ← Main notebook
├── 📁 Visualization_Images/                         ← All plots as JPG
└── 📄 README.md                                     ← This file
```

---

## ⚙️ How to Run

### Prerequisites
```bash
pip install kagglehub scikit-learn matplotlib seaborn pandas numpy
```

### Steps
1. Clone this repository
2. Open the Jupyter Notebook:
   ```bash
   jupyter notebook AI_ML_Engineering_Internship_Tasks_3.ipynb
   ```
3. Run all cells from top to bottom
4. Dataset will auto-download via `kagglehub`

---

## 🛠️ Technologies Used

- **Python 3.8+**
- **Jupyter Notebook**
- `kagglehub` — Dataset download
- `scikit-learn` — ML models (LogisticRegression, DecisionTreeClassifier)
- `pandas` / `numpy` — Data manipulation
- `matplotlib` / `seaborn` — Visualization

---

## 👤 Author

**[Your Name Here]**  
AI/ML Engineering Intern  
📧 your.email@example.com  
🔗 [LinkedIn](https://linkedin.com) | [GitHub](https://github.com)

---

*This project was completed as part of an AI/ML Engineering Internship program.*
