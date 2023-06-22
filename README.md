# RANK-OF-A-MATRIX

## Aim:
To write a python program to find the rank of a matrix

## Equipment’s required:
1. 	Hardware – PCs
2. 	Anaconda – Python 3.7 Installation / Moodle-Code Runner

## Algorithm:

### Step 1: Import numpy package
### Step 2: Get the input matrix
### Step 3: Find the rank of the matrix
### Step 4: Print the result

## Program:
```python
#Program to find the rank of a matrix.
#Developed by: Selva Kumar A
#RegisterNumber:22009007
import numpy as np
a=np.array([[1,2,3,],[3,6,9]])
b=np.linalg.matrix_rank(a)
print(b)
```
~~~ python
ex 1 Newton - Raphson method
~~~
![image](https://github.com/Selvakumar525/RANK-OF-A-MATRIX/assets/120643262/587741a0-a420-4c65-8ca7-71bdf7156eac)
~~~
Program:
def f(x):
    return x**3-x-2
def f1(x):
    return 3*x**2-1
xo=float (input ("Enter the initial approximation: "))
for i in range (1,10):
    xn=xo-f(xo)/f1(xo)
    xo=xn
print ("The approximate root using Newton-Raphson method is %.4f"%xn)
~~~
~~~ python
ex 2 Gauss - Seidel method
~~~
![image](https://github.com/Selvakumar525/RANK-OF-A-MATRIX/assets/120643262/272ddae4-771c-4837-a8ed-f2b27c860613)
x0=0; y0=0; z0=0
for i in range (1,10):
    x=1/4*(1-y0-z0)
    x0=x
    y=1/3*(2-x0-z0)
    y0=y
    z=1/5*(3-x0-y0)
    z0=z
print ("The approximate solution of x = %.4f, y= %.4f, z=%.4f"%(x, y,z))
~~~
~~~ python
ex 3 Lagrange’s Interpolation method
~~~
![image](https://github.com/Selvakumar525/RANK-OF-A-MATRIX/assets/120643262/f205bd83-723d-4f2e-b72b-413640bcf901)
x= [0,1,2,4,5,6]
y= [1,14,15,5,6,19]
s=float (input ("Enter the value of x to be in: "))
sum=0
for i in range (0,6):
    prod=1
    for j in range (0,6):
          if i!=j:
                prod=prod*(s-x[j])/(x[i]-x[j])
   sum=sum+prod*y[i]
print ("The functional value is %.4f"%sum)
~~~
~~~ python
ex 4 trapezoidal rule
![image](https://github.com/Selvakumar525/RANK-OF-A-MATRIX/assets/120643262/426d825e-ed10-434d-91ca-4453c46ef24b)
def f(x):
    return 1/(1+x**2)
a=float (input ("Enter the lower limit: "))
b=float (input ("Enter the upper limit: "))
h=float (input ("Enter the step size: "))
n=int((b-a)/h)
sum=0
for i in range (1, n):
    sum=sum+f(a+i*h)
trap=h/2*(f(a)+f(b)+2*sum)
print ("The Integral value is %.5f"%trap)
~~~
~~~ python
ex 5  Runge-Kutta method of fourth order
![image](https://github.com/Selvakumar525/RANK-OF-A-MATRIX/assets/120643262/0861a72d-aa19-436d-9b2c-d1411d1fa5b1)
def f (x, y):
    return x+y**2
x0=float (input ("Enter initial point of x: "))
y0=float (input ("Enter initial point of y: "))
h=float (input ("Enter step value h: "))
k1=h*f (x0, y0)
k2=h*f (x0+h/2,y0+k1/2)
k3=h*f (x0+h/2,y0+k2/2)
k4=h*f (x0+h,y0+k3)
y=y0+(k1+2*k2+2*k3+k4)/6
print ("The value of y using RK method is %.4f"%y)
~~~
~~~ python
ex 6 Adam’s predictor and corrector method
![image](https://github.com/Selvakumar525/RANK-OF-A-MATRIX/assets/120643262/704f59d5-d47e-49ba-ae09-79520d2f7ebe)
def f (x, y):
return x**2*(1+y)
x0=float (input ("Enter x0: "))
y0=float (input ("Enter y0: "))
x1=float (input ("Enter x1: "))
y1=float (input ("Enter y1: "))
x2=float (input ("Enter x2: "))
y2=float (input ("Enter y2: "))
x3=float (input ("Enter x3: "))
y3=float (input ("Enter y3: "))
h =0.1
y4p=y3+(h/24) *(55*f(x3,y3)-59*f(x2,y2)+37*f(x1,y1)-9*f(x0,y0))
x4=x3+h
y4c=y3+(h/24) *(9*f(x4,y4p) +19*f(x3,y3)-5*f(x2,y2)+f(x1,y1))
print ("Approximate soln is %0.4f"%y4c)
~~~

## Output:
![](Rank%20of%20a%20matrix.png)

## Result:
Thus the rank for the given matrix is successfully solved by  using a python program.
