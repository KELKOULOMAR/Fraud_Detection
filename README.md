# Machine-Learning-Classification
# Credit card fraud detection

The mean goal is to predict instances of fraud using data based on [this dataset from Kaggle](https://www.kaggle.com/dalpozz/creditcardfraud).
 
Each row in `fraud_data.csv` corresponds to a credit card transaction. Features include confidential variables `V1` through `V28` as well as `Amount` which is the amount of the transaction. 
 
The target is stored in the `class` column, where a value of 1 corresponds to an instance of fraud and 0 corresponds to an instance of not fraud.

### 1st step:
Import data and calculate the percentage of the observations in the dataset that are instances of fraud.

### 2nd step:
Split data to X_train, X_test, y_train, and y_test.

### 3rd step:
Training a dummy classifier that classifies everything as the majority class of the training data and calculate its accuracy and its the recall.

### 4th step: 
As the pourcentage of fraud if very small, accuracy is not a good metric for our project. 
Recall and precision are better metrics to evaluate our model. 
As the recall of dummy regressor is very small, we train a SVC classifer using the default parameters and calculate its accuracy, it's recall and it's precision.

### 5th step:
We see that the recall is better in SVC classifier than dummy regressor.
Even if we have a good precision score, but to avoid to misclassify any fraud, we will improve recall by optimising parameters of the SVC classifier.

### 6th step:
We train a logistic regression and optimize our model with Grid Search CV function. 
We evaluate again with precision and recall.

#### As a conclusion, the SVC model with C=1e9 and gamma= 1e-07 is the best model to use in our case.
