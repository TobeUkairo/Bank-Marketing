# Bank-Marketing
 In this scenario, various factors influence a customers decision to subscribe a term deposit as a result of direct marketing campaigns (Phone calls)
# Executive Summary

**Objective**: Create a predictive model to determine if clients will subscribe to a term deposit during phone marketing campaigns ('yes' or ‘no).

**Key Findings**: 
- the features “pdays” “month” and “job” are factors  that are critical for predicting if clients will subscribe to a term deposit during phone marketing campaigns. 

- The 'age' column appears to exhibit a normal distribution.

- The occupations 'blue-collar,' 'management,' and 'technicians' collectively account for over 58% of the clients in our dataset.

- Approximately 60% of our clients are married.

- Half of our clients hold a secondary degree, while nearly 30% possess a tertiary degree.

- More than 95% of our data represents individuals without a history of default.

- Over 50% of our data indicates clients with housing loans.

- More than 80% of our clients do not have any form of loan.

- The 'contact' column contains numerous 'unknown' values, and the decision has been made to retain them as they are.

- The 'day' column poses challenges and will be dropped from the analysis.

- Considering the campaign strategy, it is plausible that fewer contacts were made during winter, with summer being the preferred season for campaigns.

- The 'duration' column contains several outliers, which will be addressed in subsequent steps.

- At least 75% of our data reflects instances where clients were contacted at least 3 times.

- Similarly, at least 75% of our data indicates instances where clients were not previously contacted.

**Recommendation**: Focus on acquiring high-value brands and adjust pricing strategies based on age, mileage, and fuel type.


## Data Overview

**Dataset Description**: The data is related with direct marketing campaigns of a Portuguese banking institution. The marketing campaigns were based on phone calls. Often, more than one contact to the same client was required, in order to access if the product (bank term deposit) would be ('yes') or not ('no') subscribed.




## Data Preparation

**Cleaning**: dropped the following columns  'previous', 'poutcome', 'emp.var.rate', 'cons.price.idx', 'cons.conf.idx', 'euribor3m', 'nr.employed', 'day_of_week','duration'

**Transformation**: Applied standard scaler to the X_train dataset and X_test dataset.

**Feature Engineering**: used label encoder to encode all categorical variables, a smote was used to help solve the problem of imbalanced data.

**Model Selection**: compared between KNN, Decision Tree, Logistic Regression and SVM models.

**Hyperparameter Tuning**: Employed GridSearchCV for optimal parameter selection.

## Model Insights and Interpretation

**Model Performance**:

The decision tree model performed best in terms of training time, precision, accuracy and precision all considered. Although logistic regression had a higher precision, the Decision tree model outperformed it in terms of all other metrics as well as training speed.


## Limitations and Future Work

**Limitations**:

Imbalanced dataset. 


## Future Directions

Aim to get a more balanced data set for better performing models. When gathering data pay attention to factors like month, occupation and number of days that passed by after the client was last contacted from a previous campaign.

## Conclusion

The analysis provides valuable information into factors that affect a clients decision to subscribe. The company can take advantage of these findings identify critical factors affecting success of campaigns as well as to optimise targeting strategies.
