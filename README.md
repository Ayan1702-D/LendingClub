# LendingClub Anomaly Detection & Risk Analysis

This project uses Machine Learning (Isolation Forest) to identify high-risk anomalies within the LendingClub dataset (2007-2018). By identifying these "edge cases," we can capture significant financial losses that traditional credit scoring might miss.


# Dataset Information
The raw data for this project is sourced from the LendingClub Dataset (2007-2018) on Kaggle.

Source: [https://www.kaggle.com/datasets/wordsforthewise/lending-club/data]

Accepted Dataset: 22,60,699 records.

Rejected Dataset: 2,76,48,741 records.

Note on Data Quality: During analysis, it was discovered that 59.0% of rejected anomalies contained impossible DTI values (>100), suggesting significant data entry or fraud issues at the application stage.


# Key Findings & Business Impact

High Risk Detection: Anomalies have a 17.8% default rate, which is 1.42x higher than the normal rate (12.6%).

Financial Impact: The model successfully flagged $448M in total bad loan dollars.

Data Quality Discovery: Found that 59.0% of rejected anomalies contained impossible Debt-to-Income (DTI) values (>100).

Fraud Detection: Identified a "High Income/High Loan" segment representing 23.9% of anomalies, suggesting potential income verification issues.


# Risk Segments Identified

Low FICO (29.7%): Traditional credit risk already identified by scoring.

High Income/High Loan (23.9%): Average income of $136k vs. $75k normal; requires income verification.

High Public Records (16.9%): Applicants with bankruptcies or legal issues; highest correlation with anomalies.


# Project Status
[x] Data Preprocessing: Handled 4M+ records and capped DTI values.

[x] Anomaly Detection: Trained Isolation Forest model (stored in models/).

[x] Risk Analysis: Compared accepted vs. rejected loan patterns.

[ ] Next Phase: Develop a real-time FastAPI for loan scoring.

[ ] Next Phase: Create a Dashboard for risk monitoring.
