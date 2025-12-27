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
```py
import numpy as np 
import matplotlib.pyplot as plt

x=np.array([2,9,5,5,3,7,1,8,6,2])
y=np.array([69,98,82,77,71,84,55,94,84,64])

x_mean=np.mean(x)
y_mean=np.mean(y)

num = 0
denom=0
for i in range (len(x)):
    num+=(x[i]-x_mean)*(y[i]-y_mean)
    denom+=(x[i]-x_mean)**2
m=num/denom
b=y_mean-m*x_mean
print("Slope=",m,"Intercept=",b)

y_predicted = m*x+b
print("Y Predicted =", y_predicted)

plt.figure(figsize=(12,8))
plt.scatter(x,y,label='Data points')
plt.plot(x,y_predicted,color='red',linewidth=3,label='Regression Line')
plt.grid(True)
plt.show()
```
## Output
</br>
<img width="1066" height="711" alt="image" src="https://github.com/user-attachments/assets/423320cf-a6a3-4e03-89b2-4a3c746eed49" />

</br>

## Result
Thus the univariate Linear Regression was implemented to fit a straight line using least squares.
