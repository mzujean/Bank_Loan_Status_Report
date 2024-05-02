-- Database creation 
CREATE DATABASE bank_loan;


 -- Total Loaned Amount
SELECT SUM(current_loan_amount) AS Total_Loan_Amount 
FROM bank_loan_status;

/* What is the distribution of loan statuses among customers? */
SELECT loan_status, COUNT(*) AS Total_distribution FROM bank_loan_status
GROUP BY loan_status;

/* What is the average current loan amount for each loan status category? */
SELECT 
loan_status, 
AVG(current_loan_amount) AS Average_Loan_Amount
FROM bank_loan_status 
GROUP BY loan_status;


 /*What is the average current credit balance for 
 customers with different loan statuses? */
SELECT 
	loan_status, 
	ROUND(AVG(current_credit_balance),2) AS AVG_credit_balance
FROM bank_loan_status
GROUP BY loan_status
ORDER BY loan_status;

/* What is the average credit score for customers with different loan statuses?*/

SELECT loan_status, AVG(credit_score)AS Average_credit_score
FROM bank_loan_status
GROUP BY loan_status;

/* How does the annual income vary among customers with different loan statuses?*/

SELECT loan_status, AVG(annual_income) AS Average_income
FROM bank_loan_status
GROUP BY loan_status;


/* How does the term of the loan vary across different loan statuses? */

SELECT 
	loan_status, 
	term,
	COUNT(*) AS 'Length_Of_Loan_VS_Status'
FROM bank_loan_status 
GROUP BY loan_status, term;


/* How does the current loan amount vary based on the purpose of the loan */
SELECT 
purpose, 
ROUND(AVG(current_loan_amount),2) AS AVG_Current_loan_VS_Purpose
FROM bank_loan_status
GROUP BY purpose
ORDER BY AVG_Current_loan_VS_Purpose DESC;

/* How long, on average, have customers been in their current jobs for each loan status?*/

SELECT 
    loan_status,
    years_in_current_job,
    ROUND(AVG(years_of_credit_history),2) AS avg_credit_years
FROM bank_loan_status
GROUP BY loan_status, years_in_current_job
ORDER BY loan_status DESC;
