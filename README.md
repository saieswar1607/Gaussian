# Gaussian Elimination

## AIM:
To write a program to find the solution of a matrix using Gaussian Elimination.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Moodle-Code Runner

## Algorithm
1. Start the program.
2. Import numpy and Import sys
3. Get input from the user.
4. Solve the matrix in Guassian Elimination method.
5. Display the values.
6. Stop the program.

## Program:
```
'''
Program to solve a matrix using Gaussian elimination with partial pivoting.
Developed by: K. Sai Eswar
RegisterNumber: 21000679
'''
import numpy as np
import sys
n=int(input())
a=np.zeros((n,n+1))
x=np.zeros(n)
for i in range (n):
    for j in range (n+1):
        a[i][j]=float(input())
for i in range (n):
    if a[i][i]==0:
        sys.exit('Divide by zero detected!')
    for j in range (i+1,n):
        ratio=a[j][i]/a[i][i]
        for k in range (n+1):
            a[j][k]=a[j][k]-ratio*a[i][k]
x[n-1]=a[n-1][n]/a[n-1][n-1]
for i in range (n-2,-1,-1):
    x[i]=a[i][n]
    for j in range(i+1,n):
        x[i]=x[i]-a[i][j]*x[j]
    x[i]=x[i]/a[i][i]
for i in range(n):
      print('X%d = %0.2f' %(i,x[i]), end = ' ')

```

## Output:
![gaussian elimination](./ge.png)


## Result:
Thus the program to find the solution of a matrix using Gaussian Elimination is written and verified using python programming.

