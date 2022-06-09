# Prosper Loans Data Exploration

## Dataset

The data set consists of information regarding 113,937 loans of Prosper including the loan amount, the APR, the variables characterizing a borrower and others. The data set was cleaned and conisists of The description of the data attributes can be found  [here](https://docs.google.com/spreadsheets/d/1gDyi_L4UvIrLTEC6Wri5nbaMmkGmLQBk-Yx3z0XDEtI/edit#gid=0).


## Summary of Findings

In the univariate part of the exploratory analysis I discovered that the average borrower belongs to a "middle class" - the most common monthly income is around $ 5000 per montn, they have equal chances of having or not having a home, most likely they're employed. The most popular term is 36-month loan and the vast majority of loans are not defaulted or delayed. The most common reason for getting a loan is a debt consolidation.

In the bivariate part I found that the loan amount and the APR are mostly impacted by the credit score and that the median loan amount and the range of loan amount values differs a lot across terms (the longer the term the higher the median). I also discovered that retired borrowers have the lowest median APR and one of the highest median loan amount and the unemployed borrowers have, on the contrary, the lowest amount and the highest APR. I also noticed that the APR doesn't change much across the term and that homeowners have slighthly higher median income, median loan amount and slightly lower APR than those who doesn't own a home. It was also observed that 36-term loans have the highest percentage of defaulted and delayed loans in comparison with other term offers. The other interesting observation is that retired borrowers have the highest proportion of high Prosper score (10 and 11) values while self-employed have the lowest proportion of those scores. I used log transformation to plot the loan amount vs. credit score and observed a linear relationship - the loan amount increases as the credit score increases. The APR, on the contrary, decreases with the decrease of the credit score. After checking the distribution with violin plots I observed that the debt consolidation category have the highest median loan amount and the lowest median APR. The business category has the 2nd highest loan amount and the 2nd lowest APR. It's also notable that delayed and defaulted loans have lower median loan amount and higher median APR.

In the multivariate analysis I could see that for 60-month term a lot of data points are located at the APR of 0.2 and the credit score of 700. For 36-month term a lot of data points located at the same credit score value but with the APR of 0.4 and for 12-month I can see more data points with really high credit score (>800) and really low APR (0.1 or less) than in other terms. I could also see that delayed and defaulted loans have more data points at lower credit score and higher APR ticks than current and completed loans. I could also see that when the Prosper score increases the loan amount increases and the APR decreases even though some exceptions from this rule was observed - the median loan amount of defaulted loans started decreasing from point 8 of the Prosper score as well as completed loans decreased starting from point 8 and increased again on point 1. 


## Key Insights for Presentation

For this presentation I'll focus on the next questions:
1. What is the main characteristics of an average borrower.
2. What variables affect the loan amount and the APR the most.

I'll start by introducing the distribution of the income level, then I add the bar charts showing the fact of owning a home, Employment status, Category, Term and the loan status. Then I'll show percentage clustered barcharts of the loan status and the Prosper score and scatterplots of the credit score vs. the loan amount and the credit score vs. the APR. I also include violin plots on the loan status. Then, I'll introduce faceted grid with term and the loan status. Finally, I'll add point plots showing how the loan amount and the APR change with changing of the Prosper score.

## Links
[What does it mean to default on a loan](https://www.valuepenguin.com/loans/what-does-it-mean-to-default-on-a-loan)

[How to Place Legend Outside of The Plot](https://www.delftstack.com/howto/matplotlib/how-to-place-legend-outside-of-the-plot-in-matplotlib/)

[How to convert CategoricalIndex to normal Index](https://stackoverflow.com/questions/60203258/how-to-convert-categoricalindex-to-normal-index)