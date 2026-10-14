# Juhayna Financial Performance Analysis

A financial analytics project focused on reviewing Juhayna Food Industries (JUFO) quarterly performance using Python, Excel, and Power BI. The project explores profitability, financial position, and cash-flow trends to support data-driven business analysis.

## Project Overview

The analysis uses quarterly financial statement data to examine how Juhayna's performance changes over time. It combines financial statement analysis, a Power BI dashboard, and a Python-based machine-learning experiment that compares regression models to forecast quarterly revenue. It covers three core financial statements:

- **Income Statement** — revenue, cost of revenue, gross profit, operating income, net income, and profitability margins.
- **Balance Sheet** — assets, liabilities, equity, working capital, cash, inventory, and debt.
- **Cash Flow Statement** — operating, investing, and financing cash flows, capital expenditures, and free cash flow.

The provided dataset contains quarterly periods from **September 2021 through June 2026**.

## Objectives

- Track quarterly revenue and profit performance.
- Review gross, operating, and net profit margins.
- Compare balance-sheet indicators, including inventory, working capital, and debt.
- Examine operating cash flow and free cash flow trends.
- Present financial information in a dashboard to make trends easier to explore.

## Tools & Technologies

- **Python** — data analysis and preparation.
- **Pandas & NumPy** — tabular data manipulation and numerical analysis.
- **Matplotlib** — data visualization.
- **scikit-learn** — regression models and model comparison.
- **Excel / openpyxl** — financial statement data source and workbook reading.
- **Power BI** — interactive financial dashboard and reporting.

> The tools listed above reflect the project materials and stated workflow. Add any additional libraries or techniques only if they are used in the final notebook.

## Dataset

The Excel workbook, `JUFO_QUARTERLY_Financials.xlsx`, includes the following sheets:

| Sheet | Main coverage |
|---|---|
| Income Statement | Revenue, costs, profit, margins, earnings, and EPS |
| Balance Sheet | Assets, liabilities, equity, cash, inventory, and debt |
| Cash Flow | Operating, investing, and financing cash flows |

The source workbook presents the financial values as supplied. Confirm the reporting currency and units from the original data source before interpreting or comparing absolute amounts.

## Workflow

1. Review the quarterly financial statements and available fields.
2. Prepare the data for analysis and comparison across reporting periods.
3. Explore profitability, liquidity, leverage, and cash-flow indicators.
4. Build visual summaries in Power BI.
5. Use the resulting trends to identify areas that may warrant further business investigation.

## Machine Learning: Quarterly Revenue Forecasting

The notebook builds a time-based forecasting workflow for quarterly revenue using the `Income Statement` sheet. It extracts the `Revenue` row, parses reporting-period dates, sorts the observations chronologically, and creates year, quarter, and time-index fields.

### Features and target

- **Target (`Y`):** `Revenue`
- **Features (`X`):** `Time_Index` plus quarter indicator variables (`Q1`, `Q2`, `Q3`, and `Q4`)
- **Forecast horizon:** Q3 2026 and Q4 2026

### Models compared

| Model | Configuration |
|---|---|
| Linear Regression | `LinearRegression()` |
| Decision Tree Regressor | `random_state=42` |
| Random Forest Regressor | `n_estimators=200`, `random_state=42` |

### Time-based evaluation

The notebook evaluates the models using two chronological tests:

1. **Test 1 — 2025:** train on periods through 2024 and test on 2025.
2. **Test 2 — Q1–Q2 2026:** train on periods through 2025 and test on the first two quarters of 2026.

For each test, it calculates the absolute percentage error for each test observation and reports `100 - mean(absolute percentage error)` as **Accuracy (%)**. In regression forecasting, this is more accurately described as a *MAPE-derived score* rather than conventional classification accuracy; it can be negative if percentage errors exceed 100%. The notebook then averages this score across tests to select the model with the highest mean score.

After model selection, the chosen model is refit on all available observations before forecasting Q3 and Q4 2026. The notebook plots the historical revenue trend and an actual-versus-forecast chart. Forecasts are model estimates, not reported financial results.

> **Interpretation note:** the current model uses only time index and quarter indicators. It does not include explanatory business drivers such as volume, pricing, inflation, costs, or market conditions. With a relatively small quarterly dataset, forecasts should be treated as exploratory and interpreted alongside the actual financial statements.

## Example Observations

Based on the latest period available in the supplied workbook (**June 2026**):

- Reported revenue: **9,078**.
- Reported net income: **712.91**.
- Reported year-over-year revenue growth: **23.31%**.
- Reported gross margin: **23.73%**.
- Reported operating margin: **12.39%**.
- Reported free cash flow: **-213.82**.

These figures are reproduced from the supplied workbook; the currency and scale should be verified against the source before drawing conclusions from absolute values. They are descriptive observations, not investment advice.

## Project Files

- `JUFO_QUARTERLY_Financials.xlsx` — quarterly financial statements.
- `Project_Juhayna.pbix` — Power BI report file.
- [Google Colab Notebook](https://colab.research.google.com/drive/1IRF2zcnDzpce7PuL_tjlXdqDtLHWb63s) — Python analysis notebook. Access may require permission to the original Google Drive file.

## How to Explore

1. Open the Google Colab notebook and run the cells in order.
2. Review the Excel workbook to inspect the source financial statements.
3. Open `Project_Juhayna.pbix` in Power BI Desktop to explore the report.

## Skills Demonstrated

Financial statement analysis · Data preparation · Exploratory data analysis (EDA) · Regression modeling · Time-based model evaluation · Revenue forecasting · Data visualization · Power BI reporting · Python-based analysis · Business-focused interpretation of financial trends

## Notes

This is an analytical portfolio project based on the supplied financial data. Any conclusions should be interpreted in the context of the dataset's definitions, reporting period, currency, and units.
