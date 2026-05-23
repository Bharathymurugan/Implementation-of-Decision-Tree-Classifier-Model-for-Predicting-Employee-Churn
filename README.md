# Implementation-of-Decision-Tree-Classifier-Model-for-Predicting-Employee-Churn

## AIM:
To write a program to implement the Decision Tree Classifier Model for Predicting Employee Churn.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
1. Import the required libraries and load the employee dataset containing features related to employee performance and churn.
2. Split the dataset into input features and target labels, then divide it into training and testing datasets.
3. Train the Decision Tree Classifier model using the training dataset.
4. Predict employee churn using the trained model and evaluate the classification performance.

## Program:
```
/*
Program to implement the Decision Tree Classifier Model for Predicting Employee Churn.
Developed by: Bharathy M
RegisterNumber:  212225040046

import pandas as pd
from sklearn.model_selection import train_test_split
from sklearn.tree import DecisionTreeClassifier
from sklearn.metrics import confusion_matrix, accuracy_score, classification_report
from sklearn import tree
import matplotlib.pyplot as plt


data = {
    'satisfaction_level': [0.38, 0.80, 0.11, 0.72, 0.37, 0.41, 0.10, 0.92],
    'last_evaluation': [0.53, 0.86, 0.88, 0.87, 0.52, 0.50, 0.77, 0.89],
    'number_project': [2, 5, 7, 5, 2, 2, 6, 5],
    'average_monthly_hours': [157, 262, 272, 223, 159, 153, 247, 224],
    'time_spend_company': [3, 6, 4, 5, 3, 3, 4, 5],
    'Work_accident': [0, 0, 0, 0, 0, 0, 0, 0],
    'promotion_last_5years': [0, 0, 0, 0, 0, 0, 0, 0],
    'Departments': ['sales','accounting','hr','technical','support','management','marketing','product'],
    'salary': ['low','medium','medium','high','low','low','medium','high'],
    'left': [1, 1, 1, 1, 1, 0, 1, 0]  # Target variable: 1=Churn, 0=Stayed
}

df = pd.DataFrame(data)


df = pd.get_dummies(df, columns=['Departments','salary'], drop_first=True)


X = df.drop('left', axis=1)
y = df['left']


X_train, X_test, y_train, y_test = train_test_split(X, y, test_size=0.25, random_state=42)


dt_model = DecisionTreeClassifier(criterion='entropy', max_depth=4, random_state=42)
dt_model.fit(X_train, y_train)


y_pred = dt_model.predict(X_test)


print("Confusion Matrix:\n", confusion_matrix(y_test, y_pred))
print("\nAccuracy Score:", accuracy_score(y_test, y_pred))
print("\nClassification Report:\n", classification_report(y_test, y_pred))


plt.figure(figsize=(20,10))
tree.plot_tree(dt_model, feature_names=X.columns, class_names=['Stayed','Churn'], filled=True)
plt.show()

*/
```

## Output:
<img width="559" height="345" alt="image" src="https://github.com/user-attachments/assets/fd62cbe7-ef05-4fed-a86b-557e6008a0d4" />
<img width="1122" height="605" alt="image" src="https://github.com/user-attachments/assets/9f6a2e77-f4e2-4a4a-a2a7-d1e466d78035" />



## Result:
Thus the program to implement the  Decision Tree Classifier Model for Predicting Employee Churn is written and verified using python programming.
