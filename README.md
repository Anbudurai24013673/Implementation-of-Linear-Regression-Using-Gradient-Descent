# Implementation-of-Linear-Regression-Using-Gradient-Descent

## AIM:
To write a program to predict the profit of a city using the linear regression model with gradient descent.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
1. Import all the required packages.
2. Display the output values using graphical representation tools as scatter plot and graph.
3. predict the values using predict() function.
4. Display the predicted values and end the program

## Program:
```
/*
Program to implement the linear regression using gradient descent.
Developed by: Anbudurai A
RegisterNumber:  212224230018

import numpy as np
import pandas as pd
from sklearn.preprocessing import StandardScaler
def linear_regression(X1,y,learning_rate=0.01,num_iters=1000):
    X=np.c_[np.ones(len(X1)),X1]
    theta=np.zeros(X.shape[1]).reshape(-1,1)
    for _ in range(num_iters):
        predictions=(X).dot(theta).reshape(-1,1)
        errors=(predictions - y).reshape(-1,1)
        theta-=learning_rate*(1/len(X1))*X.T.dot(errors)
    return theta
data=pd.read_csv('50_Startups.csv',header=None)
print(data.head())
X=(data.iloc[1:, :-2].values)
print(X)
X1=X.astype(float)
scaler=StandardScaler()
y=(data.iloc[1:,-1].values).reshape(-1,1)
print(y)
X1_scaled=scaler.fit_transform(X1)
Y1_scaled=scaler.fit_transform(y)
print(X1_scaled)
print(Y1_scaled)
theta=linear_regression(X1_scaled,Y1_scaled)
new_data=np.array([165349.2,136897.8,471784.1]).reshape(-1,1)
new_Scaled=scaler.fit_transform(new_data)
prediction=np.dot(np.append(1,new_Scaled),theta)
prediction=prediction.reshape(-1,1)
pre=scaler.inverse_transform(prediction)
print(f"Predicted value: {pre}")

*/
```

## Output:
![image](https://github.com/user-attachments/assets/cd97a252-f5e5-4ec2-867a-a9c29678d9bb)
![image](https://github.com/user-attachments/assets/06c794b9-a144-46a6-bd88-bcd5e977a13f)
![image](https://github.com/user-attachments/assets/e5b07817-ea53-4e19-8d06-fa86b5a91529)
![image](https://github.com/user-attachments/assets/bce4d37c-7e42-44eb-bc22-097d69340a42)
![image](https://github.com/user-attachments/assets/cc65a143-94c2-491a-a750-90ea9674ae97)







## Result:
Thus the program to implement the linear regression using gradient descent is written and verified using python programming.
