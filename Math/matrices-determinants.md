# Matrices & Determinants

A practice set for Latex and Numpy on the topic of Matrices and Determinants.
How to use this notebook:

1. Use the "Run" button to execute the code.
2. Select binder or collab
3. Once the binder window is open, Click Kernel-restart and run all.

Contact:
[Royce]()
[Durvish]()

#### Given: 
\begin{equation}
A= \left( \begin{array}{ccc}
    2 &    1 &   4\\
  3 &    1 &  8\end{array} \right)\qquad
B = \left( \begin{array}{ccc}
1 & 3\\
0 & 2\\
1 & -2\\
0 & 1\end{array} \right)\qquad
C = \left( \begin{array}{ccc}
2 & -1\\
4 & -3\end{array} \right)
\end{equation}
>
\begin{equation}
x= \left( \begin{array}{ccc}
    3\\
    -1\\
    1\end{array} \right)\qquad
y = \left( \begin{array}{ccc}
2\\
2\end{array} \right)\qquad
z = \left( \begin{array}{ccc}
-4\\
1\\
0\\
8\end{array} \right)
\end{equation}
>
#### Questions:

**A:** Compute the all possible matrix products: 
$MN$, with $M,N \in \{A,B,C\} $

**B:** Compute the all possible matrix products: 
$Mv$, with $M \in \{A,B,C\}$ $ v \in \{x,y,z\} $

**C:** Compute the all possible matrix products: 
$MNP$, with $M,N,P \in \{A,B,C\}$ 

**D:** Compute the all possible matrix products: 
$v^TM$, with $M \in \{A,B,C\}$ and $v \in \{x,y,z\} $

**E:** Compute the all possible matrix products: 
$v^TMw$, with $M \in \{A,B,C\}$ and $v,w \in \{x,y,z\} $

**F:** Compute the all possible matrix products: 
$v^Tw$, with $v,w \in \{x,y,z\} $

**G:** Compute the all possible matrix products: 
$vw^T$, with $v,w \in \{x,y,z\} $


## Importing packages:


```python
!pip install jovian python-qt --upgrade --quiet
```


```python
pip install --user array_to_latex --upgrade --quiet
```

    Note: you may need to restart the kernel to use updated packages.



```python
import numpy as np
from numpy import linalg as LA
import jovian
```


```python
to_tex = lambda A : a2l.to_ltx(A, frmt = '{:6}', arraytype = 'bmatrix', mathform=True)
```

## A: Two matrices:
>
Compute the all possible matrix products: 
$MN$, with $M,N \in \{A,B,C\} $
>

Lets create the matrix A, B and C along with the vectors x, y and z using the `numpy.matrix` function


```python
A = np.matrix([[2,1,4],
              [3,1,8]])

B = np.matrix([[1,3],
              [0,2],
              [1,-2],
              [0,1]])

C = np.matrix([[2,-1],
              [4,-3]])
```


```python
x = np.array([[3],
             [-1],
             [1]])

y = np.array([[2],
             [2]])

z = np.array([[-4],
             [1],
             [0],
             [8]])             
```


```python
print('Matrix A shape:', A.shape)
print('Matrix B shape:', B.shape)
print('Matrix C shape:', C.shape)
```

    Matrix A shape: (2, 3)
    Matrix B shape: (4, 2)
    Matrix C shape: (2, 2)



```python
print('Vector x shape:', x.shape)
print('Matrix y shape:', y.shape)
print('Matrix z shape:', z.shape)
```

    Vector x shape: (3, 1)
    Matrix y shape: (2, 1)
    Matrix z shape: (4, 1)



```python
print('Vector x shape:', x.shape)
print('Matrix y shape:', y.shape)
print('Matrix z shape:', z.shape)
```

    Vector x shape: (3, 1)
    Matrix y shape: (2, 1)
    Matrix z shape: (4, 1)



```python
BC = B*C
#BC.shape
#to_tex(BC) ###remove the single hash to retrieve Latex
```

   $$ BC_{(4,2)}= \begin{bmatrix}
         14.00 & -10.00\\
          8.00 &  -6.00\\
        -6.00 &    5.00\\
          4.00 &  -3.00
      \end{bmatrix} $$


```python
BA = B*A
#BA.shape
#to_tex(BA)
```

$$ BA_{(4,3)} =\begin{bmatrix}
   11.00 &    4.00 &   28.00\\
    6.00 &    2.00 &   16.00\\
  -4.00 &  -1.00 & -12.00\\
    3.00 &    1.00 &    8.00
\end{bmatrix} $$


```python
CA = C*A
#CA.shape
#to_tex(CA)
```

$$ CA_{(2,3)}= \begin{bmatrix}
    1.00 &    1.00 &    0.00\\
  -1.00 &    1.00 &  -8.00
\end{bmatrix} $$

>The possible combinations are $BC$, $BA$ and $CA$

