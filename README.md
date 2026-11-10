# Algorithm for QR Decomposition
## Aim:
To implement QR decomposition algorithm using the Gram-Schmidt method.
## Equipment’s required:
1.	Hardware – PCs
2.	Anaconda – Python 3.7 Installation / Moodle-Code Runner
## Algorithm:
1.	Intialize the matrix Q and u
2.	The vector u and e is given by

    ![eqn1](./ex4.jpg)

    ![eqn2](./ex6.jpg)

    ![eqn3](./ex3.jpg)

3.	Obtain the Q matrix   
    ![eqn4](./ex1.jpg)
4.	Construct the upper triangular matrix R
    ![eqn5](./ex2.jpg)



## Program:
### Gram-Schmidt Method
```
''' 
Program to QR decomposition using the Gram-Schmidt method
Developed by: M.K. JEVVITH
RegisterNumber: 26018300
'''
import os
os.environ["OPENBLAS_NUM_THREADS"]="1"
import numpy as np
def QR_Decomposition(A):
    m,n=A.shape
    Q=np.zeros((n,n))
    R=np.zeros((n,n))
    for j in range(n):
        v=A[:,j]
        for i in range(j):
            R[i,j]=np.dot(Q[:,i],a[:,j])
            v=v-R[i,j]*Q[:,i]
        R[j,j]=np.linalg.norm(v)
        Q[:,j]=v/R[j,j]
    print(f"The Q Matrix is\n {Q}")
    print(f"The R Matrix is\n {R}")
a = np.array(eval(input()))
QR_Decomposition(a)






```

## Output
```
<img width="1920" height="1080" alt="Screenshot (101)" src="https://github.com/user-attachments/assets/2a1c58fc-1d3a-4048-a12a-742287ed9471" />

```

## Result
Thus the QR decomposition algorithm using the Gram-Schmidt process is written and verified the result.
