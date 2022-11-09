# Lending Case Study
The aim of the project is to identify the patterns in a consumer finance company - called Lending Club's data. It is a consumer finance company which specializes in giving loan to various kind of Urban consumers. The objective is to identify the patterns in the data which helps the company to identify less risky customer.
The company has 2 problem statements:
1) not to lose opportunity by not giving the loan to the right customer
2) Not to lose money by giving the loan to the risky customer 



## Table of Contents
1) Data Understanding
2) Data Cleaning
    2.1) Removing the NaN and missing values from rows and columns
    2.2) Removing columns with singular value or nutliple values which are not significant to the analysis such as emp_title, desc, etc
    2.3) Imputing the missing values and NA values
    2.4) Analyzing the values and their distribution
    2.5) Identifying which variables are categorical and ordinal
3) Data Analysis
    3.1) Univariate Analysis
    3.2) Segmented Variate Analysis
    3.3) Bi-Variate Analysis
    3.4) Correlation Analysis
4) Recommendations/Conclusions


## General information

1. Objective
The aim of the project is to identify the patterns in a consumer finance company - called Lending Club's data. It is a consumer finance company which specializes in giving loan to various kind of Urban consumers. The objective is to identify the patterns in the data which helps the company to identify less risky customer.
The company has 2 problem statements:
1) not to lose opportunity by not giving the loan to the right customer
2) Not to lose money by giving the loan to the risky customer 
The company wants to understand the driving factors (or driver variables) behind loan default, i.e. the variables which are strong indicators of default. The company can utilise this knowledge for its portfolio and risk assessment.

2. About the Data set:
The data for this project is a consumer finance comany data. It contains the information about past loan applicants and whether they ‘defaulted’ or not.
The following columns were used to identify the patterns in this project:

    a. Customer's financial Attributes:
        - Annual Income (annual_inc) - Annual income of the customer. Generally the higher the income the more are the chances of that loan passing 
        - Home Ownership (home_ownership) - Wether the customer owns a home or stays rented. Owning a home adds a collateral which increases the chances of loan pass.
        - Employment Length (emp_length) - Employment tenure of a customer (this is overall tenure). Higher the tenure, more financial stablity, thus higher chances of loan pass
        - Debt to Income (dti) -A ratio calculated using the borrower’s total monthly debt payments on the total debt obligations, excluding mortgage and the requested LC loan, divided by the borrower’s self-reported monthly income. The percentage of the salary which goes towards paying loan. Lower DTI, higher the chances of a loan pass.
        - State (addr_state) - Location of the customer. Can be used to create a generic demographic analysis. There could be higher delinquency or defaulters demographicaly.

    b. Loan Attributes

        - Loan Ammount (loan_amt) - The listed amount of the loan applied for by the borrower. If at some point in time, the credit department reduces the loan amount, then it will be reflected in this value.
        - Grade (grade) - LC assigned loan grade
        - Term (term) - The number of payments on the loan. Values are in months and can be either 36 or 60.
        - Loan Date (issue_date) - The month which the loan was funded
        - Purpose of Loan (purpose) - A category provided by the borrower for the loan request. 
        - Verification Status (verification_status) - Indicates if income was verified by LC, not verified, or if the income source was verified
        - Interest Rate (int_rate) - Interest Rate on the loan
        - Installment (installment) - The monthly payment owed by the borrower if the loan originates.


    c. Decesion Parameters:
        Loan Accepted - There are 3 cases:
            - Fully Paid - Applicant has fully paid the loan (the principal and the interest rate)
            - Current - Applicant is in the process of paying the instalments, i.e. the tenure of the loan is not yet completed. These candidates are not labelled as 'defaulted'.
            - Charged-off - Applicant has not paid the instalments in due time for a long period of time, i.e. he/she has defaulted on the loan

    d. Removed Columns:
        The following types of columns were removed:
        - Any column with a singular value across the rows
        - Insignificant number of NaN values
        - NaN values in a column higher than 60% of total values
        - Columns which were text as well as non-categorical such as description, title, etc
        - Columns which were insignificant to the analysis such as id, member_id, etc



## Recommendations/Conclusions
- For the customers coming for a loan for vacation, house or small business should be either charged higher interest or some collateral should be taken as their default percentage is almost 17%.

 - The above mentioned loans are generally not small ticket loans as well

- Also for small business and house loans term should be lessened as almost 50% of the cases are of “Charged Off” and have 60 months as term

- Lending club should also consider not giving 60 month term loans to other categories as this term leads to higher “Charged Off” cases

- Grades are a good predictor of loan default and some associated metrics should be taken into account for calculating the interest rate by the Lending Club

- As per the data California is the state for which thorough verification should be done before issuing a loan

- Same goes for the states of Florida, New York and Newark


## Technologies Used
- Pandas
- Numpy
- Datetime
- Seaborn
- Matplotlib


## Contributors
- Lydia Sharon James (Group Leader)
- Paratyaksh Singh