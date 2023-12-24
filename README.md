# Implementation of Univariate Linear Regression
## Aim:
To implement univariate Linear Regression to fit a straight line using least squares.
## Equipment’s required:
1.	Hardware – PCs
2.	Anaconda – Python 3.7 Installation / Moodle-Code Runner
## Algorithm:
1.	Get the independent variable X and dependent variable Y.
2.	Calculate the mean of the X -values and the mean of the Y -values.
3.	Find the slope m of the line of best fit using the formula.
 ![eqn1](./eq1.jpg)
4.	Compute the y -intercept of the line by using the formula:
![eqn2](./eq2.jpg)  
5.	Use the slope m and the y -intercept to form the equation of the line.
6.	Obtain the straight line equation Y=mX+b and plot the scatterplot.
## Program
```
##Program for Univariate linear regression using the least squares method.
#Developed by: KARTHIKEYAN M
#Register no: 23005191

import numpy as np
import matplotlib.pyplot as py
x=np.array([0,1,2,3,4,5,6,7,8,9])
y=np.array([9,8,7,6,5,4,3,2,1,0])
x_mean=np.mean(x)
y_mean=np.mean(y)
num,denom=0,0
for i in range (len(x)):
    num+=(x[i]-x_mean)*(y[i]-y_mean)
    denom+=(x[i]-x_mean)**2
m=num/denom
b=y_mean-(m*x_mean)
print(m,b)
y_pred=(m*x)+b
print(y_pred)
py.scatter(x,y,color='pink')
py.plot(x,y_pred,color='blue')
py.show()

```
## Output
![Screenshot 2023-12-24 223503](https://github.com/karthik-2106/Univariate-Linear-Regression/assets/150319557/27a387e5-1cc2-4d75-ba7d-740c42434c74)
![Screenshot 2023-12-24 223521](https://github.com/karthik-2106/Univariate-Linear-Regression/assets/150319557/2e6fc866-ae1a-4c8f-ba58-ed000c06e80a)

## Result
Thus the univariate Linear Regression was implemented to fit a straight line using least squares.
