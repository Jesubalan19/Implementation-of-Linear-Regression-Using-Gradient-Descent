# Implementation-of-Linear-Regression-Using-Gradient-Descent

## AIM:
To write a program to predict the profit of a city using the linear regression model with gradient descent.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
1. Import the required library and read the dataframe.
2. Write a function computeCost to generate the cost function.
3. Perform iterations og gradient steps with learning rate.
4. Plot the Cost function using Gradient Descent and generate the required graph.

## Program:
```
/*
Program to implement the linear regression using gradient descent.
Developed by: Jesubalan A
RegisterNumber: 212223240060

import numpy as np
import pandas as pd
from sklearn.preprocessing import StandardScaler
def linear_regression(X1, y, learning_rate=0.01, num_iters=1000):
    X = np.c_[np.ones(len(X1)), X1]
    theta = np.zeros(X.shape[1]).reshape(-1,1)

    for _ in range(num_iters):
        predictions = (X).dot (theta).reshape(-1, 1)
        errors = (predictions - y).reshape(-1,1)
        theta -= learning_rate * (1/ len(X1)) * X.T.dot (errors)
    
    return theta
data = pd.read_csv('50_Startups.csv',header=None)
print(data.head())
X=(data.iloc[1:, :-2].values)
print(X)
X1=X.astype(float)
scaler=StandardScaler()
y = (data.iloc[1:,-1].values).reshape(-1,1)
print(y)
X1_Scaled = scaler.fit_transform(X1)
Y1_Scaled = scaler.fit_transform(y)
print(X1_Scaled)
print(Y1_Scaled)

theta = linear_regression(X1_Scaled, Y1_Scaled)

new_data = np.array([165349.2,136897.8,471784.1]).reshape(-1,1)
new_Scaled = scaler.fit_transform(new_data)
prediction = np.dot(np.append(1, new_Scaled), theta)
prediction = prediction.reshape(-1,1)
pre = scaler.inverse_transform(prediction)
print(f"Predicition value: {pre}")  
*/
```

## Output:
![Screenshot 2024-03-15 104001](https://github.com/Jesubalan19/Implementation-of-Linear-Regression-Using-Gradient-Descent/assets/144979294/12f693fc-1365-4e3a-86c7-96318313106b)
![Screenshot 2024-03-15 104023](https://github.com/Jesubalan19/Implementation-of-Linear-Regression-Using-Gradient-Descent/assets/144979294/73e99353-2cec-4e7d-9477-91c36cfc2670)
![Screenshot 2024-03-15 104103](https://github.com/Jesubalan19/Implementation-of-Linear-Regression-Using-Gradient-Descent/assets/144979294/2139f218-e118-499d-a425-107f3f316e33)
![Screenshot 2024-03-15 104118](https://github.com/Jesubalan19/Implementation-of-Linear-Regression-Using-Gradient-Descent/assets/144979294/277bd557-522c-4273-b8ba-3fd693097d84)


## Result:
Thus the program to implement the linear regression using gradient descent is written and verified using python programming.
