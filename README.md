Based on an inspection of financial_data.csv, this dataset contains financial, demographic, and behavioral profile records for 17,908 individual loan applicants.

The main purpose of this dataset is to analyze applicant characteristics and build predictive risk profiles to determine whether a user will complete the onboarding funnel—specifically, whether they will digitally sign (e_signed) their loan agreement.

Dataset Overview
Total Records: 17,908 rows

Total Attributes: 21 columns

Target Feature: e_signed (Binary: 1 if the applicant signed, 0 if they dropped out or were rejected)

Detailed Column Descriptions
The 21 features in this dataset can be broken down into four distinct categories:

1. Identification & Demographics
entry_id (Integer): A unique identification number assigned to each applicant. (This is a database key and should be dropped during machine learning model training).

age (Integer): The age of the applicant. The dataset spans working-age adults ranging from 18 to 96 years old, with an average age of 43.

home_owner (Binary): Indicates whether the applicant owns their home (1) or rents/lives elsewhere (0).

2. Employment & Financial Stability
income (Integer): The monthly or annual verified income of the applicant. The average income in this cohort sits around $3,657.

pay_schedule (Categorical): How frequently the applicant receives their paycheck. It contains four unique variations:

bi-weekly (Most common, accounting for over 10,700 applicants)

weekly

semi-monthly

monthly

years_employed (Integer): The number of full years the applicant has been at their current job.

months_employed (Integer): The remaining number of months the applicant has been at their current job (used alongside years_employed to calculate total precise tenure).

current_address_year (Integer): The number of years the applicant has resided at their current street address, acting as a proxy for residential stability.

3. Banking & Credit Behavior
personal_account_y (Integer): The number of full years the applicant has held their primary personal bank account.

personal_account_m (Integer): The remaining number of months the applicant has held their primary personal bank account.

has_debt (Binary): Indicates if the applicant has an open, outstanding debt or credit balance (1) or not (0).

amount_requested (Integer): The principal loan amount requested by the user. Requests range from a minimum of $350 to a maximum of $10,200, with an average request of roughly $950.

inquiries_last_month (Integer): The number of hard credit checks or inquiries pulled against the applicant’s credit file in the past 30 days. High numbers generally signal credit-seeking urgency.

4. Risk Models & Performance Indicators
risk_score (Integer): The primary comprehensive internal credit risk assessment rating calculated for the application. Higher values reflect different internal weighting tiers.

risk_score_2 through risk_score_5 (Float): Alternative, secondary mathematical risk sub-matrices. These scores are normalized decimals (mostly ranging between 0 and 1) representing individual credit attributes like repayment likelihood, macro fraud vectors, or behavioral trends.

ext_quality_score & ext_quality_score_2 (Float): Third-party quality and creditworthiness grades pulled from external consumer reporting bureaus.

e_signed (Binary): The target variable. It records whether the applicant signed the contract digitally (1) or walked away/failed verification (0). Roughly 53.8% of the records in this dataset successfully e-signed.
