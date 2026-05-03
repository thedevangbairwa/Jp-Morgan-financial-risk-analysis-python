\# JP Morgan Financial Risk Analysis Using Python



\## Overview

This repository contains an end-to-end financial risk and customer behavior analysis based on transactional account data. The project is designed to demonstrate practical data analysis skills including data cleaning, exploratory analysis, customer profiling, risk identification, visualization, and statistical hypothesis testing.



\---



\## Business Problem

Banks need to understand customer transaction behavior and identify early warning signs of financial risk. This project addresses the following questions:

1\. How do credits and debits behave over time across accounts?

2\. Which accounts show strong net inflow and which show heavy net outflow?

3\. Which accounts show risky patterns such as large withdrawals, unstable balances, or anomalous transactions?

4\. Does high transaction volume reliably indicate higher average balance?



\---



\## Dataset Summary

The dataset contains transaction-level records including:

\- Identifiers: TransactionID, CustomerID, AccountID

\- Categorical fields: AccountType, TransactionType, Product, Firm, Region, Manager

\- Numerical fields: TransactionAmount, AccountBalance, RiskScore, CreditRating, TenureMonths

\- Date field: TransactionDate



Transaction types observed include Deposit, Withdrawal, Payment, and Transfer.



\---



\## Tools \& Skills Used



\- \*\*Python\*\*

&#x20; - Data cleaning, transformation, and analysis



\- \*\*Pandas \& NumPy\*\*

&#x20; - Data preprocessing, aggregation, and numerical analysis



\- \*\*Matplotlib \& Seaborn\*\*

&#x20; - Data visualization and exploratory analysis



\- \*\*Jupyter Notebook\*\*

&#x20; - Interactive analysis and documentation



\- \*\*Exploratory Data Analysis (EDA)\*\*

&#x20; - Trend analysis, KPI calculation, and pattern identification



\---



\## Approach Summary

The project was completed in the following stages:

1\. Data cleaning and formatting

&#x20;  - Converted date field into a consistent datetime format

&#x20;  - Ensured financial fields were numeric and consistent

&#x20;  - Standardized categorical values to avoid grouping errors

2\. Descriptive transaction analysis

&#x20;  - Monthly and yearly summaries of credits, debits, and net transaction volume

&#x20;  - Credit versus debit trend analysis

&#x20;  - Top and bottom accounts by net inflow

&#x20;  - Dormant account detection using transaction gaps

3\. Customer profile building

&#x20;  - Activity level segmentation (High, Medium, Low) based on transaction frequency

&#x20;  - Segmentation using average balance and transaction volume

&#x20;  - Profile identification for high net inflow accounts, high frequency low balance accounts, and low/near-zero balance risk cases

4\. Financial risk identification

&#x20;  - Frequent large withdrawals detection

&#x20;  - Balance volatility measurement using standard deviation

&#x20;  - Anomaly detection using Z-score methodology

&#x20;  - Combined risk flags for suspicious or irregular behavior

5\. Visualization and exploratory analysis

&#x20;  - Trend, distribution, segmentation, and risk-focused visuals

6\. Hypothesis testing

&#x20;  - Welch’s t-test to evaluate whether high-volume accounts have higher average balances than low-volume accounts



\---



\## Key Assumptions

1\. Deposit is treated as credit (money in)

2\. Withdrawal, Payment, and Transfer are treated as debit (money out)

3\. Dormant accounts are defined as accounts with a transaction gap of 60 days or more between consecutive transactions

4\. Anomaly detection uses a Z-score threshold of absolute value greater than 3



\---



\## Results Summary

1\. Credits versus debits

&#x20;  - Debit activity consistently exceeds credit activity across time periods, resulting in net outflow for the overall portfolio.

2\. Account performance

&#x20;  - A small subset of accounts contributes disproportionately to positive net inflow.

&#x20;  - Several accounts show heavy net outflow and are candidates for monitoring.

3\. Risk signals

