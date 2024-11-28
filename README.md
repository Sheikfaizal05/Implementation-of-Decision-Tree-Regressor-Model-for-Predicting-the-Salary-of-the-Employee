# Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee

## AIM:
To write a program to implement the Decision Tree Regressor Model for Predicting the Salary of the Employee.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
1.Import pandas

2.Import Decision tree classifier

3.Fit the data in the model

4.Find the accuracy score
## Program:
```
/*
Program to implement the Decision Tree Regressor Model for Predicting the Salary of the Employee.
Developed by: SHEIK FAIZALS
RegisterNumber:24900982
*/
```
```
import pandas as pd
data=pd.read_csv("Salary.csv")
data.head()
data.info()
data.isnull().sum()
from sklearn.preprocessing import LabelEncoder
le=LabelEncoder()
data["Position"]=le.fit_transform(data["Position"])
data.head()
x=data[["Position","Level"]]
x.head()
y=data["Salary"]
y.head()
from sklearn.model_selection import train_test_split
x_train,x_test,y_train,y_test=train_test_split(x,y,test_size=0.2,random_state=2)
from sklearn.tree import DecisionTreeRegressor
dt=DecisionTreeRegressor()
dt.fit(x_train,y_train)
y_pred=dt.predict(x_test)
y_pred
from sklearn.metrics import r2_score
r2=r2_score(y_test,y_pred)
R2 score:  0.48611111111111116
dt.predict([[5,6]])
```

## Output:
![Screenshot 2024-11-28 161719](https://github.com/user-attachments/assets/79073eb5-0130-4368-a388-38ac22aa8219)
![Screenshot 2024-11-28 161826](https://github.com/user-attachments/assets/682984d9-2918-46ba-b965-36cd7febaa61)
![Screenshot 2024-11-28 161911](https://github.com/user-attachments/assets/bef3d02a-fc9c-4187-9427-f243afae760f)
![Screenshot 2024-11-28 161921](https://github.com/user-attachments/assets/31f57635-8436-43f8-97a1-4502db10cc76)
![Screenshot 2024-11-28 162607](https://github.com/user-attachments/assets/f41e5c34-1225-468b-b5a7-be0a0699d47b)
![Screenshot 2024-11-28 162707](https://github.com/user-attachments/assets/c4e02de6-102c-4b1a-8a5c-d2b87db2b1ea)


## Result:
Thus the program to implement the Decision Tree Regressor Model for Predicting the Salary of the Employee is written and verified using python programming.
