# LendingClub Analytics

### Analyze Lending Club loan data.
#### 1. Perform data visualization and exploratory data analysis on the loan data from Lending Club company.
1. The loans applied by potential borrowers, the amount issued to the borrowers and the amount funded by investors are similarly distributed, meaning that it is most likely that qualified borrowers are going to get the loan they had applied for. Most of the loans issued were in the range of 10,000 to 20,000 USD.
2. Loans issues was increasing year by year as the Lending Club exploded, most loans were issued in the year of 2015.
3. Define the loan whose loan_condition is 'Charged Off', 'Default', 'Does not meet the credit policy. Status:Charged Off', 'In Grace Period', 'Late (16-30 days)' or 'Late (31-120 days)' as 'Bad Loan'.
7.6% of total loans are bad loans but there are current loans which have the risk becoming bad loans. Loan business of Lending Club has been growing up rapidly since 2012 and the riskmanagement became omre effective after 2013.
4. From the run chart of loans issued by region for the period from June, 2007 through December, 2015, we can find out that SouthEast , West and NorthEast regions had the highest amount lof loans issued.(Possible due to local economic.)
5. The regions of the West and SouthEast had a higher percentage in most of the b "bad" loan statuses.The NorthEast region had a higher percentage in Grace Period and Does not meet Credit Policy loan status.
6. Classify the borrowers by annual income as below: 
Low income category: Borrowers that have an annual income lower or equal to 100,000 usd. 
Medium income category: Borrowers that have an annual income higher than 100,000 usd but lower or equal to 200,000 usd. 
High income category: Borrowers that have an annual income higher than 200,000 usd. 
Borrowers having higher annual income took higher loan amounts than people with lower income and always had a average lower interest rate on their loans. 
Loans that were borrowed by the Low income category had a slightly higher change of becoming a bad loan.
Borrowers with High and Medium annual incomes had a longer employment length than people with lower incomes.
7. The borrowers with lower credit score or applied for a larger amount of money would receive a higher interest rate. The average interest rate of bad loans was higher than the one of the good loan, borrowers with lower credit grade would receive a higher rate which put pressure on them in return and the default became more likely.
8. Main factors that causes for a loan to be considered a "Bad Loan": low annual income, high debt to income, high interest rates, low grade
9. Mortgage was the variable from the home ownership column that used the highest amount borrowed within loans that were considered to be bad.
10. The Midwest and West regions had the most defaults.
11. Loans that have a high interest rate(above 13.23%) are more likely to become a bad loan.
Loans that have a longer maturity date (60 months) are more likely to be a bad loan.
12. The reasons for clients to apply for a loan contribute to a "higher" risk. People that apply for educational and small business purposed tend to have a higher risk of being a bad loan. The reason that clients applied the most for a loan was to consolidate debt.Clients applied less for educational purposes for all three income categories.

#### 2. Build a model to predict whether a loan will default.
Define the loan whose loan_condition is 'Charged Off', 'Default', 'Does not meet the credit policy. Status:Charged Off', 'In Grace Period', 'Late (16-30 days)' or 'Late (31-120 days)' as 'Bad Loan', 'Fully Paid' and 'Current' as 'Good Loan'. Build  Logistic Regression and XGBoost model to predict whether a loan has the risk of default.
Accuracy of the XGBoost model with the best performance is 0.92.

#### 3. Select features for monitoring current loan status --- the risk of defaulting in the future.
dti(debt to income), revol_util(The borrower’s revolving line utilization rate (the amount of the credit line used relative to total credit available).), annual_inc,(annual income) ， rov_bal(The borrower’s revolving balance (amount unpaid at the end of the credit card billing cycle).), total_acc(The total number of credit lines currently in the borrower's credit file), mths_since_last_delinq (The number of months since the borrower's last delinquency.), inq_last_6mths(The number of inquiries in past 6 months (excluding auto and mortgage inquiries)).
