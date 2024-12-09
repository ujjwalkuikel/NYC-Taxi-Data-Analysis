# TLC Trip Data

# Prastut Dahal, Dipika Bogati, Ujjwal Kuikel

## Project Introduction

The data originates from the NYC Taxi and Limousine Commission (TLC) and is submitted by authorized technology providers under the Taxicab & Livery Passenger Enhancement Programs (TPEP/LPEP) and it claims that it enforces measures to maintain, as much as possible, the data's completeness and reliability. This project focuses on analyzing Yellow Taxi trip data from January to June 2024 which is total 2.6 million rows. The dataset provides comprehensive records including pick-up and drop-off dates and times, locations, trip distances, itemized fare components, rate types, payment methods, and passenger counts as reported by drivers.


## Project Details

TLC Trip data is used to implement the regression, classification and forecast.

For classification, payment_type categorical column is used in the project. The payment_type column include 6 categorical records as:

1= Credit card
2= Cash
3= No charge
4= Dispute
5= Unknown
6= Voided trip

However, for the models used for classification expect the record to be indexed from 0. So, the record is pre-processed in such a way that column data starts from 0 to 5. The models also expect the record to not have the empty value and NaN value so it is solved on the pre-processing section.

The models used for classifications are:

1. Logistic Regression
2. Decision Tree
3. Random Forest
4. XGBoost

Each model is trained and tested using 5-fold cross validation and ensured there is no leakage from training data to testing data. Now, the metrics like precision, recall, f1 score and accuracy is used to identify the models accuracy for the classification of the trip record datasets. It is expected that XGBoost have the higher accuracy followed by Random Forest  and (decision tree and Logistic Regression). However, the results show that Random Forest is higher performing for the given datasets compared to all three models. In order to increase efficiency of XGBoost, parameter update has also been done but the result were worst than the parameter used in the current project. To some extent, Random Forest is also expected to give higher performing result because Random Forest is an ensemble of decision trees, where each tree is trained on a random subset of the data with random feature selection. This randomness reduces the risk of overfitting compared to a single Decision Tree.
