---
layout: chapter
booklet: "linear-algebra"
booklet_title: "Introduction to Linear Algebra"
booklet_subtitle: "A Comprehensive Guide for Students"
booklet_author: "Dr. Jane Smith"
chapter_number: 2
title: "Matrices and Matrix Operations"
subtitle: "Linear Transformations in Action"
author: "Dr. Jane Smith"
---

# Introduction to Matrices

A matrix is a rectangular array of numbers arranged in rows and columns. Matrices are fundamental tools in linear algebra for representing and manipulating linear transformations.

## Matrix Notation

An $m \times n$ matrix $A$ has $m$ rows and $n$ columns:

$$A = \begin{pmatrix}
a_{11} & a_{12} & \cdots & a_{1n} \\
a_{21} & a_{22} & \cdots & a_{2n} \\
\vdots & \vdots & \ddots & \vdots \\
a_{m1} & a_{m2} & \cdots & a_{mn}
\end{pmatrix}$$

We denote the entry in the $i$-th row and $j$-th column as $a_{ij}$.

## Matrix Operations

### Addition
Two matrices of the same size can be added element-wise:
$$(A + B)_{ij} = a_{ij} + b_{ij}$$

**Example:**
$$\begin{pmatrix} 1 & 2 \\ 3 & 4 \end{pmatrix} + \begin{pmatrix} 5 & 6 \\ 7 & 8 \end{pmatrix} = \begin{pmatrix} 6 & 8 \\ 10 & 12 \end{pmatrix}$$

### Scalar Multiplication
Each entry of the matrix is multiplied by the scalar:
$$(cA)_{ij} = c \cdot a_{ij}$$

### Matrix Multiplication
Matrix multiplication is defined when the number of columns in the first matrix equals the number of rows in the second matrix:
$$(AB)_{ij} = \sum_{k=1}^{p} a_{ik}b_{kj}$$

For an $m \times p$ matrix $A$ and a $p \times n$ matrix $B$, the result is an $m \times n$ matrix.

**Example:**
$$\begin{pmatrix} 1 & 2 \\ 3 & 4 \end{pmatrix} \begin{pmatrix} 5 & 6 \\ 7 & 8 \end{pmatrix} = \begin{pmatrix} 19 & 22 \\ 43 & 50 \end{pmatrix}$$

## Special Matrices

### Identity Matrix
The **identity matrix** $I_n$ is an $n \times n$ matrix with 1's on the diagonal and 0's elsewhere:
$$I_3 = \begin{pmatrix} 1 & 0 & 0 \\ 0 & 1 & 0 \\ 0 & 0 & 1 \end{pmatrix}$$

Properties: $AI = IA = A$ for any compatible matrix $A$.

### Zero Matrix
The **zero matrix** has all entries equal to zero.

### Transpose
The **transpose** of matrix $A$, denoted $A^T$, is obtained by interchanging rows and columns:
$$(A^T)_{ij} = a_{ji}$$

### Symmetric Matrix
A matrix $A$ is **symmetric** if $A = A^T$.

### Diagonal Matrix
A **diagonal matrix** has non-zero entries only on the main diagonal.

## Matrix Properties

### Associative Property
$(AB)C = A(BC)$ when the products are defined.

### Distributive Properties
- $A(B + C) = AB + AC$
- $(A + B)C = AC + BC$

### Transpose Properties
- $(A^T)^T = A$
- $(A + B)^T = A^T + B^T$
- $(AB)^T = B^T A^T$

## Inverse Matrix

A square matrix $A$ is **invertible** (or non-singular) if there exists a matrix $A^{-1}$ such that:
$$AA^{-1} = A^{-1}A = I$$

### Properties of Inverse
- $(A^{-1})^{-1} = A$
- $(AB)^{-1} = B^{-1}A^{-1}$
- $(A^T)^{-1} = (A^{-1})^T$

A matrix is invertible if and only if its determinant is non-zero.

## Determinants

For a $2 \times 2$ matrix:
$$\det\begin{pmatrix} a & b \\ c & d \end{pmatrix} = ad - bc$$

For larger matrices, determinants are calculated using cofactor expansion or other methods.

## Applications

Matrices are used in:
- Solving systems of linear equations
- Computer graphics transformations
- Data analysis and statistics
- Network theory
- Quantum mechanics