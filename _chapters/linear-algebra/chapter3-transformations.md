---
booklet: "linear-algebra"
booklet_title: "Introduction to Linear Algebra"
booklet_subtitle: "A Comprehensive Guide for Students"
booklet_author: "Dr. Jane Smith"
chapter_number: 3
title: "Linear Transformations"
subtitle: "Functions Between Vector Spaces"
author: "Dr. Jane Smith"
tex_source: "tex-sources/linear-algebra/chapter3-transformations.tex"
---

# Linear Transformations

A linear transformation is a function between vector spaces that preserves the vector space operations of addition and scalar multiplication.

## Definition

A function $T: V \to W$ between vector spaces $V$ and $W$ is called **linear** if:
1. $T(\mathbf{u} + \mathbf{v}) = T(\mathbf{u}) + T(\mathbf{v})$ for all $\mathbf{u}, \mathbf{v} \in V$
2. $T(c\mathbf{v}) = cT(\mathbf{v})$ for all $\mathbf{v} \in V$ and scalars $c$

These two properties can be combined into a single condition:
$$T(c_1\mathbf{v_1} + c_2\mathbf{v_2}) = c_1T(\mathbf{v_1}) + c_2T(\mathbf{v_2})$$

## Matrix Representation

Every linear transformation from $\mathbb{R}^n$ to $\mathbb{R}^m$ can be represented by an $m \times n$ matrix $A$ such that:
$$T(\mathbf{x}) = A\mathbf{x}$$

### Finding the Matrix Representation
If $T: \mathbb{R}^n \to \mathbb{R}^m$, then the matrix $A$ has columns that are the images of the standard basis vectors:
$$A = [T(\mathbf{e_1}) \quad T(\mathbf{e_2}) \quad \cdots \quad T(\mathbf{e_n})]$$

where $\mathbf{e_i}$ are the standard basis vectors of $\mathbb{R}^n$.

## Examples of Linear Transformations

### 1. Rotation in the Plane
Rotating vectors in $\mathbb{R}^2$ by angle $\theta$ counterclockwise:
$$R_\theta = \begin{pmatrix} \cos\theta & -\sin\theta \\ \sin\theta & \cos\theta \end{pmatrix}$$

### 2. Scaling
Scaling vectors by factors $s_x$ and $s_y$:
$$S = \begin{pmatrix} s_x & 0 \\ 0 & s_y \end{pmatrix}$$

### 3. Reflection
Reflecting across the $x$-axis:
$$R_x = \begin{pmatrix} 1 & 0 \\ 0 & -1 \end{pmatrix}$$

### 4. Projection
Orthogonal projection onto the $x$-axis:
$$P_x = \begin{pmatrix} 1 & 0 \\ 0 & 0 \end{pmatrix}$$

### 5. Shearing
Horizontal shear:
$$H = \begin{pmatrix} 1 & k \\ 0 & 1 \end{pmatrix}$$

## Properties of Linear Transformations

1. **Zero Vector**: $T(\mathbf{0}) = \mathbf{0}$
2. **Linear Combinations**: $T$ preserves linear combinations
3. **Composition**: The composition of linear transformations is linear
4. **Inverse**: If $T$ is invertible, then $T^{-1}$ is also linear

## Kernel and Image

### Kernel (Null Space)
The **kernel** of $T$ is the set of all vectors that map to the zero vector:
$$\ker(T) = \{\mathbf{v} \in V : T(\mathbf{v}) = \mathbf{0}\}$$

### Image (Range)
The **image** of $T$ is the set of all possible output vectors:
$$\text{Im}(T) = \{T(\mathbf{v}) : \mathbf{v} \in V\}$$

### Rank-Nullity Theorem
For a linear transformation $T: V \to W$ where $V$ is finite-dimensional:
$$\dim(V) = \dim(\ker(T)) + \dim(\text{Im}(T))$$

## Injective and Surjective Transformations

### Injective (One-to-One)
$T$ is injective if $T(\mathbf{u}) = T(\mathbf{v})$ implies $\mathbf{u} = \mathbf{v}$.
Equivalently: $T$ is injective iff $\ker(T) = \{\mathbf{0}\}$.

### Surjective (Onto)
$T$ is surjective if for every $\mathbf{w} \in W$, there exists $\mathbf{v} \in V$ such that $T(\mathbf{v}) = \mathbf{w}$.
Equivalently: $\text{Im}(T) = W$.

### Bijective (Isomorphism)
$T$ is bijective if it is both injective and surjective. Bijective linear transformations are called **isomorphisms**.

## Change of Basis

When working with different bases, we need to understand how linear transformations change their matrix representations.

If $B$ and $C$ are bases for vector spaces $V$ and $W$ respectively, and $T: V \to W$ is linear, then:
$$[T]_C^B$$
represents the matrix of $T$ with respect to bases $B$ and $C$.

## Applications

Linear transformations are fundamental in:
- Computer graphics (rotations, scaling, translations)
- Signal processing
- Data compression (PCA)
- Differential equations
- Quantum mechanics