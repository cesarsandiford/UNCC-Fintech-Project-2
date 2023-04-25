# Loan Default Prediction

This project is about using machine learning to predict loan defaults with given data about customers with a Supervised model.
In times of uncertainty, FinTechs are in big risk when it comes to higher percentage of loan defaults and using machine learning to understand and identify the risk is very important to have in hand so they can make decisions to raise the credit standards in the future and minimize risk.


### 1. Import the requires Libraries

Importing the necessary libraries to fit the model.

`import numpy as np`
`import pandas as pd`
`from pathlib import Path`
`from sklearn.model_selection import train_test_split`
`from sklearn.linear_model import LogisticRegression`
`from imblearn.over_sampling import RandomOverSampler`
`from sklearn.metrics import balanced_accuracy_score`
`from sklearn.metrics import confusion_matrix`
`from imblearn.metrics import classification_report_imbalanced`

import warnings
warnings.filterwarnings('ignore')

### 2. Load the CSV file into a Pandas dataframe

Loading the csv file in google colab `from google colab import files`

<img width="773" alt="Screenshot 2023-04-24 at 8 08 00 PM" src="https://user-images.githubusercontent.com/112976523/234141907-4cf3fbd4-98e6-47b0-aa61-0c2ddd6d8ed0.png">

### 3. Separate the data into labels and features

1. Separate `y` for defaulted column.

2. Separate `x` to drop defaulted column.

    <img width="712" alt="Screenshot 2023-04-24 at 8 08 14 PM" src="https://user-images.githubusercontent.com/112976523/234142413-7d202284-a132-4859-9287-7caded78380e.png">

### 4. Plot the clusters using the `x` for "Loan" and `y` for "Bank Balance"

<img width="411" alt="Screenshot 2023-04-24 at 8 08 30 PM" src="https://user-images.githubusercontent.com/112976523/234142806-fea8a17b-2fe8-41d1-8ee8-30412dd801d9.png">


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

Then print the `results`.


### 8. Print the balanced_accuracy score of the model
`print(balanced_accuracy_score(y_test, y_pred))`


### 9. Generate a confusion matrix for the model
`print(confusion_matrix(y_test, y_pred))`


### 10. Print the classification report for the model
`print(classification_report_imbalanced(y_test, y_pred))`

<img width="676" alt="Screenshot 2023-04-24 at 8 18 49 PM" src="https://user-images.githubusercontent.com/112976523/234143353-8121824f-16d9-48ef-8929-e0132324ec65.png">


### 11. Predict a Logistic Regression Model with Resampled Training Data (Repeat process)

## Final with Classification Report Oversampled

<img width="653" alt="Screenshot 2023-04-24 at 8 08 53 PM" src="https://user-images.githubusercontent.com/112976523/234142886-57143617-479c-4f06-8785-47d95626502f.png">




### Conclusion:
By having the Logistic Regression model applied to the dataset, the balanced accuracy score was 58% meaning it was not too accurate. Since the data was imbalanced by the defaults, I gave it a proper chance by oversampling it to increase the accuracy of the mode up to 84%. Huge improvement! F1 score average was 94 vs the resampled average was 90. In conclusion, Oversampling the model brings a better prediction for this situation. Also, predicting defaults can be difficult given that customers could have different lifestyle, emergencies, unexpected situation or money opportunities in life.





## Created by: 

Cesar Sandiford






