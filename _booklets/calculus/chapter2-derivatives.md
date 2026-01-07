---
layout: chapter
booklet: "calculus"
booklet_title: "Calculus Fundamentals"
booklet_subtitle: "Limits, Derivatives, and Integrals"
booklet_author: "Prof. Michael Johnson"
chapter_number: 2
title: "Derivatives and Differentiation"
subtitle: "Rates of Change"
author: "Prof. Michael Johnson"
---

# The Derivative

The derivative measures the instantaneous rate of change of a function. It's one of the most important concepts in calculus with applications across science and engineering.

## Definition of the Derivative

The derivative of $f(x)$ at $x = a$ is:
$$f'(a) = \lim_{h \to 0} \frac{f(a+h) - f(a)}{h}$$

Alternatively, using the limit definition:
$$f'(x) = \lim_{h \to 0} \frac{f(x+h) - f(x)}{h}$$

## Geometric Interpretation

The derivative $f'(a)$ represents:
- The slope of the tangent line to $y = f(x)$ at the point $(a, f(a))$
- The instantaneous rate of change of $f$ at $x = a$

### Equation of the Tangent Line
The tangent line to $y = f(x)$ at $(a, f(a))$ is:
$$y - f(a) = f'(a)(x - a)$$

## Differentiation Rules

### Basic Rules
1. **Constant Rule**: $\frac{d}{dx}[c] = 0$
2. **Power Rule**: $\frac{d}{dx}[x^n] = nx^{n-1}$
3. **Constant Multiple**: $\frac{d}{dx}[cf(x)] = cf'(x)$
4. **Sum Rule**: $\frac{d}{dx}[f(x) + g(x)] = f'(x) + g'(x)$

### Product Rule
$$\frac{d}{dx}[f(x)g(x)] = f'(x)g(x) + f(x)g'(x)$$

**Example**: $\frac{d}{dx}[x^2 \sin x] = 2x \sin x + x^2 \cos x$

### Quotient Rule
$$\frac{d}{dx}\left[\frac{f(x)}{g(x)}\right] = \frac{f'(x)g(x) - f(x)g'(x)}{[g(x)]^2}$$

**Example**: $\frac{d}{dx}\left[\frac{x^2}{x+1}\right] = \frac{2x(x+1) - x^2 \cdot 1}{(x+1)^2} = \frac{x^2 + 2x}{(x+1)^2}$

### Chain Rule
For composite functions:
$$\frac{d}{dx}[f(g(x))] = f'(g(x)) \cdot g'(x)$$

**Example**: $\frac{d}{dx}[\sin(x^2)] = \cos(x^2) \cdot 2x = 2x\cos(x^2)$

## Derivatives of Common Functions

### Trigonometric Functions
- $\frac{d}{dx}[\sin x] = \cos x$
- $\frac{d}{dx}[\cos x] = -\sin x$
- $\frac{d}{dx}[\tan x] = \sec^2 x$
- $\frac{d}{dx}[\sec x] = \sec x \tan x$
- $\frac{d}{dx}[\csc x] = -\csc x \cot x$
- $\frac{d}{dx}[\cot x] = -\csc^2 x$

### Inverse Trigonometric Functions
- $\frac{d}{dx}[\arcsin x] = \frac{1}{\sqrt{1-x^2}}$
- $\frac{d}{dx}[\arccos x] = -\frac{1}{\sqrt{1-x^2}}$
- $\frac{d}{dx}[\arctan x] = \frac{1}{1+x^2}$

### Exponential and Logarithmic Functions
- $\frac{d}{dx}[e^x] = e^x$
- $\frac{d}{dx}[a^x] = a^x \ln a$
- $\frac{d}{dx}[\ln x] = \frac{1}{x}$
- $\frac{d}{dx}[\log_a x] = \frac{1}{x \ln a}$

## Implicit Differentiation

When $y$ is defined implicitly by an equation $F(x,y) = 0$, we differentiate both sides with respect to $x$:

**Example**: For $x^2 + y^2 = 25$
$$2x + 2y\frac{dy}{dx} = 0$$
$$\frac{dy}{dx} = -\frac{x}{y}$$

## Logarithmic Differentiation

For functions of the form $y = [f(x)]^{g(x)}$:
1. Take the natural logarithm: $\ln y = g(x) \ln[f(x)]$
2. Differentiate implicitly
3. Solve for $\frac{dy}{dx}$

**Example**: $y = x^x$
$$\ln y = x \ln x$$
$$\frac{1}{y}\frac{dy}{dx} = \ln x + 1$$
$$\frac{dy}{dx} = x^x(\ln x + 1)$$

## Higher-Order Derivatives

- **Second derivative**: $f''(x) = \frac{d^2f}{dx^2}$
- **Third derivative**: $f'''(x) = \frac{d^3f}{dx^3}$
- **nth derivative**: $f^{(n)}(x) = \frac{d^nf}{dx^n}$

### Physical Interpretations
If $s(t)$ represents position:
- $s'(t) = v(t)$ is velocity
- $s''(t) = a(t)$ is acceleration

## Applications of Derivatives

### Critical Points
Points where $f'(x) = 0$ or $f'(x)$ is undefined.

### Optimization
- **Local maximum**: $f'(a) = 0$ and $f''(a) < 0$
- **Local minimum**: $f'(a) = 0$ and $f''(a) > 0$
- **Inflection point**: $f''(a) = 0$ and $f''(x)$ changes sign

### Related Rates
When two or more related quantities change with time, we can find relationships between their rates of change.

**Example**: A balloon is inflated. If radius increases at 2 cm/s, how fast is volume increasing when $r = 10$ cm?

Given: $\frac{dr}{dt} = 2$ cm/s
Find: $\frac{dV}{dt}$ when $r = 10$ cm

Since $V = \frac{4}{3}\pi r^3$:
$$\frac{dV}{dt} = 4\pi r^2 \frac{dr}{dt} = 4\pi(10)^2(2) = 800\pi \text{ cm}^3/\text{s}$$

### Linear Approximation
Near $x = a$:
$$f(x) \approx f(a) + f'(a)(x-a)$$

This gives the best linear approximation to $f(x)$ near $x = a$.