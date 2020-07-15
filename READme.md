# Classification Model
### Author: Ryan Sims

Using data from a Porteguese banking institution, develop a classification model to predict deposit term subscribers.  This is a supervised machine learning problem.
> It is important to understand that predicting clients as non subscribers when they are actually subscribers is a category that needs to be minimal.  This false negative enumerates the model's error in misclassifying subscribers.

## Methods:

### 1) EDA
> Begin with understanding the data types in the data set.  Numerical data and categorical data must be treated in different manners in order to be prepared for modeling.  Columns with data in string format will have to be encoded to be given a numerical value.  Label encoder works best to assign a number for each label in the column.  The downside is that it doesn't assign any sort of heirarchy.  If a heirarchy is desired it is possible to code it manually. 

> The numerical data can be categorized as well by grouping into bins.  This was done on the Age column, since there were 78 unique ages present in the dataset.  Scaling and Normalizing is another consideration for numerical data.

### 2) Classifiers
> Using scikit-learn classifers, model the data using a train/test split and then compare the training and test sets for generalization.  
> The confusion matrix will be used to determine how effective the model is.  The model with the least amount of False Negatives will be considered the most effective.

## Results
> The model yielded good generalization and accuracy.  The decision tree classifier had the fewest False Negative errors, while the Logistic Regression classifier had the best accuracy score.

## Recommendations
> Classifying term deposit subscribers displayed how effective different classifying methods can be. Out of all the classifiers used, Decision Tree had the fewest False Negatives. This is crucial since we want to minimize the amount of actual subscribers the model misses.

It is recommended that clients be contacted via cellular phones, instead of landline telephones. 4,369 subscribers were contacted via cellphone versus 360 subscribers on landline.

Subscribers without housing loans were present more than subscribers with housing loans. The ratio was less than 2:1 so it is recommended to consider clients with or witout housing loans.

It is also recommended to pitch the client longer than about 5 minutes. Subscribers were on the phone for about 5 minutes or more before subscribing.