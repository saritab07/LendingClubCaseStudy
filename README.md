# Lending Club Case Study
> A consumer finance company which specialises in lending various types of loans to urban customers has the following business requirement. When the company receives a loan application, the company has to make a decision for loan approval based on the applicant’s profile. Two types of risks are associated with the bank’s decision:
- If the applicant is likely to repay the loan, then not approving the loan results in a loss of business to the company
- If the applicant is not likely to repay the loan, i.e. he/she is likely to default, then approving the loan may lead to a financial loss for the company
Problem statement is to identify patterns that can provide guidance to the company to predict applicant’s loan repayment behavior and accordingly approve loan application.



## Table of Contents
* [Overall Approach for Analysis](##overallapproachforanalysis)
* [Data Sourcing & Cleaning](#technologies-used)
* [Variable Identification for Analysis](#conclusions)
* [Univariate Analysis](#acknowledgements)
* [Bivariate Analysis](#acknowledgements)
* [Derived Metric](#acknowledgements)
* [Correlation Analysis on Numeric Variable](#acknowledgements)
* [Heat Map Analysis](#acknowledgements)
* [Overall Analysis Conclusion](#overallanalysisconclusion)
* [Recommendation Based on Analysis](##FinalRecommendationBasedonAnalysis)

<!-- You can include any other section that is pertinent to your problem -->

## Overall Approach for Analysis
- The overall approach taken for analyzing the data is depcited in the following diagram

  ![image](https://github.com/saritab07/LendingClubCaseStudy/assets/97290022/e0398495-ee70-43b1-a5a7-29cfbebd7695)

<!-- You don't have to answer all the questions - just the ones relevant to your project. -->

## Data Sourcing & Data Cleaning
- Data Sourcing : Data provided for the case study in the module has been used
![image](https://github.com/saritab07/LendingClubCaseStudy/assets/97290022/08c46ee6-021d-44a4-b690-2c5b8ffd63ca)

![image](https://github.com/saritab07/LendingClubCaseStudy/assets/97290022/3bd62b0f-599d-47d2-95ed-a1d8ef0227af)
- Data Cleaning Steps:
Missing Value Check
Dropping columns with more than or equal to 60% null values
Checking for unique counts
Identifying sample dataset by applying filter on “Loan Status” = ‘Charged off’ for the analysis
![image](https://github.com/saritab07/LendingClubCaseStudy/assets/97290022/712749a8-302b-4b6e-815f-0d25244efcef)
![image](https://github.com/saritab07/LendingClubCaseStudy/assets/97290022/d7ea6418-a716-44a0-9937-62fdfe48219c)

<!-- You don't have to answer all the questions - just the ones relevant to your project. -->


## Variable Identification for Analysis  
- Below Variables have been identified for the analysis
  ![image](https://github.com/saritab07/LendingClubCaseStudy/assets/97290022/27c7151e-8e5f-40d7-a49d-0a6947c4bc8b)


<!-- As the libraries versions keep on changing, it is recommended to mention the version of library used in this project -->

## Univariate Analysis
- Using the numeric columns identified, below analysis results found:
  - More loan was given on “Term” with 36 months in comparison to 60 months
  - More loan was given for a “Funded Amount” in the range of 5000 – 15000
  

![image](https://github.com/saritab07/LendingClubCaseStudy/assets/97290022/572e77a9-b251-4eec-aad8-615c568e49ed)


  - More loan in on lower “Interest Rate” provided. Interest rates have been categorized from “Low” to “Very High” for analysis. 



## Bivariate Analysis
### Bivariate Analysis - Details
A) Bivariate analysis has been conducted on the Target Variable of “Loan Status = ‘Charged off’” for ‘Purpose’ to identify the pattern for probable defaulting
  ![image](https://github.com/saritab07/LendingClubCaseStudy/assets/97290022/0180bde7-cb1a-434b-8f81-44eadc5b7bf9)

#### Analysis Conclusion
It is noted that loan applicants for “Debt Consolidation” purpose have more Charged off loan status. This concludes that there is a more probability of defaulting a loan in the Debt Consolidation category

B) Bivariate analysis has been conducted on the Target Variable of “Loan Status = ‘Charged off’” for ‘Grade’ to identify the pattern for probable defaulting
![image](https://github.com/saritab07/LendingClubCaseStudy/assets/97290022/7350d54d-3710-45a7-8d58-54dd0468f893)

#### Analysis Conclusion
It is noted that loan applicants for “Grade B” have more Charged off loan status. This concludes that there is a more probability of defaulting a loan in the Grade B category 

C) Bivariate analysis has been conducted on the Target Variable of “Loan Status = ‘Charged off’” for ‘Term’ to identify the pattern for probable defaulting
![image](https://github.com/saritab07/LendingClubCaseStudy/assets/97290022/f575791b-c6b3-42b5-ad6c-ba7ab3086963)

#### Analysis Conclusion
It is noted that loan applicants for “36 months” loan period have more Charged off loan status. This concludes that there is a more probability of defaulting a loan in the 36 month term category. The probable reasons could be that the Monthly Installment of repayment amount(EMI) would have been higher than the repayment capacity of the loan applicant. Therefore, checking the monthly salary and assessing the repayment capacity month-wise would be recommended. There could be multiple other parallel loans that an applicant has which could be leading to defaulting. Therefore, checking for other existing loans would be recommended.

D) Bivariate analysis has been conducted on the Target Variable of “Loan Status = ‘Charged off’” for ‘Verification_Status’ to identify the pattern for probable defaulting
![image](https://github.com/saritab07/LendingClubCaseStudy/assets/97290022/8e83fc64-d88e-436d-8739-9fee60506207)


#### Analysis Conclusion
It is noted that loan applicants for “Not Verified” Annual Salary have more Charged off loan status. This concludes that there is more probability of defaulting a loan in the Not verified category. The probable reasons could be the annual salary has been wrongly indicated by the loan applicant or could have changed(reduced) during the loan period due various reasons which might have led to the defaulting of loan repayment. 

### Bivariate Analysis - Summary

- Bivariate analysis has been conducted on the Target Variable of “Loan Status” = ‘Charged off’” for the below columns to identify the pattern for probable defaulting
  - Purpose
  - Grade
  - Verification Status
  - Term


- Based on the univariate analysis conducted we notice that, the highest loans that were charged off were
-   - Related to loans provided for the purpose of “Debt Consolidation"
    - Related to “B” and “C” Grade
    - Pertained to a non verified source as the “Verification Status” is “Not Verified”
    - Pertain to 36 months “Term”

#### Analysis Conclusion:
- It is noted that loan applicants for “Debt Consolidation” purpose have more Charged off loan status. This concludes that there is a more probability of defaulting a loan in the Debt Consolidation category
- It is noted that loan applicants for “Grade B” have more Charged off loan status. This concludes that there is a more probability of defaulting a loan in the Grade B category
- It is noted that loan applicants for “Not Verified” Annual Salary have more Charged off loan status. This concludes that there is more probability of defaulting a loan in the Not verified category. The probable reasons could be the annual salary has been wrongly indicated by the loan applicant or could have changed(reduced) during the loan period due various reasons which might have led to the defaulting of loan repayment.
- It is noted that loan applicants for “36 months” loan period have more Charged off loan status. This concludes that there is a more probability of defaulting a loan in the 36 month term category. The probable reasons could be that the Monthly Installment of repayment amount(EMI) would have been higher than the repayment capacity of the loan applicant. Therefore, checking the monthly salary and assessing the repayment capacity month-wise would be recommended. There could be multiple other parallel loans that an applicant has which could be leading to defaulting. Therefore, checking for other existing loans would be recommended.

## Derived Metric
### Derived Metric - Identification & Approach
- Target column = Emp_length (purpose is to identify the cohort of users who are more likely to default loan repayment)
- Performed String to Integer conversion for Emp_Length
- Replaced null values with value “Undetermined Experience” 
- Created a derived column named as “Emp_Exp” showing the categorization of employee_length

![image](https://github.com/saritab07/LendingClubCaseStudy/assets/97290022/330dd9b8-97e8-4b1e-9e6f-7f7144af318a)

### Derived Metric - Analysis
![image](https://github.com/saritab07/LendingClubCaseStudy/assets/97290022/c5ecbfe6-e323-4ea0-a82c-72a73839ac81)

#### Analysis Conclusion
Based on analysis it can be noted that people with “Intermediate” experience level are more likely to default loan repayment

## Correlation Analysis
Performed correlation analysis between Funded Amount & Annual Income. The correlation is 0.35 for these variables.

![image](https://github.com/saritab07/LendingClubCaseStudy/assets/97290022/7f9c4fab-9dae-443d-8985-b5e776f7e914)

#### Analysis Conclusion
With the above analysis we can conclude that if the Annual Income is more then Funded Amount can be more. This can suggest positive repayment behavior of the loan applicant.

## Heat Map Analysis
- Interest Rate has been converted to float from percentage and then categorized into various categories(L – Low, M – Medium, H –High, VH-Very High)
- Stacked the Loan Purpose into these interest categories to determine the category to determine where most default has happened. 
![image](https://github.com/saritab07/LendingClubCaseStudy/assets/97290022/4c5b1823-fe40-4b5c-a1a0-7f5868126d9f)

#### Analysis Conclusion
Based on the above we notice that Loans provided for “Debt Consolidation” purpose with a higher interest rate has more defaulting of loan repayment.

## Overall Analysis Conclusion
- Based on the Univariate Analysis it is observed that maximum defaulting of repayment of loan happens in:
  - Loans approved for the 36 months term
  - Loan amount approved is the range of 5000 – 15000

- Bivariate Analysis Conclusion:
  - It is noted that loan applicants for “Debt Consolidation” purpose have more Charged off loan status. This concludes that there is a more probability of defaulting a loan in the Debt Consolidation category
  - It is noted that loan applicants for “Grade B” have more Charged off loan status. This concludes that there is a more probability of defaulting a loan in the Grade B category
  - It is noted that loan applicants for “Not Verified” Annual Salary have more Charged off loan status. This concludes that there is more probability of defaulting a loan in the Not verified category. The probable reasons could be the annual salary has been wrongly indicated by the loan applicant or could have changed(reduced) during the loan period due various reasons which might have led to the defaulting of loan repayment.
  - It is noted that loan applicants for “36 months” loan period have more Charged off loan status. This concludes that there is a more probability of defaulting a loan in the 36 month term category. The probable reasons could be that the Monthly Installment of repayment amount(EMI) would have been higher than the repayment capacity of the loan applicant. Therefore, checking the monthly salary and assessing the repayment capacity month-wise would be recommended. There could be multiple other parallel loans that an applicant has which could be leading to defaulting. Therefore, checking for other existing loans would be recommended.

- Based on Derived Metric analysis it can be noted that people with “Intermediate” experience level are more likely to default loan repayment.

## Final Recommendation Based on Analysis
- Company can provide loan based on Annual Salary Verification Status, Purpose, Term and Grade. Verification of Annual Salary, Monthly repaying capacity of loan applicants are crucial in determining the repayment status.

- Loan applicants having higher annual income are more likely to repay loan for a higher funded amount in comparison to a lower annual income applicant. 

- If “Debt Consolidation” is the purpose of the loan and the interest rate is Very High (>75% of overall distribution of interest rate) then the chances of defaulting a loan repayment is “High”.






Created by [@saritab07] & [@gaurav3714] - feel free to contact us!


<!-- Optional -->
<!-- ## License -->
<!-- This project is open source and available under the [... License](). -->

<!-- You don't have to include all sections - just the one's relevant to your project -->
