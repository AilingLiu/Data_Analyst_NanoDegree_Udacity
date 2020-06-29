# Exploration on Loan Data.ipynb
## by Ailing Liu

## Project Backgound

[Prosper](https://www.prosper.com/) is a peer-to-peer lending platform that aims to connect people who need money with those who have money to invest. In this Exploratory Data Analysis, I explored a Prosper dataset containing loan information for over 113k borrowers.


## Dataset

The dataset consisted of borrower APRs and attributes of 113,937 loans. The attributes included borrower's Prosper Score, borrower's occupation, original loan amount, loan term, borrower's stated monthly income, as well as many other features such as borrower's employment status, current loan status etc. The dataset can be found [here](https://s3.amazonaws.com/udacity-hosted-downloads/ud651/prosperLoanData.csv), 
with feature documentation available [here](https://docs.google.com/spreadsheets/d/1gDyi_L4UvIrLTEC6Wri5nbaMmkGmLQBk-Yx3z0XDEtI/edit#gid=0).

The exploration was divided into 3 analytical segments in increasing order of complexity: Univariate Plots, Bivariate Plots, and Multivariate Plots, as well as a summary at the end of each segment that summarized the findings throughout data exploration.

## Summary of Findings

In the exploration, I found that the borrower APR was negatively correlated with prosper score and it was also negatively correlated with prosper rating in alphabet letter. In addition, I also found that the borrower APR decrease with the increase of borrow term for people with HR-C raings. But for people with B-AA ratings, the APR increased with the increase of borrow term. It make sense because when people have higher credit score, they are likely to borrow a longer contract term, so a higher APR percerntage will prevent them and maximize the profits.

Outside of the main variables of interest, I created new featur 'Non-Performing Percentage' to indicate the loan status. If loan status was 'defaulted' or 'chargedoff', then this loan was not performed profitably. By integrating the occupation and its average income, I identified that borrower with lower income has higher risk of non-performing loan than those who has higher income in similar position. When new data coming in, we can compare the data points to the trend line. Judging from their position, if they are far below or above the line, it will represent these new borrowers are either “more reliable” or “less reliable,” when compared to other occupations making similar incomes.


## Key Insights
If borrower has low prosper score, he is likely to receive higher APR percentage. However, if borrower's prosper rating is within range C to AA, the longer contract term he applies for, the higher APR percentage he's going to receive. This way, the loan company can prevent people to apply for large loan while maximizing their profits. In addition, Employed and fulltime borrower are the largest group for prosper loan, and this group is in favor of 3 to 5 year repayment term, instead of 1 year. Finally, non-performing ratio decrease while the income of borrower increase, showing negative correlation. Their fitting line serves as strong indicator of reliability of new borrowers based on their income and occupation.


## Reference:

[Prosper Loan Exploratory Data Analysis](https://jianru-shi.github.io/Prosper_Loan_EDA/Prosper_Loan_EDA.html)
