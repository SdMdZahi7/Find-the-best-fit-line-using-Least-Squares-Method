# Implementation of Univariate Linear Regression
## AIM:
To implement univariate Linear Regression to fit a straight line using least squares.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
1. Get the independent variable X and dependent variable Y.
2. Calculate the mean of the X -values and the mean of the Y -values.
3. Find the slope m of the line of best fit using the formula. 
<img width="231" alt="image" src="https://user-images.githubusercontent.com/93026020/192078527-b3b5ee3e-992f-46c4-865b-3b7ce4ac54ad.png">
4. Compute the y -intercept of the line by using the formula:
<img width="148" alt="image" src="https://user-images.githubusercontent.com/93026020/192078545-79d70b90-7e9d-4b85-9f8b-9d7548a4c5a4.png">
5. Use the slope m and the y -intercept to form the equation of the line.
6. Obtain the straight line equation Y=mX+b and plot the scatterplot.

## Program:
~~~
Program to implement univariate Linear Regression to fit a straight line using least squares.
Developed by: SYED MUHAMMED ZAHI
RegisterNumber: 212221230114
#import libraries
import numpy as np
import matplotlib.pyplot as plt

#assign input
X=np.array([0,1,2,3,4,5,6,7,8,9])
Y=np.array([1,3,2,5,7,8,8,9,10,12])

# mean values of input
X_mean=np.mean(X)
print("X_mean =",X_mean)
Y_mean=np.mean(Y)
print("y_mean =",Y_mean)

num=0
denum=0
for i in range(len(X)):
  num+=(X[i]-X_mean)*(Y[i]-Y_mean)
  denum+=(X[i]-X_mean)**2

# find m
print("find m")
m=num/denum
print("m=",m)

# find b
print("find b")
b=(Y_mean)-(m*X_mean)
print("b =",b)

# find Y_pred
print("find Y_pred")
Y_pred=m*X+b
print("Y_pred =",Y_pred)

#plot graph
plt.scatter(X,Y,color='orange')
plt.plot(X,Y_pred,color='maroon')
print("Graph")
plt.show()
~~~

## Output:
![image](https://user-images.githubusercontent.com/94187572/198179654-42a13297-bc41-4c9b-b5bf-b8c5f9a8dc50.png)
![image](https://user-images.githubusercontent.com/94187572/198179692-8b4f691f-f692-4281-8a5f-29fc0017ed84.png)
![image](https://user-images.githubusercontent.com/94187572/198179717-feeba955-e2e2-40a5-ab17-fd42ff9e6534.png)
## Result:
Thus the univariate Linear Regression was implemented to fit a straight line using least squares using python programming.
