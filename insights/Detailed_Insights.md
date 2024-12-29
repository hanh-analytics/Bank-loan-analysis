# Detailed Insights 🔍 
_This file tends to investigate deeper into insights I mentioned in [Execute Summary](insights/Executive_Summary.md). This report's goal is to examine the bank's loan portfolio with an emphasis on a number of important financial indicators, including debt-to-income (DTI) ratios, interest rates, loan amounts, and loan status. The objectives of this research are to evaluate possible risks, shed light on the portfolio's health, and make suggestions for better lending practices._

In this report, we will examine:

 - **Bank health**: Key indicators such as the Total Amount Received, Total Funded Amount and DTI ratio provide insight into the bank's profitability and risk exposure.
   
 - **Portfolio perfomance**: There is still a considerable chance of a _higher default risk_ even though the presence of Good Loan status and comparatively low average DTI ratios for both low-risk and high-risk categories indicate solid portfolio performance.
   
 - **Higher risk of defaults**: By examining interest rates and purposes, we can determine the high needs of clients and then recommend an appropriate method of risk mitigation.

## 1. Data Overview:
 ### 1.1. Dataset Summary:

- **Grade**: The grade is used by banks to control risk and set loan prices. Higher-grade loans are more appealing to investors and usually have lower interest rates.
  
- **Loan Status**: The purpose of `Loan Status` is to show the loan's current status (e.g., fully paid, current, default). Banks utilize `Loan Status` to classify loans for risk analysis, track loan health, and identify provisioning needs.
  
- **Purpose**: By segmenting and tailoring loan offerings, banks may match lending terms to the demands of their borrowers.
  
- **Verification Status**: `Verification Status` shows if the borrower's financial data has been validated. Banks utilize this field to assess the trustworthiness of loan applications, confirm income, and measure data reliability.

- **DTI (Debt-to-Income Ratio)**: `DTI` determines how much debt the borrower can afford to take on. `DTI` is used by banks to evaluate a borrower's capacity to manage loan payments and make smart lending choices.
  
- **Loan Amount**: The loan amount shows the amount of the principle. Banks calculate loan sizes based on loan amounts. In this case, the total loan amount is `Total Funded Amount`. 
  
- **Loan Applications**: When people or companies apply for loans, they fill out comprehensive forms that contain financial and personal data. This information is gathered either on paper or electronically.
  
- **Amount Received**: The amount of money that clients repay for their loans to the bank.

- **Current**: The fact that borrowers are paying on time shows that they have good repayment habits and liquidity.

- **Fully Paid**: The portfolio has a high success rate since borrowers have successfully repaid their loans.

- **Charged Off**: Loans that have been written off as uncollectible. A low percentage indicates fewer defaults and better credit risk management.
  
 ### 1.2 Data Quality Notes:
 - **General Cleaning**: For the purpose of addressing missing values, eliminating duplicates, and standardizing formatting across columns—including dates and categorical variables—the dataset was thoroughly cleaned.

 - **Data Transformation**: To make time-series analysis easier, string-based data such as `issue_date` were transformed into date-time format.

 - **Data Integrity Checks**: The `total_payment` and `loan_amount` were cross-validated to find any discrepancies or mistakes in the data entry.

 - **Data Filtering**: Loans with invalid or missing statuses were not included in the study to guarantee accurate and significant findings.


## 2. Detailed Insights:

 ### 2.1. Bank health: 

 ![Big_Number](https://github.com/hanh-analytics/Bank-loan-analysis/blob/a1ecef8a4af1b06c177ab529c69cf6974093773b/visualization/Big_Number.jpg)
  
- A high DTI ratio and plenty of liquidity seem to underpin the bank's apparent stability. This indicates that debtors contribute 13.3% of their monthly gross income to debt repayments, with an average DTI of 13.3% per month. Lenders typically desire a DTI ratio of less than 36%, meaning that mortgage payments should not account for more than 28% to 35% of income. This implies that the bank is bringing in customers with manageable and comparatively steady debt loads, a sign of ethical lending operations.
Furthermore, the liquidity ratio is above 100% since the total amount received ($473.1 million) exceeds the total amount funded ($435.8 million). In addition to having enough cash on hand to satisfy short-term commitments like depositor withdrawals, loan repayments, and operating expenses, this shows that the bank is equipped to handle unanticipated circumstances like downturns in the economy.

![KPI_By_Loan_Status](https://github.com/hanh-analytics/Bank-loan-analysis/blob/a1ecef8a4af1b06c177ab529c69cf6974093773b/visualization/KPI_by_Loan_Status.jpg)

- Between the total funded amount, total amount received, and total loan applications, the total funded amount shows the financial worth of loans that are performing well (good loans) vs. those that are not (bad loans), which directly represents the portfolio's exposure. Regarding portfolio performance, the proportion of good loan status `Fully Paid` and `Current` (84.96% in total) exceeds that of `Charged Off` in the total funded amount, which typically indicates a healthy bank loan portfolio. Increased cash inflows from higher repayments boost liquidity and profitability, while lower charge-offs reduce losses and raise the yield on the entire portfolio. Strong underwriting guidelines and borrower selection are evident, supported by efficient monitoring and recovery procedures. Additionally, a portfolio that is primarily composed of `Current` and `Fully Paid` loans indicates reduced risk, which attracts investors and may result in better conditions for funding or refinancing options.
 
 Overall, the analysis shows that the bank's strong portfolio performance supports its stable health. The analysis of important indicators like the average DTI, liquidity ratio, and total funded amount by loan status shows that the bank is operating efficiently and is in a strong position to pay its debts.

 




