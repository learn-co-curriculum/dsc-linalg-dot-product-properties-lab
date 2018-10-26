
# Properties of Dot Product - Lab

## Introduction

In this lab we shall look at some interesting properties of a Dot product type matrix multiplication. Understanding these properties will become useful as we move forward with machine learning advanced linear algebra. The lab will require you to calculate results to provide a proof for these properties.

## Objectives
You will be able to:
* Understand and analytically explain Distributive, Commutative and Associative properties of dot product

## Instructions

* For each property, create suitably sized matrices with random data and prove the equations 
* Ensure that size/dimension assumptions are met while performing calculations (you'll see errors otherwise)
* Calculate the LHS and RHS for all equations and show if they are equal or not

## Distributive Property - Matrices multiplication is distributive
### Prove that A.(B+C)=A.B+A.C


```python
import numpy as np
A = np.array([[2, 3], [1, 4], [7, 6]])
B = np.array([[5], [2]])
C = np.array([[4], [3]])

left = A.dot(B+C)
right = A.dot(B) + A.dot(C)

print (left == right)
```

    [[ True]
     [ True]
     [ True]]


## Associative Property - Matrices multiplication is associative
### Prove that A.(B.C)=(A.B).C


```python
A = np.array([[2, 3], [1, 4], [7, 6]])
B = B = np.array([[5, 3], [2, 2]])
C = np.array([[4], [3]])

left = A.dot(B.dot(C))
right = (A.dot(B)).dot(C)

left == right
```




    array([[ True],
           [ True],
           [ True]])



## Commutative Property - Matrix multiplication is NOT commutative
### Prove that for matrices, A.B ≠ B.A


```python
A = np.array([[2, 3], [6, 5]])
B = np.array([[5, 3], [2, 2]])

left = A.dot(B)
right = B.dot(A)

print (left)
print(right)

left == right
```

    [[16 12]
     [40 28]]
    [[28 30]
     [16 16]]





    array([[False, False],
           [False, False]])



## Commutative Property -  vector multiplication IS commutative
### Prove that for vectors, x<sup>T</sup> . y = y<sup>T</sup> . x
Note: superscipt<sup>T</sup> denotes the transpose we saw earlier


```python
x = np.array([[2], [6], [7]])
y = np.array([[3], [5], [9]])

left = np.transpose(x).dot(y)
right = np.transpose(y).dot(x)
left == right
```




    array([[ True]])



#### and finally 
## Simplification of the matrix product
### Prove that  (A.B)<sup>T</sup> = B<sup>T</sup> . A<sup>T</sup>


```python
A = np.array([[2, 3], [1, 4], [7, 6]])
B = np.array([[5, 3], [2, 2]])

left = np.transpose(A.dot(B))
right = np.transpose(B).dot(np.transpose(A))
left == right
```




    array([[ True,  True,  True],
           [ True,  True,  True]])



## Summary 

So now we have seen enough matrix algebra to help us solve a problem of linear equations as we saw earlier in this section. We shall see how to do this next. 
