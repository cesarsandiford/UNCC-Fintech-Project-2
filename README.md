# Loan Default Prediction

Using Maching Learning in order to predict high risk customers if they default on their loans.

### 1. Import the requires Libraries

Importing the necessary libraries to fit the model.
`import numpy as np
import pandas as pd
from pathlib import Path
from sklearn.model_selection import train_test_split
from sklearn.linear_model import LogisticRegression
from imblearn.over_sampling import RandomOverSampler
from sklearn.metrics import balanced_accuracy_score
from sklearn.metrics import confusion_matrix
from imblearn.metrics import classification_report_imbalanced`

import warnings
warnings.filterwarnings('ignore')

### 2. Load the CSV file into a Pandas dataframe

Loading the csv file in google colab `from google colab import files`


### 3. Separate the data into labels and features

1. Separate `y` for defaulted column.

2. Separate `x` to drop defaulted column.

    

### 4. Plot the clusters using the x for "Loan" and y for "Bank Balance"



### 5. Check the balance of our target values
`y.value_counts()`
     
`0    967 good standing`
`1     33 defaulted`


### 6. Split the data using train_test_split and Instantiate the Logistic Regression model to fit.

`lr = LogisticRegression(random_state=1)`
`lr.fit(X_train, y_train)`

### 7. Make a prediction using the testing data
`y_pred = lr.predict(X_test)`

`results = pd.DataFrame({
    "Prediction": y_pred, 
    "Actual": y_test
}).reset_index(drop=True)`

Then print the results.


### 8. Print the balanced_accuracy score of the model
`print(balanced_accuracy_score(y_test, y_pred))`


### 9. Generate a confusion matrix for the model
`print(confusion_matrix(y_test, y_pred))`


### 10. Print the classification report for the model
`print(classification_report_imbalanced(y_test, y_pred))`


### 11. Predict a Logistic Regression Model with Resampled Training Data (Repeat process)



## Created by: 

Cesar Sandiford






