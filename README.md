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
import numpy as np
import matplotlib.pyplot as plt
x = np.array([0,1,2,3,4,5,6,7,8,9])
y = np.array([1,3,2,5,7,8,8,9,10,12])
plt.scatter(x,y)
plt.show()
xmean = np.mean(x)
ymean = np.mean(y)
num=0
den=0
for i in range(len(x)):
    num+=(x[i]-xmean)*(y[i]-ymean)
    den+=(x[i]-xmean)**2
m = num/den
b = ymean - m*xmean
print(m,b)
ypred = m*x+b
print(ypred)
plt.scatter(x,y,color='Red')
plt.plot(x,ypred,color='Blue')
plt.show()
```
## Output
<img width="997" height="576" alt="Screenshot 2026-11-23 201839" src="https://github.com/user-attachments/assets/9b6663d0-fdbb-42ed-ac18-8b25b8fd80a9" />

<img width="993" height="625" alt="Screenshot 2026-11-23 201914" src="https://github.com/user-attachments/assets/58a31208-4bcf-4235-ab0e-8423f25680af" />

<img width="1000" height="603" alt="Screenshot 2026-11-23 201935" src="https://github.com/user-attachments/assets/24f58ff4-b172-4ba0-af46-839c75f1ffd8" />

## Result
Thus the univariate Linear Regression was implemented to fit a straight line using least squares.
