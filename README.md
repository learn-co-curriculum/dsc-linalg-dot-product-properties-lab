
# Properties of Dot Product - Lab

## Introduction

In this lab, you'll be practicing some interesting properties of a dot product-type matrix multiplication. Understanding these properties will become useful as you study machine learning. The lab will require you to calculate results to provide a proof for these properties.

## Objectives

In this lab you will: 

- Demonstrate the distributive, commutative, and associative property of dot products 
- Use the transpose method to transpose Numpy matrices 
- Compute the dot product for matrices and vectors 


## Instructions

* For each property, create suitably sized matrices with random data to prove the equations 
* Ensure that size/dimension assumptions are met while performing calculations (you'll see errors otherwise)
* Calculate the LHS and RHS for all equations and show if they are equal or not

## Distributive Property - matrix multiplication IS distributive

### Prove that $A \cdot (B+C) = (A \cdot B + A \cdot C) $


```python
# Your code here
```


```python
# __SOLUTION__ 
import numpy as np
A = np.array([[2, 3], [1, 4], [7, 6]])
B = np.array([[5], [2]])
C = np.array([[4], [3]])

left = A.dot(B + C)
right = A.dot(B) + A.dot(C)

print (left == right)
```

## Associative Property - matrix multiplication IS associative
### Prove that $A \cdot (B \cdot C) = (A \cdot B) \cdot C $


```python
# Your code here 
```


```python
# __SOLUTION__ 
A = np.array([[2, 3], [1, 4], [7, 6]])
B = B = np.array([[5, 3], [2, 2]])
C = np.array([[4], [3]])

left = A.dot(B.dot(C))
right = (A.dot(B)).dot(C)

left == right
```

## Commutative Property - matrix multiplication is NOT commutative
### Prove that for matrices, $A \cdot B \neq B \cdot A $


```python
# Your code here 
```


```python
# __SOLUTION__ 
A = np.array([[2, 3], [6, 5]])
B = np.array([[5, 3], [2, 2]])

left = A.dot(B)
right = B.dot(A)

print(left)
print(right)

left == right
```

## Commutative Property -  vector multiplication IS commutative
### Prove that for vectors,  $x^T \cdot y = y^T \cdot x$
Note: superscipt<sup>T</sup> denotes the transpose we saw earlier


```python
# Your code here 
```


```python
# __SOLUTION__ 
x = np.array([[2], [6], [7]])
y = np.array([[3], [5], [9]])

left = np.transpose(x).dot(y)
right = np.transpose(y).dot(x)
left == right
```

## Simplification of the matrix product
### Prove that $ (A \cdot B)^T = B^T \cdot A^T $


```python
# Your code here 
```


```python
# __SOLUTION__ 
A = np.array([[2, 13], [1, 4], [72, 6], [18, 12], [27,5]])
B = np.array([[5, 30], [22, 2]])

left = np.transpose(A.dot(B))
right = np.transpose(B).dot(np.transpose(A))
left == right
```

## Summary 

You've seen enough matrix algebra by now to solve a problem of linear equations as you saw earlier. You'll now see how to do this next. 
