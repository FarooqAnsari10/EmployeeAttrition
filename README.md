# Employee Attrition Prediction

A complete end-to-end data analytics and machine learning project that predicts employee attrition using the IBM HR Analytics dataset. Built as a submission for the **IBM SkillsBuild Data Analytics with AI Academic Internship Program** conducted by BharatCares in association with AICTE.

---

## Short Description

This project analyses the IBM HR Analytics Employee Attrition dataset to understand what drives employees to leave a company and builds a **Random Forest classifier** to predict which employees are at risk of attrition. The notebook walks through data cleaning, exploratory data analysis (EDA), feature engineering, model building, and evaluation — concluding with actionable HR recommendations.

---

## Dataset

**IBM HR Analytics Employee Attrition & Performance**  
Source: [https://www.kaggle.com/datasets/pavansubhasht/ibm-hr-analytics-attrition-dataset](https://www.kaggle.com/datasets/pavansubhasht/ibm-hr-analytics-attrition-dataset)

- **1,470 rows** × **35 columns**
- Target variable: `Attrition` (Yes / No)
- Originally published by IBM data scientists

Place the downloaded file as `employee_attrition.csv` in the same directory as the notebook before running.

---

## Technologies Used

| Tool / Library | Purpose |
|---|---|
| Python 3.9+ | Core programming language |
| pandas | Data loading, cleaning, manipulation |
| numpy | Numerical operations |
| matplotlib | Visualisation (plots, charts) |
| seaborn | Statistical visualisations |
| scikit-learn | ML models, preprocessing, evaluation |
| Jupyter Notebook / JupyterLab | Interactive notebook environment |

---

## Project Structure

```
IBM-Internship-Project/
│
├── Farooq_EmployeeAttrition.ipynb   ← Main Jupyter Notebook (run this)
├── Farooq_ProjectReport.docx        ← Project report (Word document)
├── employee_attrition.csv           ← Dataset (must be in this folder)
├── requirements.txt                 ← Python dependencies
└── README.md                        ← This file
```

After running the notebook, these plot images are also saved:
- `plot_attrition_distribution.png`
- `plot_attrition_by_department.png`
- `plot_attrition_overtime.png`
- `plot_correlation_heatmap.png`
- `plot_age_distribution.png`
- `plot_income_vs_attrition.png`
- `plot_confusion_matrix.png`
- `plot_feature_importance.png`
- `plot_roc_curve.png`

---

## Setup Instructions

**1. Clone or download this project folder.**

**2. Ensure `employee_attrition.csv` is in the project root** (same directory as the notebook).

**3. Install dependencies:**

```bash
pip install -r requirements.txt
```

> It is recommended to use a virtual environment:
> ```bash
> python -m venv venv
> venv\Scripts\activate        # Windows
> source venv/bin/activate     # macOS / Linux
> pip install -r requirements.txt
> ```

---

## How to Run

Open the notebook in Jupyter:

```bash
jupyter notebook Farooq_EmployeeAttrition.ipynb
```

Or in JupyterLab:

```bash
jupyter lab Farooq_EmployeeAttrition.ipynb
```

Then select **Kernel → Restart & Run All** to execute all cells from top to bottom.

The notebook will automatically load `employee_attrition.csv` from the same directory.

---

## Notebook Sections

| # | Section | Description |
|---|---------|-------------|
| 1 | Import & Load | Libraries, load CSV, display first 5 rows |
| 2 | Data Exploration | Shape, data types, missing values, statistics |
| 3 | Data Cleaning | Drop constants, encode target & categoricals |
| 4 | EDA | 6 visualisations: distribution, department, overtime, heatmap, age, income |
| 5 | Feature Engineering | TenureBucket, IncomePerYear, SatisfactionScore |
| 6 | Model Building | Random Forest + Logistic Regression, accuracy comparison |
| 7 | Model Evaluation | Classification report, confusion matrix, feature importance, ROC curve |
| 8 | Conclusion | Key findings + 4 actionable HR recommendations |

---

## Key Results

| Metric | Random Forest | Logistic Regression |
|--------|:---:|:---:|
| Accuracy | ~87% | ~76% |
| ROC-AUC | ~0.83 | ~0.79 |
| Recall (Attrition) | ~0.70 | ~0.68 |

**Top attrition drivers identified:**
1. **OverTime** — employees working overtime leave at ~3× the rate
2. **MonthlyIncome** — employees who left earned ~40% less on average
3. **Age / Tenure** — younger and early-tenure employees are highest risk
4. **JobSatisfaction** — low satisfaction is a reliable leading indicator
5. **Department** — Sales has the highest absolute attrition count

---

## Author

**Farooq**  
IBM SkillsBuild Data Analytics with AI Academic Internship Program  
Conducted by BharatCares in association with AICTE
