# Gaussian Elimination

## AIM:

To write a program to find the solution of a matrix using Gaussian Elimination.

## Equipments Required:

1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Moodle-Code Runner

## Algorithm

1.Get the matrix from user.

2.Using "from numpy as np sys" to import numpy (Ge).

3.Print the result matrices (Gaussian Elimination).

4.End the program.

## Program:
```
'''
Program to solve a matrix using Gaussian elimination with partial pivoting.
Developed by: SANJAY T
RegisterNumber: 212222110039
'''
import numpy as np
import sys
n=int(input())
a=np.zeros((n,n+1))
x=np.zeros(n)
for i in range (n):
    for j in range(n+1):
        a[i][j]=float(input())
for i in range (n):
    if a[i][i]==0.0:
        sys.exit('Divide by zero dectected!')
    for j in range(i+1,n):
        ratio=a[j][i]/a[i][i]
        for k in range(n+1):
            a[j][k]=a[j][k]-ratio*a[i][k]
x[n-1]=a[n-1][n]/a[n-1][n-1]
for i in range(n-2,-1,-1):
    x[i]=a[i][n]
    for j in range(i+1,n):
        x[i]=x[i]-a[i][j]*x[j]
    x[i]=x[i]/a[i][i]
for i in range(n):
    print('X%d = %0.2f'%(i,x[i]),end=' ')
```

## Output:

![6 maths](https://github.com/sanjaythiyagarajan/Gaussian/assets/119409242/d56c4b11-cb5a-4e04-aab5-6956dcab2d7a)


## Result

Thus the program to find the solution of a matrix using Gaussian Elimination is written and verified using python programming.

