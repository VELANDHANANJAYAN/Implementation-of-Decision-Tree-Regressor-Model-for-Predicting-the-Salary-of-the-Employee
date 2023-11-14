# Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee

## AIM:
To write a program to implement the Decision Tree Regressor Model for Predicting the Salary of the Employee.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
1.Import the required libraries .

2.Read the data frame using pandas.

3.Get the information regarding the null values present in the dataframe.

4.Apply label encoder to the non-numerical column inoreder to convert into numerical values.

5.Determine training and test data set.

6.Apply decision tree regression on to the dataframe.

7.Get the values of Mean square error, r2 and data prediction.

## Program:
Program to implement the Decision Tree Regressor Model for Predicting the Salary of the Employee.
Developed by: VELAN D
RegisterNumber:  212222040176
data=pd.read_csv("Salary Data.csv")
data.head()
data.tail()
data.info()
data["Gender"]=data["Gender"].astype('category')
data["Education Level"]=data["Education Level"].astype('category')
data["Job Title"]=data["Job Title"].astype('category')
data.info()
data["Gender"]=data["Gender"].cat.codes
data["Education Level"]=data["Education Level"].cat.codes
data["Job Title"]=data["Job Title"].cat.codes
data.info()
data.head()
x=data[['Age','Gender','Education Level','Job Title','Years of Experience']]
x
x.shape
y=data[['Salary']]
y.shape
from sklearn.model_selection import train_test_split
x_train, x_test, y_train, y_test = train_test_split(x, y, test_size=0.2, random_state=2)
from sklearn.tree import DecisionTreeRegressor
dtr=DecisionTreeRegressor()
dtr.fit(x_train,y_train)
y_pred=dtr.predict(x_test)
print(y_pred)
x_train.shape
from sklearn import metrics
mse=metrics.mean_squared_error(y_test,y_pred)
mse
r2=metrics.r2_score(y_test,y_pred)
r2
dtr.predict([[44,0,2,130,20]])

## Output:
READ CSV HEAD FILE:
![280455431-3ffb504d-a7a1-4b42-b749-0f3258bcf656](https://github.com/VELANDHANANJAYAN/Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee/assets/119405038/6e6326ed-a1ef-4cce-8e6c-a5aa8619bd1a)
TAIL:
![280455469-79f6f7b2-e790-4c46-9b7b-f571c25ede2f](https://github.com/VELANDHANANJAYAN/Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee/assets/119405038/21a70f7b-8314-407f-8186-5512bb68b223)
DATASET INFO:
![280455480-271d7609-b28e-4831-8171-6c39b47a5d20](https://github.com/VELANDHANANJAYAN/Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee/assets/119405038/64f3119e-85a6-4d56-b561-b1c19627c96c)
![280455490-f73952ba-feef-4e59-b81b-641792c23306](https://github.com/VELANDHANANJAYAN/Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee/assets/119405038/99d45631-6483-4783-a049-ec03a933fe88)
![280455495-d3f6e59b-b67d-414c-a0cd-9ce4e5299dc4](https://github.com/VELANDHANANJAYAN/Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee/assets/119405038/36b7b32d-5539-4f74-991c-79a79f15fc6a)
![280455503-fbab1c96-a847-49e5-9506-4f00c69fa18e](https://github.com/VELANDHANANJAYAN/Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee/assets/119405038/16a0f0a0-3671-45a2-803c-b194c3360a1a)

X-DATA:
![280455514-87c15651-41cf-479b-ae52-02199bca48d2](https://github.com/VELANDHANANJAYAN/Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee/assets/119405038/b4541c9b-8ce8-43ce-9a70-b6d594ed03dd)

DATA SHAPE:
![280455538-b13e6c8c-9715-4102-be85-56028ac0ad1b](https://github.com/VELANDHANANJAYAN/Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee/assets/119405038/848381e3-0e6c-41e8-9205-cca9e0ee3340)

Y_PRED:
![280455553-674e7856-c6c6-4897-8ad2-d4ac3827c18f](https://github.com/VELANDHANANJAYAN/Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee/assets/119405038/e20b2501-4c9d-417e-be2c-471c3e844028)

MEAN SQUARED VALUE:
![280455571-ff568d12-9386-458b-8798-27dc71ba0ceb](https://github.com/VELANDHANANJAYAN/Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee/assets/119405038/894df431-91bd-431b-be19-11abb6e76da9)

R2 VALUE:
![280455583-f41bcce2-bce0-460f-970a-d4401fb4b4bf-1](https://github.com/VELANDHANANJAYAN/Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee/assets/119405038/a636f23c-9fe3-4621-b187-e8db568e647f)

DTR PREDICT:
![280455589-557c20fa-1ba0-43c1-a323-41cbed452f87](https://github.com/VELANDHANANJAYAN/Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee/assets/119405038/8c4b719c-7c0c-465b-a381-d75188f42444)


## Result:
Thus the program to implement the Decision Tree Regressor Model for Predicting the Salary of the Employee is written and verified using python programming.
