# Detailed Insights 🔍 
_This file tends to investigate deeper into insights I mentioned in [Execute Summary](https://github.com/hanh-analytics/Bank-loan-analysis/blob/5f755523c9110c16462607b7c3539cc0034df64e/insights/Executive_Summary.md). This report's goal is to examine the bank's loan portfolio with an emphasis on a number of important financial indicators, including debt-to-income (DTI) ratios, interest rates, loan amounts, and loan status. The objectives of this research are to evaluate possible risks, shed light on the portfolio's health, and make suggestions for better lending practices._

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

 ### 2.1. Bank health and portfolio perfomance: 

 ![Big_Number](https://github.com/hanh-analytics/Bank-loan-analysis/blob/a1ecef8a4af1b06c177ab529c69cf6974093773b/visualization/Big_Number.jpg)
  
- A high DTI ratio and plenty of liquidity seem to underpin the bank's apparent stability. This indicates that debtors contribute 13.3% of their monthly gross income to debt repayments, with an average DTI of 13.3% per month. Lenders typically desire a DTI ratio of less than 36%, meaning that mortgage payments should not account for more than 28% to 35% of income. This implies that the bank is bringing in customers with manageable and comparatively steady debt loads, a sign of ethical lending operations.
Furthermore, the liquidity ratio is above 100% since the total amount received ($473.1 million) exceeds the total amount funded ($435.8 million). In addition to having enough cash on hand to satisfy short-term commitments like depositor withdrawals, loan repayments, and operating expenses, this shows that the bank is equipped to handle unanticipated circumstances like downturns in the economy.

![KPI_By_Loan_Status](https://github.com/hanh-analytics/Bank-loan-analysis/blob/a1ecef8a4af1b06c177ab529c69cf6974093773b/visualization/KPI_by_Loan_Status.jpg)

- Between the total funded amount, total amount received, and total loan applications, the total funded amount shows the financial worth of loans that are performing well (good loans) vs. those that are not (bad loans), which directly represents the portfolio's exposure. Regarding portfolio performance, the proportion of good loan status `Fully Paid` and `Current` (84.96% in total) exceeds that of `Charged Off` in the total funded amount, which typically indicates a healthy bank loan portfolio. Increased cash inflows from higher repayments boost liquidity and profitability, while lower charge-offs reduce losses and raise the yield on the entire portfolio. Strong underwriting guidelines and borrower selection are evident, supported by efficient monitoring and recovery procedures. Additionally, a portfolio that is primarily composed of `Current` and `Fully Paid` loans indicates reduced risk, which attracts investors and may result in better conditions for funding or refinancing options.
 
 Overall, the analysis shows that the bank's strong portfolio performance supports its stable health. The analysis of important indicators like the average DTI, liquidity ratio, and total funded amount by loan status shows that the bank is operating efficiently and is in a strong position to pay its debts.

 ### 2.2: The Potential of higher-risks Borrowers:

 Even while the bank's overall health appears to be solid, possible increases in debt could put the bank in trouble. I want to highlight two points to demonstrate that there may be a rise in the default risk:
 
 ![Interest rate](https://github.com/hanh-analytics/Bank-loan-analysis/blob/a334401925af8cd1d8dd0e397779e0c136d07c36/visualization/Interest_rate_by_Purpose.jpg)

 - First of all, we can see that the average rate for every purpose of lending money is higher than 10%, while loans like cars, education, house, home improvement, and renewable energy are most likely to range from around 5% to 7%. From the perspective of the lenders, a higher risk of default leads to a greater likelihood that some loans will eventually be charged off (written off as bad debt), especially in categories with higher interest rates. On the other hand, borrowers with higher rates are more likely to struggle with repayment, which can lead to missed payments, defaults, or the need to refinance. This puts more pressure on the borrower’s finances, further elevating the chance of default.

![Total Loan Application by Purpose](https://github.com/hanh-analytics/Bank-loan-analysis/blob/a334401925af8cd1d8dd0e397779e0c136d07c36/visualization/Total_Application_by_Purpose.jpg)

- It is necessary to consider the needs of the customers. The graph that illustrates the bank's lending purpose shows that _credit card_ and _debt consolidated_ are at the top of the list. A high volume of applications for credit card and debt consolidation loans may indicate that borrowers are having difficulty managing their existing debt burden, which could raise the likelihood of defaults if borrowers are unable to successfully manage their new debt levels.

- The health of the bank could also be harmed because a significant concentration of loans for certain uses could put the bank at higher risk. An excessive amount of the bank's portfolio devoted to unsecured loans or high-risk clients may have an impact on the portfolio's overall stability.

- As well as that, a credit card and aggregated debt are frequently linked to lower interest rates than other loan types, such as payday or personal loans. The _profitability_ of the loan portfolio may decline if the bank has a lot of these loans, particularly if a significant portion of the loans are being given at low interest rates.

To sum up, the bank's portfolio indicates a tendency toward higher-risk borrowers, as demonstrated by the high demand for credit card refinance and debt consolidation loans and their high interest rates. These elements imply that a significant proportion of the clientele may already be experiencing financial difficulties, which raises the possibility of defaults. Although these loan options meet borrowers' urgent needs, they also highlight how crucial it is to put strong risk management plans into place and make sure the bank's lending and pricing policies appropriately offset the higher risk profile.
 

 