## B: Matrix and Vector:
>
Compute the all possible matrix products: 
$Mv$, with $M \in \{A,B,C\}$ $ v \in \{x,y,z\} $
>

Computing the possible combinations $ Ax,By $ & $Cy $:


```python
Ax= A*x
#Ax.shape
#to_tex(Ax)
```

$$ Ax_{(2,1)}= \begin{bmatrix}
    9\\
   16
\end{bmatrix} $$


```python
By= B*y
#to_tex(By)
```

$$ By_{(4,1)}= \begin{bmatrix}
    8\\
    4\\
  -2\\
    2
\end{bmatrix} $$


```python
Cy= C*y
#to_tex(Cy)
```

$$ Cy_{(2,1)}= \begin{bmatrix}
    2\\
    2
\end{bmatrix}$$

For the remaining combinations:

Ay = shapes (2,3) and (2,1) not aligned: 3 (dim 1) != 2 (dim 0)

Az = shapes (2,3) and (4,1) not aligned: 3 (dim 1) != 4 (dim 0)

Bx = shapes (4,2) and (3,1) not aligned: 2 (dim 1) != 3 (dim 0)

Bz = shapes (4,2) and (4,1) not aligned: 2 (dim 1) != 4 (dim 0)

Cx = shapes (2,2) and (3,1) not aligned: 2 (dim 1) != 3 (dim 0)

Cz = shapes (2,2) and (4,1) not aligned: 2 (dim 1) != 4 (dim 0)


## C: Three matrices:
>
Compute the all possible matrix products: 
$MNP$, with $M,N,P \in \{A,B,C\}$ 
>

According to the associative rule, we can verify the above combinations using: $(AB)C=A(BC)$

The possible combinations are: 

1. $(BC)A = B(CA):$


```python
BC_A =BC * A
#BC_A.shape
#to_tex(BC_A)
```

$$ (BC)A_{(4,3)}= \begin{bmatrix}
     -2  &       4  &    -24 \\
     -2  &       2  &    -16 \\
       3  &     -1  &      16 \\
     -1  &       1  &     -8 
\end{bmatrix} $$


```python
B_CA =B * CA
#B_CA.shape
#to_tex(B_CA)
```

$$ B(CA)_{(4,3)}= \begin{bmatrix}
     -2  &       4  &    -24 \\
     -2  &       2  &    -16 \\
       3  &     -1  &      16 \\
     -1  &       1  &     -8 
\end{bmatrix} $$

2. $(BC)C = B(CC)$


```python
BC_C =BC * C
#BC_C.shape
#to_tex(BC_C)
```

$$ (BC)C_{(4,2)}= \begin{bmatrix}
    -12  &      16 \\
     -8  &      10 \\
       8  &     -9 \\
     -4  &       5 
\end{bmatrix} $$


```python
B_CC =B * (C*C)
#BC_C.shape
#to_tex(B_CC)
```

$$ B(CC)_{(4,2)}= \begin{bmatrix}
    -12  &      16 \\
     -8  &      10 \\
       8  &     -9 \\
     -4  &       5 
\end{bmatrix} $$

## D: Vector and matrix:
>
Compute the all possible matrix products: 
$v^TM$, with $M \in \{A,B,C\}$ and $v \in \{x,y,z\} $
>

To compute this, we can create a new set of transpose matrices for $x^T$ , $y^T$, $z^T$ as follows:


```python
x_t = np.transpose(x)
y_t = np.transpose(y)
z_t = np.transpose(z)

#remove the hashes below to extract latex:
#to_tex(x_t)
#to_tex(y_t)
#to_tex(z_t)
```

\begin{equation}
x^T= \left( \begin{array}{ccc}
    3 &  -1 &    1\end{array} \right)\qquad
y^T = \left( \begin{array}{ccc}
2 &    2\end{array} \right)\qquad
z^T = \left( \begin{array}{ccc}
-4 &    1 &    0 &    8\end{array} \right)
\end{equation}


```python
print('x transpose shape:', x_t.shape)
print('y transpose shape:', y_t.shape)
print('z transpose shape:', z_t.shape)
```

    x transpose shape: (1, 3)
    y transpose shape: (1, 2)
    z transpose shape: (1, 4)


The possible combinations are: $(y^TA)x$ , $(z^TB)y$ and $(y^TC)y$


```python
y_tA = y_t * A 
#y_tA.shape
#to_tex(y_tA)
```

$$ y^TA_{(1,3)}= \begin{bmatrix}
      10  &       4  &      24 
\end{bmatrix} $$


```python
z_tB = z_t * B 
#z_tB.shape
#to_tex(z_tB)
```

$$ z^TB_{(1,2)}= \begin{bmatrix}
     -4  &     -2 
\end{bmatrix} $$


```python
y_tC = y_t * C 
#y_tC.shape
#to_tex(y_tC)
```

$$ y^TC_{(1,2)}= \begin{bmatrix}
      12  &     -8 
\end{bmatrix} $$

