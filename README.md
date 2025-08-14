
# Employee Turnover Prediction with Logistic Regression

This project aims to predict employee turnover (resignation) using a Logistic Regression model, based on the Human Resources Dataset by Rich Huebner from Kaggle. The dataset includes HR attributes such as employee demographics, status, department, performance score, salary, and more ([scribd.com](https://www.scribd.com/document/486957839/Human-Resources-Data-Set-Kaggle-pdf?utm_source=chatgpt.com)).

---

##  Dataset Overview
- The dataset was originally created as a teaching tool for HR analytics, including fields like employee number, demographics, hire/termination dates, reason for termination, department, salary, manager, performance score, and other employment details ([scribd.com](https://www.scribd.com/document/486957839/Human-Resources-Data-Set-Kaggle-pdf?utm_source=chatgpt.com)).
- It contains multiple interconnected sheets, including HR core data, salary grid, recruiting costs, and production staff metrics, enabling multi-level analysis of performance and turnover factors ([aihr.com](https://www.aihr.com/blog/hr-data-sets-people-analytics/?utm_source=chatgpt.com)).

---

##  Key Business Questions
1. **Which factors most influence employee turnover?**  
   Identifying key predictors such as job level, performance score, or days late can help HR proactively mitigate turnover risk.

2. **Are compensation levels aligned with performance?**  
   Understanding mismatch between pay and performance can guide fair reward strategies and reduce disengagement.

3. **How effective are recruiting channels?**  
   Using recruiting cost data, assessing which sources yield long-tenure, high-performing hires can optimize hiring budgets.

4. **What are common termination reasons?**  
   Analyzing trends across termination reasons (e.g., job mismatch, unsatisfactory pay, relocation) can help tailor retention programs.

---

##  Model Overview

- **Model**: Logistic Regression with L2 regularization (`penalty='l2'`, `C=1.0`, solver='liblinear')  
- **Handling Imbalance**: `class_weight='balanced'`  
- **Preprocessing**:
  - Categorical encoding with `LabelEncoder`
  - Numerical features standardized with `StandardScaler`
- **Validation**: Stratified 5-Fold Cross Validation (F1-score metric)

---

##  Evaluation Metrics
| Metric                 | Value    |
|------------------------|----------|
| Test Accuracy          | 98.41%   |
| Test F1 Score          | 97.56%   |
| CV F1 Score (mean)     | 99.39%   |

Confusion matrix indicates very few misclassifications, demonstrating both **precision and reliability** in predictions.

---

##  Feature Importance Highlights
Top influential factors include:
- Employment Status
- Employment Status ID
- Termination Reason
- Days Late in Last 30 days
- Recruitment Source

These insights can inform targeted HR strategies like tailored engagement programs, monitoring late-coming trends, and optimizing recruitment channels.

---

##  Project Structure
```
├── README.md
└── turnover_logistic.ipynb      # Main notebook with data preprocessing, modeling, and evaluation
```

---

###  About the Author
_Chantika Anasthya_
