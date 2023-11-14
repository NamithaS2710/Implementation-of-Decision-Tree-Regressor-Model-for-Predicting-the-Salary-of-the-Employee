# Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee

## AIM:
To write a program to implement the Decision Tree Regressor Model for Predicting the Salary of the Employee.
## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook
## Algorithm
1. Import the required libraries.
2. Upload the csv file and read the dataset.
3. Check for any null values using the isnull() function.
4. From sklearn.tree import DecisionTreeRegressor.
5. Import metrics and calculate the Mean squared error.
6. Apply metrics to the dataset, and predict the output.
## Program:
```
/*
Program to implement the Decision Tree Regressor Model for Predicting the Salary of the Employee.
Developed by: NAMITHA.S
RegisterNumber: 212221040110 
*/
```
```
import pandas as pd
data=pd.read_csv("/content/Salary.csv")
print("data.head():")
data.head()
print("data.info():")
data.info()
print("isnull() and sum():")
data.isnull().sum()
from sklearn.preprocessing import LabelEncoder
le=LabelEncoder()
data["Position"]=le.fit_transform(data["Position"])
print("data.head() for salary:")
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
print("MSE value:")
mse
r2=metrics.r2_score(y_test,y_pred)
print("r2 value:")
r2
print("data prediction:")
dt.predict([[5,6]])
```
## Output:
1. data.head()
![image](https://github.com/Jai-Pradhiksha/Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee/assets/100289733/71bc786f-650b-459a-b442-5a86de97a1e4)
2. data.info()
   ![image](https://github.com/Jai-Pradhiksha/Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee/assets/100289733/90a6bcc0-a652-4fd5-a9c4-e5305c56a2dc)
3. isnull() and sum()
   ![image](https://github.com/Jai-Pradhiksha/Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee/assets/100289733/bfe2fc8f-51e4-4140-9fc0-265fa0af93cb)
4. data.head() for salary
   ![image](https://github.com/Jai-Pradhiksha/Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee/assets/100289733/f6371e23-6aab-46cf-99b3-0a5f5a217b75)
5. MSE value
   ![image](https://github.com/Jai-Pradhiksha/Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee/assets/100289733/00578d8b-6065-415b-976d-38219fcb2fe3)
6. r2 value
   ![image](https://github.com/Jai-Pradhiksha/Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee/assets/100289733/ce5bd277-4caa-40f5-8a29-d9793c577b6e)
7. Data prediction
   ![image](https://github.com/Jai-Pradhiksha/Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee/assets/100289733/627e1674-1479-492d-b845-a79c9fd498e2)                                                                                                                                                                                                                                                                                                                                                                                                                                                              
                                                                                                                                                                                                                                                                                                                                                                                                         
## Result:
Thus the program to implement the Decision Tree Regressor Model for Predicting the Salary of the Employee is written and verified using python programming.
