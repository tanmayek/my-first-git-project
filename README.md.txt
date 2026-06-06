# Fraud Transaction Detection using SQL and Power BI

## Project Summary

I built this project to understand how fraud patterns can be detected using SQL rules and Power BI visuals. The dataset contains more than 6 million financial transactions. My main goal was to find which transaction types, amounts, and balance patterns were linked with fraud.

## Tools Used

- PostgreSQL
- SQL
- Power BI
- GitHub

## What I Did

- Loaded the transaction dataset into PostgreSQL
- Checked total transaction count and fraud count
- Analyzed fraud by transaction type
- Compared fraud count vs fraud rate
- Tested amount-based fraud thresholds
- Used CTEs and CASE statements to classify risk
- Used ROW_NUMBER() to rank high-value transactions
- Created a rule-based risk score
- Built a Power BI dashboard to show the results

## Main Findings

- The dataset had 6,362,620 transactions.
- Only 8,213 transactions were fraud, so the fraud rate was about 0.13%.
- Fraud appeared mainly in TRANSFER and CASH_OUT transactions.
- TRANSFER had the highest fraud rate even though CASH_OUT had slightly more fraud cases.
- Many fraud transactions drained the sender's account balance.
- A simple amount threshold alone created too many alerts.
- Combining transaction type, amount, and balance-drain behavior gave a better fraud risk score.

## Dashboard

The Power BI dashboard includes:

- Total transactions
- Total fraud transactions
- Fraud rate
- Fraud count by transaction type
- Fraud rate by transaction type
- Average transaction amount by type
- Balance drain pattern
- Fraud count by risk score

![Dashboard](dashboard.png)

## Files

- `fraud_detection.sql` - SQL queries used for analysis
- `Fraud_Detection_Dashboard.pbix` - Power BI dashboard file
- `dashboard.png` - dashboard screenshot
- `README.md` - project documentation

## Power BI File

The PBIX file exceeds GitHub's web upload size limit. The dashboard screenshot and SQL queries are included in this repository.

## What I Learned

This project helped me understand that fraud detection is not just about finding high transaction amounts. A better approach is to combine multiple signals like transaction type, amount, and balance movement. I also learned how SQL can be used to create rule-based fraud scoring before building a dashboard.