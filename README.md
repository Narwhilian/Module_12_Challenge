# Analysis Summary

## Overview of Analysis

For this report I utilized superised learning to train a model to correctly classify risky and healthy loans. My model examined the size of the loan, the interest rate, the income of the borrower, the debt to income ratio of the borrower, the number of accounts in their name, the number of derogatory marks against the borrower and total debt as well as the labled status of the loan (risky/non risky) to train to predict patterns among those variables to correctly predict the status of a loan as risky or non risky.

While my initial analysis had strong results using a logistic regression model, I determined that the data was very imbalanced (which would be expected since healthy, non-risky loans far outnumber those that are risky to the lender). I was able to improve the model by relying on resampling (in this case over sampling) to balance out the data.

## Results

The following are the results of both models.

* Supervised Machine Learning Model 1 (Logistic Regression with original unbalanced data):

  * Accuracy: 95.2%
  * Precision (minority class/risky loans): 85%
  * Recall (minority class/risky loans): 91%


* Supervised Machine Learning Model 2 (Logistic Regression with Oversampled data):

  * Accuracy: 99.4%
  * Precision (minority class/risky loans): 84%
  * Recall (minority class/risky loans): 99%

## Summary

While both models performed well in their test predictions it is important to compare their results to determine the best (if any) to use when identifying risky loans.

The resampled model had a slightly higher accuracy score of 99.4% meaning it was better at correctly identifying true positives and true negatives (risky and healthy loans respectively). In terms of accuracy the oversampled model performs better.

While the precision score of the original unbalanced model was slightly higher than the precision score of the oversampled model (85% vs 84%). At the end of the day the two precision scores are so incredibly close that I would say neither is clearly better than the other in a practical sense. 

Finally the oversampled model had a higher recall score than the original model using the unbalanced data (99% vs 91%) this means out of all the risky loans (the sum of the true positive and false negative results) the oversampled model correctly labled the risky loans as "risky" 8% more often than the original model using the unbalanced data. 

I would reccomend using the oversampled model since it is more accurate, has better recall, and while it has slightly lower precision score it is still comparable to the other model.

