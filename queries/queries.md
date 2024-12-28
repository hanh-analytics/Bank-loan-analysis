# BANK LOAN REPORT|QUERY DOCUMENT 
## KPI's:
1. Total Loan Applications
   <br>
   
   ```sql
   SELECT COUNT(id) AS Total_Loan_Applications
   FROM bank_loan
   ```
   
   > Total_Loan_Applications: 3856
2. _MTD_ Loan Applications (_Month-To-Date_ Loan Applications)
   ```sql
   SELECT COUNT(id) AS MTD_Total_Applications
   FROM bank_loan
   WHERE strftime('%m', issue_date) = '12'
   AND strftime('Y', issue_date) = '2021
   ```
   >  MTD_Total_Applications: 4314
3. _PMTD_ Loan Applications (_Previous-Month-To-Date_ Applications)
   ```sql
   SELECT COUNT(id) AS PMTD_Total_Applications
   FROM bank_loan
   WHERE strftime('%m', issue_date) = '11'
   AND strftime('Y', issue_date) = '2021
   ```
    > PMTD_Total_Applications: 4035
   ---
4. Total Funded Amount
   ```sql
   SELECT SUM(loan_amount) AS Total_Funded_Amount
   FROM bank_loan
   ```
   > Total_Funded_Amount: 435757075
5. MTD Total Funded Amount
   ```sql
   SELECT SUM(loan_amount) AS MTD_Total_Funded_Amount
   FROM bank_loan
   WHERE strftime('%m', issue_date) = '12'
   AND strftime('Y', issue_date) = '2021
   ```
   >  MTD_Total_Funded_Amount: 53981425
6. PMTD Total Funded Amount
   ```sql
   SELECT SUM(loan_amount) AS PMTD_Total_Funded_Amount
   FROM bank_loan
   WHERE strftime('%m', issue_date) = '11'
   AND strftime('Y', issue_date) = '2021
   ```
   > PMTD_Total_Funded_Amount: 47754825
   ---
7. Total Amount Received
   ```sql
    SELECT SUM(total_payment) AS Total_Amount_Received
    FROM bank_loan
   ```
   > Total_Amount_Received: 473070933
8. MTD Total Amount Received
   ```sql
   SELECT SUM(total_payment) AS MTD_Total_Amount_Received
   FROM bank_loan
   WHERE strftime('%m', issue_date) = '12'
   AND strftime('Y', issue_date) = '2021
   ```
   > MTD_Total_Amount_Received: 58074380
9. PMTD Total Amount Received
    ```sql
    SELECT SUM(total_payment) AS PMTD_Total_Amount_Received
    FROM bank_loan
    WHERE strftime('%m', issue_date) = '11'
    AND strftime('Y', issue_date) = '2021
    ```
    > PMTD_Total_Amount_Received: 50132030
    ---
10. Average Interest Rate
    ```sql
    SELECT AVG(int_rate)*100 AS Avg_Int_Rate
    FROM bank_loan
    ```
    > Avg_Int_Rate: 12.0488314172048
11. MTD Average Interest
    ```sql
     SELECT AVG(int_rate)*100 AS MTD_Average_Interest
     FROM bank_loan
     WHERE strftime('%m', issue_date) = '12'
     AND strftime('Y', issue_date) = '2021'
    ```
    > MTD_Average_Interest: 12.3560408676042
 12. PMTD Average Interest
     ```sql
     SELECT AVG(int_rate)*100 AS MTD_Average_Interest
     FROM bank_loan
     WHERE strftime('%m', issue_date) = '11'
     AND strftime('Y', issue_date) = '2021'
     ```
     > PMTD_Average_Interest: 11.9417175498261
---
13. Average DTI (Debt-To-Income)
    ```sql
    SELECT AVG(dti)*100 AS Avg_DTI
    FROM bank_loan
    ```
    > Avg_DTI: 13.3274331211432


   
   
