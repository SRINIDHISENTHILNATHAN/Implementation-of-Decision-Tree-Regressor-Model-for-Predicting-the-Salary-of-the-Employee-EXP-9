# Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee

## AIM:
To write a program to implement the Decision Tree Regressor Model for Predicting the Salary of the Employee.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
1. Import the standard libraries.
2. Upload the dataset and check for any null values using .isnull() function.
3. Import LabelEncoder and encode the dataset.
4. Import DecisionTreeRegressor from sklearn and apply the model on the dataset.
5. Predict the values of arrays.
6. Import metrics from sklearn and calculate the MSE and R2 of the model on the dataset.
7. Predict the values of array.
8. Apply to new unknown values.
## Program:
### DATA SET
```

Program to implement the Decision Tree Regressor Model for Predicting the Salary of the Employee.
Developed by: SRINIDHI SENTHIL
RegisterNumber:  212222230148
import pandas as pd
data=pd.read_csv("Salary.csv")
data.head()
```
### INFO
```
data.info()
```
### DATA FRAME 
```
data.isnull().sum()
```
### LABEL ENCORDER
```
from sklearn.preprocessing import LabelEncoder
le=LabelEncoder()
data["Position"]=le.fit_transform(data["Position"])
data.head()
```
### X DATA,Y DATA
```
x=data[["Position","Level"]]
y=data["Salary"]
```
### TREE DATA SET
```
from sklearn.model_selection import train_test_split
x_train,x_test,y_train,y_test=train_test_split(x,y,test_size=0.2,random_state=2)
```
### DECISIONTREE REGRESSOR
```
from sklearn.tree import DecisionTreeRegressor
dt=DecisionTreeRegressor()
dt.fit(x_train,y_train)
y_pred=dt.predict(x_test)
```
### METRICES
```
from sklearn import metrics
mse=metrics.mean_squared_error(y_test,y_pred)
mse
```
### METRICES SCORE
```
r2=metrics.r2_score(y_test,y_pred)
r2
```
### PREDICET
```
dt.predict([[5,6]])
```

## Output:
### DATA SET

![image](https://github.com/user-attachments/assets/76806611-fe56-4902-9b81-e7ef9ac62353)

### INFO

![image](https://github.com/user-attachments/assets/2282c30a-9da9-4eca-8769-7a7caf24aaea)

### DATA FRAME 

![image](https://github.com/user-attachments/assets/a7ab3e69-791c-408e-8c01-d0fd900ab989)

### LABEL ENCORDER

![image](https://github.com/user-attachments/assets/4ea06fcb-d3b4-49c1-b474-42d682d7b660)

### METRICES

![image](https://github.com/user-attachments/assets/1b0c585f-df9a-4dfa-95cc-9c6ae9ddb309)

### METRICES SCORE
![image](https://github.com/user-attachments/assets/8050204b-7f79-4a3e-8b01-ba8604a289be)

### PREDICT
![image](https://github.com/user-attachments/assets/a8d8c5ac-9f8b-4693-93fa-16c8f019f4c2)


## Result:
Thus the program to implement the Decision Tree Regressor Model for Predicting the Salary of the Employee is written and verified using python programming.
