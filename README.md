# EX07 Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee

## AIM:
To write a program to implement the Decision Tree Regressor Model for Predicting the Salary of the Employee.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
1. Import the libraries and read the data frame using pandas.

2.Calculate the null values present in the dataset and apply label encoder.

3.Determine test and training data set and apply decison tree regression in dataset.

4.calculate Mean square error,data prediction and r2.


## Program:
```
/*
Program to implement the Decision Tree Regressor Model for Predicting the Salary of the Employee.
Developed by: vdhyasri.k
RegisterNumber:  212222230170

import pandas as pd
data=pd.read_csv("/content/Salary.csv")

data.head()

data.info()

data.isnull().sum()

from sklearn.preprocessing import LabelEncoder
le=LabelEncoder()
data["Position"]=le.fit_transform(data["Position"])
data.head()

x=data[["Position","Level"]]
y=data["Salary"]

from sklearn.model_selection import train_test_split
x_train,x_test,y_train,y_test=train_test_split(x,y,test_size=0.2,random_state=2)


from sklearn.tree import DecisionTreeRegressor
dt=DecisionTreeRegressor()
dt.fit(x_train,y_train)
y_pred=dt.predict(x_test)

from sklearn import metrics
mse=metrics.mean_squared_error(y_test,y_pred)
mse

r2=metrics.r2_score(y_test,y_pred)
r2

dt.predict([[5,6]])
  
```

## Output:
data.head()

![image](https://github.com/vidhyasrikachapalayam/Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee/assets/119477817/8aa49f07-7195-4acc-83e3-a07d6482301a)

data.info()

![image](https://github.com/vidhyasrikachapalayam/Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee/assets/119477817/e9a5d1f3-7313-4fbe-b482-7aeb537225c8)

data.isnull().sum()

![image](https://github.com/vidhyasrikachapalayam/Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee/assets/119477817/6e54f549-8f09-4065-bfd7-b9ce22ac7ac8)

data.head() for salary

![image](https://github.com/vidhyasrikachapalayam/Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee/assets/119477817/cb8dad28-427d-4885-896f-2045166954e2)

MSE value

![image](https://github.com/vidhyasrikachapalayam/Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee/assets/119477817/4612da44-b1e3-4326-8329-8e24e5fc88ae)

r2 value

![image](https://github.com/vidhyasrikachapalayam/Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee/assets/119477817/834098d3-e378-4ecb-92f5-1c3c2d334e0e)
data prediction


![image](https://github.com/vidhyasrikachapalayam/Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee/assets/119477817/42d4688e-8bb6-4d71-9cc9-178275938a47)


## Result:
Thus the program to implement the Decision Tree Regressor Model for Predicting the Salary of the Employee is written and verified using python programming.