&#x20;  - Some accounts show large withdrawals, high balance volatility, and anomalous transaction behavior.

&#x20;  - Combining multiple indicators strengthens risk detection compared to using a single metric.

4\. Hypothesis test outcome

&#x20;  - The statistical test did not show a significant difference in average balances between high-volume and low-volume transaction accounts.

&#x20;  - Transaction volume alone should not be treated as a proxy for customer financial strength.



\---



\## Business Insights

1\. Portfolio-level behavior indicates persistent net outflow, which may represent liquidity stress in certain customer segments.

2\. High engagement does not always indicate financial stability; frequent transactions can occur alongside low average balances.

3\. Balance volatility is a strong and practical monitoring feature because it highlights unstable account behavior.

4\. Outlier transactions justify automated alerts, since extreme values occur even when most transactions are within a normal range.



\---



\## Recommendations

1\. Monitoring and controls

&#x20;  - Prioritize monitoring for accounts with high balance volatility and frequent large withdrawals.

&#x20;  - Add automated alerts for anomalous transaction amounts identified through statistical thresholds.

2\. Customer engagement strategy

&#x20;  - Separate engagement-based segmentation from stability-based segmentation.

&#x20;  - High-frequency low-balance accounts should receive proactive support and monitoring due to higher stress risk.

3\. Customer value assessment

&#x20;  - Do not use transaction volume alone to classify customer value.

&#x20;  - Use a combination of net inflow, average balance, and balance stability for value and risk classification.



\---



\## Repository Structure

```

Jp-Morgan-financial-risk-analysis-python/

│

├── README.md

│

├── data/

│   ├── jp\_morgan.csv

│   └── jp\_morgan\_cleaned.csv

│

├── notebooks/

│   └── Financial\_Risk\_Analysis.ipynb

│

├── reports/

│   └── Financial\_Risk\_Analysis\_Report.pdf

│

└── visuals/

&#x20;   ├── credit\_vs\_debit\_trend.png

&#x20;   ├── net\_transaction\_trend.png

&#x20;   ├── transaction\_amount\_distribution.png

&#x20;   ├── account\_balance\_distribution.png

&#x20;   ├── balance\_volatility\_distribution.png

&#x20;   ├── balance\_vs\_volume\_scatter.png

&#x20;   └── activity\_level\_distribution.png



```



\## Screenshots

Credit vs Debit Trend

!\[Credit vs Debit Trend](visuals/credit\_vs\_debit\_trend.png)



Net Transaction Trend

!\[Net Transaction Trend](visuals/net\_transaction\_trend.png)



Activity Level Distribution

!\[Activity Level Distribution](visuals/activity\_level\_distribution.png)



Transaction Amount Distribution

!\[Transaction Amount Distribution](visuals/transaction\_amount\_distribution.png)



Balance Volatility Distribution

!\[Balance Volatility Distribution](visuals/balance\_volatility\_distribution.png)



Balance vs Transaction Volume

!\[Balance vs Volume](visuals/balance\_vs\_volume\_scatter.png)



\---



\## Project Artifacts

Notebook:

notebooks/Financial\_Risk\_Analysis.ipynb



Report:

reports/Financial\_Risk\_Analysis\_Report.pdf



Video Link:

Add your public video link inside the PDF report and optionally here:



https://www.loom.com/share/221cbfd770e5409082f6af21ed8d0135



\---



\## How to Run Locally

1\. Install Python 3.9 or higher

2\. Install dependencies:

&#x20;  pip install pandas numpy matplotlib scipy

3\. Open and run the notebook:

&#x20;  notebooks/Financial\_Risk\_Analysis.ipynb



\---



\## Notes for Reviewers

The notebook contains the full workflow, including data cleaning, analysis outputs, visualizations, and statistical testing. The PDF report provides a structured summary and includes the video link for the project walkthrough.



\---



\## Author

Dheeraj Marmat

Data Analyst Portfolio Project

