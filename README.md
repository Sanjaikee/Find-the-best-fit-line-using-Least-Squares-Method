# Implementation of Univariate Linear Regression
## AIM:
To implement univariate Linear Regression to fit a straight line using least squares.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
Step1: Start the Program

Step2: Get the independent variable X and dependent variable Y.

Step3:Calculate the mean of the X -values and the mean of the Y -values.

Step4:Find the slope m of the line of best fit using the formula.

<img width="231" alt="image" src="https://user-images.githubusercontent.com/93026020/192078527-b3b5ee3e-992f-46c4-865b-3b7ce4ac54ad.png">

Step5: Compute the y -intercept of the line by using the formula:

<img width="148" alt="image" src="https://user-images.githubusercontent.com/93026020/192078545-79d70b90-7e9d-4b85-9f8b-9d7548a4c5a4.png">

Step6: Use the slope m and the y -intercept to form the equation of the line.

Step7: Obtain the straight line equation Y=mX+b and plot the scatterplot.

Step8: End the Program

## Program:
```
/*
Program to implement univariate Linear Regression to fit a straight line using least squares.
Developed by: Sanjai S
RegisterNumber:  212223230186
*/
```

```
import numpy as np
import matplotlib.pyplot as plt

#preprocessing Input data
X= np.array(eval(input()))
Y = np.array(eval(input()))

X_mean = np.mean(X)
Y_mean = np.mean(Y)
num =0  # for slope
denom=0  # for slope

# to find sume of (xi - x') & (yi-y') & (xi-x')^2
for i in range(len(X)):
    num += (X[i] - X_mean) * (Y[i]- Y_mean)
    denom += (X[i]- X_mean)**2

#calculate slope
m = num/denom

#calculate intercept
b= Y_mean - m*X_mean

print(m,b)

#Line equation
y_predicted=m*X+b
print(y_predicted)

#to plot the graph
plt.scatter(X,Y)
plt.plot(X,y_predicted,color='red')
plt.show()
```

## Output:
![image](https://github.com/user-attachments/assets/6c0c5cc2-265f-4c4c-9fd7-2f7e128bdc52)

![image](https://github.com/user-attachments/assets/c85ae3b8-4a3c-487e-ab82-b3ef3a18cd78)

X - Independent Variable
Y - Dependent Variable'

Linear Regression: y_predicted vs. X


![image](https://github.com/user-attachments/assets/6b90d861-0de2-4a8d-8af5-b287e7f0404e)

## Result:
Thus the univariate Linear Regression was implemented to fit a straight line using least squares using python programming.
