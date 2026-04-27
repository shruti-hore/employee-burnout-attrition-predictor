# Employee Burnout & Attrition Predictor

A machine learning project that predicts whether an employee is at high risk of burnout or attrition using workplace and AI-related features.

## Dataset

Source: https://www.kaggle.com/datasets/nudratabbas/ai-worker-burnout-and-attrition-risk-dataset

- 1,500 employee records
- 21 features
- Target: attrition_risk (Low, Medium, High)

Converted into binary classification:
- 1 → High Risk
- 0 → Low / Medium Risk

---

## Problem Statement

Employee burnout and attrition are critical challenges in modern AI-driven industries. This project builds a classification model to identify high-risk employees early, allowing organizations to take preventive action.

---

## Project Pipeline

1. Data Loading  
2. Data Preprocessing  
3. Exploratory Data Analysis (EDA)  
4. Feature Selection  
5. Model Training  
6. Model Evaluation  
7. Prediction  

---

## Data Preprocessing

- Dropped `employee_id`
- Encoded categorical variables
- Converted target to binary
- Applied SMOTE to handle class imbalance
- Feature scaling using StandardScaler

---

## Models Used

### Logistic Regression (Primary)
- Simple and interpretable
- Best performance on imbalanced data

### Support Vector Machine (Secondary)
- RBF kernel
- Used for comparison

---

## Evaluation Metrics

- Precision
- Recall (primary focus)
- F1-Score
- Confusion Matrix
- ROC-AUC

---

## Results

| Metric | Logistic Regression | SVM |
|--------|---------------------|-----|
| Accuracy | 93% | 93% |
| Recall (High Risk) | 0.76 | 0.35 |
| F1-Score (High Risk) | 0.54 | 0.38 |
| ROC-AUC | ~0.89 | ~0.82 |

Logistic Regression performs significantly better in identifying high-risk employees.

---

## Key Insights

- Fear of AI replacement is the strongest predictor
- Low job satisfaction increases attrition risk
- Burnout score independently impacts risk
- Recall is more important than accuracy due to class imbalance

---

## Visualizations

- Attrition distribution
- Correlation heatmap
- Burnout vs job satisfaction
- Fear of AI vs attrition
- Feature importance

---

## Technologies Used

- Python
- pandas
- numpy
- scikit-learn
- matplotlib
- seaborn
- imbalanced-learn (SMOTE)
- Jupyter Notebook

---

## How to Run

```bash
git clone https://github.com/your-username/employee-burnout-attrition-predictor.git
cd employee-burnout-attrition-predictor
pip install -r requirements.txt
jupyter notebook
