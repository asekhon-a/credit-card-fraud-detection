Credit Card Fraud Detection and Transaction Risk Analytics
An end-to-end data analytics project investigating credit card fraud patterns, transaction risk indicators, and financial impact using Python and Microsoft Power BI.

Project Overview
Credit card fraud represents a small proportion of overall transaction activity but can create significant financial exposure.

This project analyses 100,000 credit card transactions to identify patterns associated with fraudulent activity and communicate the findings through an interactive Power BI report and fraud-monitoring dashboard.

The project covers data understanding, data cleaning, exploratory data analysis, fraud-risk analysis, financial-impact analysis, and business intelligence reporting.

Business Questions
The analysis aims to answer the following questions:

What proportion of transactions are fraudulent?
How does fraud activity change over time?
Which transaction channels have the highest observed fraud rates?
Which fraud types occur most frequently?
Which merchant categories show the highest fraud rates and financial losses?
Are international and high-risk-country transactions associated with higher fraud rates?
How does authentication behaviour differ between legitimate and fraudulent transactions?
Which behavioural characteristics are associated with fraudulent transactions?
When during the day are elevated fraud rates observed?
Where is fraud creating the greatest recorded financial exposure?
Tools & Technologies
Python
pandas
NumPy
Matplotlib
Seaborn
Jupyter Notebook
Microsoft Power BI Desktop
Power Query
DAX
Power BI Service
Visual Studio Code
Git & GitHub
Project Workflow
The project follows a structured analytical workflow.

1. Data Understanding
Inspected dataset dimensions, variables, data types, missing values, duplicates, and fraud-class distribution.
Investigated the analytical roles of transaction, customer, behavioural, geographic, authentication, and fraud-related variables.
2. Data Cleaning and Preparation
Converted transaction timestamps to datetime.
Investigated missing browser values.
Identified missing browser values as structurally associated with ATM and In-store transactions.
Represented these values as Not Applicable.
Validated binary and categorical variables.
Assessed numerical ranges.
Identified fraud_type and fraud_amount_lost as potential target-leakage variables for future predictive modelling.
Created additional temporal fields for analysis and Power BI.
3. Exploratory Data Analysis
Analysed:

Fraud volume and fraud rate
Recorded financial loss
Transaction channels
Transaction hours
Fraud types
Merchant categories
Geographic risk indicators
Authentication behaviour
Transaction velocity
Spending behaviour
Previous declines and chargebacks
4. Power BI Reporting
Developed a four-page interactive Power BI report.
Published the report to Power BI Service.
Created an executive fraud-monitoring dashboard using selected report visuals.
Key Findings
Fraudulent transactions represent approximately 2.06% of the 100,000 analysed transactions.
The dataset contains 2,055 fraudulent transactions.
Recorded fraud loss totals approximately 279.84K.
Fraudulent transaction value totals approximately 349.21K.
Online transactions show the highest observed channel fraud rate at approximately 3.18%.
Card-Not-Present fraud is the most frequently observed fraud type, with 1,054 cases.
Elevated fraud rates are observed during the early-morning period, with an observed fraud rate of approximately 11.30% at 03:00.
Transactions associated with the high-risk-country indicator show an observed fraud rate of approximately 11.05%.
International transactions show a higher observed fraud rate than domestic transactions.
Online Retail has the highest observed merchant-category fraud rate.
Travel & Airlines produces the greatest recorded fraud loss among the merchant categories examined.
Card presence, chip usage, and PIN usage occur less frequently among fraudulent transactions in this dataset.
Fraud rate, fraud frequency, and recorded financial loss do not necessarily peak within the same segments or time periods.
Power BI Report
The Power BI report contains four analytical pages.

1. Fraud Overview
Provides an executive summary of transaction activity, fraud volume, fraud rate, financial exposure, monthly fraud trends, and transaction-channel risk.

Fraud Overview

2. Fraud Patterns
Examines fraud behaviour across transaction hours, fraud types, and merchant categories.

Fraud Patterns

3. Risk Indicators
Examines geographic and authentication indicators associated with fraudulent transactions.

Risk Indicators

4. Financial Impact
Examines fraudulent transaction value, recorded fraud loss, monthly financial impact, transaction-channel exposure, and merchant-category losses.

Financial Impact

Power BI Monitoring Dashboard
A single-page executive fraud-monitoring dashboard was created in Power BI Service by pinning selected visuals from the published report.

Power BI Monitoring Dashboard

Limitations
The analysis identifies associations within the supplied dataset and does not establish causal relationships.
Elevated fraud rates within a transaction channel, geographic group, time period, or behavioural category should not be interpreted as deterministic fraud rules.
The dataset is highly imbalanced, with fraudulent transactions accounting for approximately 2.06% of observations.
fraud_type and fraud_amount_lost contain outcome information and should not be used directly as predictors of is_fraud in a future machine-learning model.
Some variables may be related to one another. For example, authentication behaviour naturally differs between Online and In-store transaction channels.
Results should therefore be interpreted using multiple transaction characteristics rather than isolated indicators.
Repository Structure
credit-card-fraud-detection/
│
├── data/
│   └── README.md
│
├── images/
│   ├── fraud_overview.png
│   ├── fraud_patterns.png
│   ├── risk_indicators.png
│   ├── financial_impact.png
│   └── power_bi_dashboard.png
│
├── notebooks/
│   ├── 01_data_understanding.ipynb
│   ├── 02_data_cleaning.ipynb
│   └── 03_exploratory_data_analysis.ipynb
│
├── powerbi/
│   └── Credit_Card_Fraud_Detection_Dashboard.pbix
│
├── .gitignore
├── requirements.ent.

## Reproducing the Analysis

1. Clone this repository.
2. Create a Python virtual environment.
3. Install the required Python libraries:

```bash
pip install -r requirements.txt
```

4. Obtain the source dataset and place it inside the `data/raw/` folder.
5. Run the notebooks in the following order:
   - `01_data_understanding.ipynb`
   - `02_data_cleaning.ipynb`
   - `03_exploratory_data_analysis.ipynb`
6. Open `powerbi/Credit_Card_Fraud_Detection_Dashboard.pbix` in Microsoft Power BI Desktop to explore the interactive report.

## Future Improvements

Future extensions could include:

- Developing fraud-classification models using Logistic Regression, Decision Trees, Random Forests, and gradient-boosting methods.
- Evaluating model performance using precision, recall, F1-score, confusion matrices, ROC-AUC, and Precision-Recall AUC.
- Comparing different strategies for handling class imbalance.
- Introducing model explainability and feature-importance analysis.
- Developing transaction-level fraud-risk scores for operational monitoring.

## Author

**Nomsa Mchunu**

Aspiring Data Analyst | Python | Power BI | Data Analytics