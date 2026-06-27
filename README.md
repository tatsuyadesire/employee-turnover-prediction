# Employee Turnover Prediction using Machine Learning

Machine Learning pipeline developed to predict employee turnover using the IBM HR Analytics dataset. The project covers the complete data science workflow, from exploratory data analysis to explainable AI and prediction reporting.

---

## Project Overview

Employee turnover represents a major challenge for organizations, directly impacting productivity, recruitment costs and knowledge retention.

This project applies supervised Machine Learning algorithms to estimate the probability of employee attrition and identify the factors that most influence turnover decisions.

The entire workflow was developed in Python following a structured pipeline suitable for portfolio presentation.

---

## Objectives

* Perform Exploratory Data Analysis (EDA)
* Prepare the dataset for Machine Learning
* Compare multiple classification algorithms
* Optimize the selected model
* Explain model decisions using SHAP
* Generate employee turnover risk predictions

---

## Dataset

**IBM HR Analytics Employee Attrition & Performance**

* 1,470 employees
* 35 original features
* Binary classification problem
* Target:

  * Yes → Employee left the company
  * No → Employee remained

---

## Technologies

* Python
* Pandas
* NumPy
* Matplotlib
* Scikit-Learn
* XGBoost
* SHAP
* Jupyter Notebook

---

## Project Structure

```text
turnover_prediction/

├── data/
│   ├── raw/
│   └── processed/
│
├── models/
│
├── notebooks/
│   ├── 01_data_loading.ipynb
│   ├── 02_eda.ipynb
│   ├── 03_modeling.ipynb
│   ├── 04_explainability.ipynb
│   └── 05_reporting.ipynb
│
├── outputs/
│
├── README.md
└── .gitignore
```

---

## Workflow

1. Data Loading
2. Exploratory Data Analysis
3. Data Cleaning
4. Feature Engineering
5. One-Hot Encoding
6. Train/Test Split
7. Logistic Regression
8. Random Forest
9. XGBoost
10. Model Optimization
11. SHAP Explainability
12. Prediction Report

---

## Model Comparison

| Model                |   Accuracy |  Precision |     Recall |   F1 Score |
| -------------------- | ---------: | ---------: | ---------: | ---------: |
| Logistic Regression  |     86.05% |     68.75% |     23.40% |     34.92% |
| Random Forest        |     83.33% |     41.67% |     10.64% |     16.95% |
| XGBoost              |     86.05% |     65.00% |     27.66% |     38.81% |
| **Balanced XGBoost** | **85.37%** | **57.14%** | **34.04%** | **42.67%** |

Although the balanced XGBoost presented a slightly lower Accuracy, it achieved the best balance between Precision and Recall, making it the selected model for the project.

---

## Explainability

Model explainability was implemented using **SHAP (SHapley Additive Explanations)**.

The analysis identified the most influential features for employee turnover prediction, including:

* OverTime
* Monthly Income
* Stock Option Level
* Age
* Distance From Home
* Number of Companies Worked
* Environment Satisfaction
* Business Travel Frequency

A global SHAP summary plot and individual prediction explanations were generated.

---

## Outputs

The project generates:

* Descriptive statistics
* Feature importance ranking
* Model comparison table
* SHAP summary visualization
* Executive report
* Employee turnover risk ranking

---

## Key Results

Selected model:

**Balanced XGBoost**

Performance:

* Accuracy: **85.37%**
* Precision: **57.14%**
* Recall: **34.04%**
* F1-Score: **42.67%**
* ROC-AUC: **75.14%**

---

## Installation

Clone this repository:

```bash
git clone https://github.com/tatsuyadesire/employee-turnover-prediction.git
```

Navigate to the project folder:

```bash
cd employee-turnover-prediction
```

Install the required dependencies:

```bash
pip install -r requirements.txt
```

Open the notebooks or run the Python scripts to reproduce the analysis.

---

## Author

**TatsuyaDesire**

Data Science Student | Data Analytics | Machine Learning | Python | VBA | Excel Automation

---

## License

This project was developed for educational and portfolio purposes.
