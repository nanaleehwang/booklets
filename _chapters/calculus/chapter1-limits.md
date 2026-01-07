---
booklet: "calculus"
booklet_title: "Calculus Fundamentals"
booklet_subtitle: "Limits, Derivatives, and Integrals"
booklet_author: "Prof. Michael Johnson"
chapter_number: 1
title: "Limits and Continuity"
subtitle: "The Foundation of Calculus"
author: "Prof. Michael Johnson"
tex_source: "tex-sources/calculus/chapter1-limits.tex"
---

# Understanding Limits

The concept of a limit is fundamental to calculus and mathematical analysis. It allows us to analyze the behavior of functions as they approach specific values.

## Informal Definition
We say that $\lim_{x \to a} f(x) = L$ if $f(x)$ gets arbitrarily close to $L$ as $x$ approaches $a$.

## Formal Definition (Epsilon-Delta)
For every $\varepsilon > 0$, there exists a $\delta > 0$ such that:
$$0 < |x - a| < \delta \implies |f(x) - L| < \varepsilon$$

This definition captures the precise meaning of "arbitrarily close" in mathematical terms.

## Types of Limits

### One-Sided Limits
- **Right-hand limit**: $\lim_{x \to a^+} f(x) = L$ (approaching from the right)
- **Left-hand limit**: $\lim_{x \to a^-} f(x) = L$ (approaching from the left)

The two-sided limit exists if and only if both one-sided limits exist and are equal.

### Infinite Limits
When a function grows without bound:
- $\lim_{x \to a} f(x) = +\infty$
- $\lim_{x \to a} f(x) = -\infty$

### Limits at Infinity
Behavior as $x$ approaches infinity:
- $\lim_{x \to \infty} f(x) = L$
- $\lim_{x \to -\infty} f(x) = L$

## Limit Laws

If $\lim_{x \to a} f(x) = L$ and $\lim_{x \to a} g(x) = M$, then:

1. **Sum Rule**: $\lim_{x \to a} [f(x) + g(x)] = L + M$
2. **Product Rule**: $\lim_{x \to a} [f(x) \cdot g(x)] = L \cdot M$
3. **Quotient Rule**: $\lim_{x \to a} \frac{f(x)}{g(x)} = \frac{L}{M}$ (if $M \neq 0$)
4. **Power Rule**: $\lim_{x \to a} [f(x)]^n = L^n$
5. **Constant Multiple**: $\lim_{x \to a} [c \cdot f(x)] = c \cdot L$

## Important Limits

### Standard Limits
- $\lim_{x \to 0} \frac{\sin x}{x} = 1$
- $\lim_{x \to 0} \frac{1 - \cos x}{x} = 0$
- $\lim_{x \to \infty} \left(1 + \frac{1}{x}\right)^x = e$

### Exponential and Logarithmic Limits
- $\lim_{x \to 0} \frac{e^x - 1}{x} = 1$
- $\lim_{x \to 0} \frac{\ln(1 + x)}{x} = 1$

## Squeeze Theorem

If $g(x) \leq f(x) \leq h(x)$ for all $x$ near $a$, and $\lim_{x \to a} g(x) = \lim_{x \to a} h(x) = L$, then:
$$\lim_{x \to a} f(x) = L$$

**Example**: Proving $\lim_{x \to 0} x^2 \sin\left(\frac{1}{x}\right) = 0$

Since $-1 \leq \sin\left(\frac{1}{x}\right) \leq 1$, we have:
$$-x^2 \leq x^2 \sin\left(\frac{1}{x}\right) \leq x^2$$

As $x \to 0$, both $-x^2 \to 0$ and $x^2 \to 0$, so by the Squeeze Theorem, the limit is 0.

## Continuity

A function $f$ is **continuous** at $x = a$ if:
1. $f(a)$ is defined
2. $\lim_{x \to a} f(x)$ exists
3. $\lim_{x \to a} f(x) = f(a)$

### Types of Discontinuity
1. **Removable discontinuity**: The limit exists but doesn't equal the function value
2. **Jump discontinuity**: Left and right limits exist but are different
3. **Infinite discontinuity**: The function approaches infinity

### Properties of Continuous Functions
- Sums, products, and compositions of continuous functions are continuous
- Polynomials are continuous everywhere
- Rational functions are continuous except at zeros of the denominator

## Intermediate Value Theorem

If $f$ is continuous on $[a, b]$ and $k$ is any value between $f(a)$ and $f(b)$, then there exists $c \in (a, b)$ such that $f(c) = k$.

**Applications**: 
- Proving existence of roots
- Bisection method for numerical approximation

## L'Hôpital's Rule

For indeterminate forms $\frac{0}{0}$ or $\frac{\infty}{\infty}$:
$$\lim_{x \to a} \frac{f(x)}{g(x)} = \lim_{x \to a} \frac{f'(x)}{g'(x)}$$

provided the limit on the right exists.

**Example**: $\lim_{x \to 0} \frac{\sin x}{x} = \lim_{x \to 0} \frac{\cos x}{1} = 1$