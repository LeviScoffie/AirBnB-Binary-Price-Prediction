# AirBnB-Binary-Price-Prediction
Logistic Regression(Binary Classification)

## Question 1

What is the most frequent observation (mode) for the column 'neighbourhood_group'?


Split the data
Split your data in train/val/test sets, with 60%/20%/20% distribution.
Use Scikit-Learn for that (the train_test_split function) and set the seed to 42.
Make sure that the target value ('price') is not in your dataframe.


## Question 2
Create the correlation matrix for the numerical features of your train dataset.
In a correlation matrix, you compute the correlation coefficient between every pair of features in the dataset.
What are the two features that have the biggest correlation in this dataset?
Example of a correlation matrix for the car price dataset:



Make price binary
We need to turn the price variable from numeric into binary.
Let's create a variable above_average which is 1 if the price is above (or equal to) 152.

## Question 3
Calculate the mutual information score with the (binarized) price for the two categorical variables that we have. Use the training set only.
Which of these two variables has bigger score?
Round it to 2 decimal digits using round(score, 2)

## Question 4
Now let's train a logistic regression
Remember that we have two categorical variables in the data. Include them using one-hot encoding.
Fit the model on the training dataset.
To make sure the results are reproducible across different versions of Scikit-Learn, fit the model with these parameters:
model = LogisticRegression(solver='lbfgs', C=1.0, random_state=42)
Calculate the accuracy on the validation dataset and round it to 2 decimal digits.


## Question 5
We have 9 features: 7 numerical features and 2 categorical.
Let's find the least useful one using the feature elimination technique.
Train a model with all these features (using the same parameters as in Q4).
Now exclude each feature from this set and train a model without it. Record the accuracy for each model.
For each feature, calculate the difference between the original accuracy and the accuracy without the feature.
Which of following feature has the smallest difference?
neighbourhood_group
room_type
number_of_reviews
reviews_per_month
note: the difference doesn't have to be positive

## Question 6
For this question, we'll see how to use a linear regression model from Scikit-Learn
We'll need to use the original column 'price'. Apply the logarithmic transformation to this column.
Fit the Ridge regression model on the training data.
This model has a parameter alpha. Let's try the following values: [0, 0.01, 0.1, 1, 10]
Which of these alphas leads to the best RMSE on the validation set? Round your RMSE scores to 3 decimal digits.
If there are multiple options, select the smallest alpha.
