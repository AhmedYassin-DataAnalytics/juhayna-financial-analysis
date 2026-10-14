# Juhayna Financial Performance Analysis & Forecasting

**DiGiLiANS Capstone Project | Data Analytics**

## Overview

This project analyzes the quarterly financial performance of **Juhayna Food Industries (JUFO)** using financial statements, a Power BI report, and a Python machine learning workflow.

The project combines historical financial analysis and interactive reporting with time-based forecasting to support data-driven interpretation of business performance.

## Project Files

| File | Description |
|---|---|
| `JUFO_QUARTERLY_Financials(1).xlsx` | Quarterly financial statements dataset |
| `Project_Juhayna.pbix` | Interactive Power BI report |
| [Google Colab Notebook](https://colab.research.google.com/drive/1IRF2zcnDzpce7PuL_tjlXdqDtLHWb63s#scrollTo=fS_kDLhGgbEB) | Python machine learning and forecasting workflow |

> To open the Power BI report, download the `.pbix` file and open it in Power BI Desktop. The Excel and PBIX files must also be uploaded to this GitHub repository for the filenames above to work as repository files.

## Dataset

The Excel workbook contains three financial statement sheets:

- **Income Statement**
- **Balance Sheet**
- **Cash Flow**

The workbook contains quarterly periods from **Q3 2021 through Q2 2026**.

## Power BI Report

The report includes four analytical pages:

- **Overview** — summary of financial performance
- **Performance** — analysis of financial performance trends
- **Working Capital** — working capital analysis
- **Liquidity** — liquidity analysis

## Machine Learning & Forecasting

The Python workflow uses quarterly financial data to prepare a time-based dataset, evaluate regression models, and generate future estimates.

The models considered in the project workflow include:

- Linear Regression
- Decision Tree Regressor
- Random Forest Regressor

The notebook also imports Logistic Regression; because it is a classification algorithm, it should only be described as part of the final model comparison if it was actually evaluated appropriately for the target used.

### Forecasting approach

1. Prepare quarterly financial data and extract the target metric.
2. Create time-related features, including year, quarter, and a time index.
3. Train and evaluate models using historical data.
4. Compare model performance using the evaluation metrics implemented in the notebook.
5. Retrain the selected model on the available historical observations and forecast upcoming quarters.

**Forecast period:** Q3 and Q4 2026  
**Reported model result:** approximately 98.6% accuracy was noted during project development; consult the notebook for the exact metric and calculation. Forecasts are estimates, not actual reported financial results.

[**Open the Machine Learning Notebook in Google Colab →**](https://colab.research.google.com/drive/1IRF2zcnDzpce7PuL_tjlXdqDtLHWb63s#scrollTo=fS_kDLhGgbEB)

## Tools & Technologies

- Microsoft Excel
- Power BI
- Python
- Pandas
- NumPy
- Scikit-learn
- Matplotlib

## Project Workflow

**Financial Statements → Data Preparation → Financial Analysis → Power BI Reporting → Model Evaluation → Forecasting**

## Skills Demonstrated

- Financial data analysis
- Quarterly trend analysis
- KPI reporting and visualization
- Data preparation with Python
- Regression modeling and model evaluation
- Time-based forecasting
- Communicating analytical findings

## Author

**Ahmed Yassin Abdelazim** — Data Analyst

- [LinkedIn](https://linkedin.com/in/ahmedyassin-dataanalytics)
- [GitHub](https://github.com/AhmedYassin-DataAnalytics)
