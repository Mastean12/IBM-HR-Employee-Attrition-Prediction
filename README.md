# IBM HR Employee Attrition Prediction

## Overview

Employee attrition is a major challenge for organizations as it leads to increased recruitment costs, productivity loss, and knowledge gaps. This project applies Machine Learning techniques to predict employee attrition using the IBM HR Analytics Employee Attrition dataset.

The objective is to identify employees who are likely to leave the organization and uncover the key factors driving attrition, enabling HR teams to make data-driven retention decisions.

---

## Dataset Information

**Dataset:** IBM HR Analytics Employee Attrition Dataset

* Total Records: 1,470 employees
* Features: 35 employee-related attributes
* Target Variable: `Attrition` (Yes/No)

### Sample Features

* Age
* Monthly Income
* Overtime
* Job Role
* Job Satisfaction
* Work-Life Balance
* Distance From Home
* Years At Company
* Total Working Years

---

## Project Workflow

### 1. Exploratory Data Analysis (EDA)

Performed detailed exploratory analysis to understand:

* Dataset structure
* Feature distributions
* Employee attrition patterns
* Relationships between employee characteristics and attrition

### 2. Data Preprocessing

* Verified missing values
* Encoded categorical variables using One-Hot Encoding
* Prepared feature matrix and target variable
* Split data into training and testing sets

### 3. Machine Learning Models

The following classification models were implemented and evaluated:

* Decision Tree Classifier
* Random Forest Classifier
* Tuned Random Forest (GridSearchCV)
* XGBoost Classifier

### 4. Model Evaluation

Models were evaluated using:

* Accuracy
* Precision
* Recall
* F1 Score
* Confusion Matrix
* ROC Curve
* AUC Score

### 5. Model Optimization

Advanced optimization techniques included:

* Hyperparameter Tuning using GridSearchCV
* ROC-AUC Analysis
* Threshold Tuning

---

## Model Performance

| Model                      | Accuracy | Precision | Recall | F1 Score |
| -------------------------- | -------- | --------- | ------ | -------- |
| Decision Tree              | 80.27%   | 38.78%    | 40.43% | 39.58%   |
| Random Forest              | 82.99%   | 36.36%    | 8.51%  | 13.79%   |
| Tuned Random Forest        | 83.33%   | 41.67%    | 10.64% | 16.95%   |
| XGBoost                    | 86.05%   | 71.43%    | 21.28% | 32.79%   |
| XGBoost (Threshold = 0.30) | 85.03%   | 54.55%    | 38.30% | 45.00%   |

---

## ROC-AUC Analysis

### XGBoost AUC Score

**AUC = 0.782**

This indicates good model capability in distinguishing employees likely to leave from those likely to stay.

---

## Key Business Insights

### Overtime Increases Attrition Risk

Employees working overtime showed a significantly higher likelihood of leaving the company.

### Monthly Income Matters

Employees with lower monthly income were more likely to leave compared to higher-paid employees.

### Younger Employees Leave More Frequently

Attrition rates were generally higher among younger employees.

### Employee Tenure Influences Retention

Employees with fewer years at the company were more likely to leave.

### Class Imbalance Challenge

Only approximately 16% of employees left the company, making attrition prediction an imbalanced classification problem.

---

## Feature Importance

The most influential features identified by the models included:

1. Monthly Income
2. Total Working Years
3. Age
4. Distance From Home
5. Overtime
6. Years At Company
7. Percent Salary Hike
8. Work-Life Balance

---

## Threshold Optimization

The default XGBoost threshold of 0.50 resulted in high precision but low recall.

By lowering the classification threshold to 0.30:

* Recall increased from **21.28%** to **38.30%**
* F1 Score improved from **32.79%** to **45.00%**
* More employees at risk of attrition were successfully identified

This demonstrates the importance of optimizing machine learning models according to business objectives rather than relying solely on accuracy.

---

## Technologies Used

* Python
* Pandas
* NumPy
* Matplotlib
* Seaborn
* Scikit-Learn
* XGBoost
* Jupyter Notebook

---

## Future Improvements

Potential enhancements for future versions:

* SMOTE for class imbalance handling
* LightGBM implementation
* SHAP explainability analysis
* Ensemble stacking techniques
* Streamlit deployment
* Interactive HR analytics dashboard

---

## Repository Structure

```text
IBM-HR-Employee-Attrition-Prediction/
│
├── IBM_HR_Attrition.ipynb
├── WA_Fn-UseC_-HR-Employee-Attrition.csv
├── README.md
├── requirements.txt
└── images/
    ├── attrition_distribution.png
    ├── overtime_vs_attrition.png
    ├── roc_curve.png
    └── feature_importance.png
```

---

## Installation

```bash
git clone https://github.com/yourusername/IBM-HR-Employee-Attrition-Prediction.git
cd IBM-HR-Employee-Attrition-Prediction

pip install -r requirements.txt
```

---

## Author

**Stephen Mariga Ndegwa**

Data Analyst | Machine Learning Engineer | AI Engineer

GitHub: https://github.com/DataExpert0112

---

### Project Highlights

✔ Exploratory Data Analysis (EDA)

✔ Feature Engineering

✔ Decision Tree Classification

✔ Random Forest Classification

✔ Hyperparameter Tuning

✔ XGBoost Modeling

✔ ROC Curve & AUC Analysis

✔ Threshold Optimization

✔ Business Insight Generation

✔ HR Analytics Application
