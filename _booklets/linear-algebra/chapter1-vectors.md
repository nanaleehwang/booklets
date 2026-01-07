---
layout: chapter
booklet: "linear-algebra"
booklet_title: "Introduction to Linear Algebra"
booklet_subtitle: "A Comprehensive Guide for Students"
booklet_author: "Dr. Jane Smith"
chapter_number: 1
title: "Vectors and Vector Spaces"
subtitle: "Foundation of Linear Algebra"
author: "Dr. Jane Smith"
---

# Introduction to Vectors

A vector is a mathematical object that has both magnitude and direction. In this chapter, we will explore the fundamental properties of vectors and vector spaces.

## Definition of a Vector

A vector can be represented in multiple ways:
- Geometrically as an arrow in space
- Algebraically as an ordered list of numbers
- Abstractly as an element of a vector space

## Vector Operations

The two fundamental operations on vectors are:
1. **Vector Addition**: $(a_1, a_2, ..., a_n) + (b_1, b_2, ..., b_n) = (a_1 + b_1, a_2 + b_2, ..., a_n + b_n)$
2. **Scalar Multiplication**: $c(a_1, a_2, ..., a_n) = (ca_1, ca_2, ..., ca_n)$

These operations satisfy several important properties:
- Commutativity: $\mathbf{u} + \mathbf{v} = \mathbf{v} + \mathbf{u}$
- Associativity: $(\mathbf{u} + \mathbf{v}) + \mathbf{w} = \mathbf{u} + (\mathbf{v} + \mathbf{w})$
- Distributivity: $c(\mathbf{u} + \mathbf{v}) = c\mathbf{u} + c\mathbf{v}$

## Vector Spaces

A **vector space** is a set $V$ along with operations of vector addition and scalar multiplication that satisfy eight axioms:

### Closure Properties
1. If $\mathbf{u}, \mathbf{v} \in V$, then $\mathbf{u} + \mathbf{v} \in V$
2. If $\mathbf{v} \in V$ and $c$ is a scalar, then $c\mathbf{v} \in V$

### Additive Properties
3. Commutativity: $\mathbf{u} + \mathbf{v} = \mathbf{v} + \mathbf{u}$
4. Associativity: $(\mathbf{u} + \mathbf{v}) + \mathbf{w} = \mathbf{u} + (\mathbf{v} + \mathbf{w})$
5. Zero vector: There exists $\mathbf{0} \in V$ such that $\mathbf{v} + \mathbf{0} = \mathbf{v}$
6. Additive inverse: For each $\mathbf{v} \in V$, there exists $-\mathbf{v} \in V$ such that $\mathbf{v} + (-\mathbf{v}) = \mathbf{0}$

### Scalar Multiplication Properties
7. Scalar associativity: $(cd)\mathbf{v} = c(d\mathbf{v})$
8. Multiplicative identity: $1\mathbf{v} = \mathbf{v}$

## Examples of Vector Spaces

- $\mathbb{R}^n$: The set of all $n$-tuples of real numbers
- $\mathbb{C}^n$: The set of all $n$-tuples of complex numbers
- $P_n$: The set of all polynomials of degree at most $n$
- $M_{m \times n}$: The set of all $m \times n$ matrices

## Linear Independence and Span

### Linear Combination
A **linear combination** of vectors $\mathbf{v_1}, \mathbf{v_2}, ..., \mathbf{v_k}$ is an expression of the form:
$$c_1\mathbf{v_1} + c_2\mathbf{v_2} + ... + c_k\mathbf{v_k}$$

### Span
The **span** of a set of vectors is the set of all possible linear combinations of those vectors.

### Linear Independence
Vectors $\mathbf{v_1}, \mathbf{v_2}, ..., \mathbf{v_k}$ are **linearly independent** if the only solution to:
$$c_1\mathbf{v_1} + c_2\mathbf{v_2} + ... + c_k\mathbf{v_k} = \mathbf{0}$$
is $c_1 = c_2 = ... = c_k = 0$.