## E: Vector-matrix-vector:
>
Compute the all possible matrix products: 
$v^TMw$, with $M \in \{A,B,C\}$ and $v,w \in \{x,y,z\} $
>

To compute this, we can create a new set of transpose matrices for $x^T$ , $y^T$, $z^T$ as follows:

The possible combinations are: $(y^TA)x$ , $(z^TB)y$ and $(y^TC)y$


```python
y_tA
```




    matrix([[10,  4, 24]])




```python
y_tA_x = y_tA * x 
#y_tA_x.shape
#to_tex(y_tA_x)
```

$$ (y^TA)x= \begin{bmatrix}
      50 
\end{bmatrix} $$


```python
z_tB_y = z_tB * y 
#z_tB_y.shape
#to_tex(z_tB_y)
```

$$ (z^TB)y_{}= \begin{bmatrix}
    -12 
\end{bmatrix} $$


```python
y_tC = y_t * C 
y_tC_y = y_tC * y 
#y_tC.shape
#to_tex(y_tC_y)
```

$$ (y^TC)y_{}= \begin{bmatrix}
       8 
\end{bmatrix}$$

## F: Vector-vector
>
Compute the all possible matrix products: 
$v^Tw$, with $v,w \in \{x,y,z\} $
>

The possible combinations are: $(x^T)x$ , $(y^T)y$ and $(z^T)z$


```python
x_t_x = np.matmul(x_t,x)
#to_tex(x_t_x)
```

$$ x^T.x=\begin{bmatrix}
      11 
\end{bmatrix}$$


```python
y_t_x = np.matmul(y_t,y)
#to_tex(y_t_x)
```

$$ y^T.y=\begin{bmatrix}
       8 
\end{bmatrix}$$


```python
z_t_z = np.matmul(z_t,z)
#to_tex(z_t_z)
```

$$ z^T.z=\begin{bmatrix}
      81 
\end{bmatrix}$$

## G: vector-vector
>
Compute the all possible matrix products: 
$vw^T$, with $v,w \in \{x,y,z\} $
>


```python
x_xt = np.matmul(x,x_t)
#to_tex(x_xt)
```

$$ x.x^T= \begin{bmatrix}
    9.00 &  -3.00 &    3.00\\
  -3.00 &    1.00 &  -1.00\\
    3.00 &  -1.00 &    1.00
\end{bmatrix} $$


```python
y_xt = np.matmul(y,x_t)
#to_tex(y_xt)
```

$$ y.x^T= \begin{bmatrix}
       6  &     -2  &       2 \\
       6  &     -2  &       2 
\end{bmatrix} $$


```python
z_xt = np.matmul(z,x_t)
#to_tex(z_xt)
```

$$ x.x^T= \begin{bmatrix}
    -12  &       4  &     -4 \\
       3  &     -1  &       1 \\
       0  &       0  &       0 \\
      24  &     -8  &       8 
\end{bmatrix} $$


```python
x_yt= np.matmul(x,y_t)
#to_tex(x_yt)
```

$$ x.y^T= \begin{bmatrix}
       6  &       6 \\
     -2  &     -2 \\
       2  &       2 
\end{bmatrix}$$


```python
y_yt= np.matmul(y,y_t)
#to_tex(y_yt)
```

$$ y.y^T= \begin{bmatrix}
       4  &       4 \\
       4  &       4 
\end{bmatrix}$$


```python
z_yt= np.matmul(z,y_t)
#to_tex(z_yt)
```

$$ z.y^T= \begin{bmatrix}
     -8  &     -8 \\
       2  &       2 \\
       0  &       0 \\
      16  &      16 
\end{bmatrix}
$$

Computing the vectors $ x,y \& z $ multiplied with $z^T$


```python
x_zt= np.matmul(x,z_t)
#to_tex(x_zt)
```

$$ x.z^T= \begin{bmatrix}
    -12  &       3  &       0  &      24 \\
       4  &     -1  &       0  &     -8 \\
     -4  &       1  &       0  &       8 
\end{bmatrix} $$


```python
y_zt= np.matmul(y,z_t)
#to_tex(y_zt)
```

$$ y.z^T= \begin{bmatrix}
     -8  &       2  &       0  &      16 \\
     -8  &       2  &       0  &      16 
\end{bmatrix} $$


```python
z_zt= np.matmul(z,z_t)
#to_tex(z_zt)
```

$$ z.z^T= \begin{bmatrix}
     16  &     -4  &       0  &    -32 \\
     -4  &       1  &       0  &       8 \\
       0  &       0  &       0  &       0 \\
    -32  &       8  &       0  &      64 
\end{bmatrix} $$


```python
jovian.commit(project="matrices-determinants")
```


    <IPython.core.display.Javascript object>


    [jovian] Updating notebook "ranton95/matrices-determinants" on https://jovian.ai[0m
    [jovian] Committed successfully! https://jovian.ai/ranton95/matrices-determinants[0m





    'https://jovian.ai/ranton95/matrices-determinants'




```python

```
