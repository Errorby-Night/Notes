# Numerical Analysis:

## Contents:
+ Introduction
+ Bisection Method

## Introduction:
It is the branch of mathematics that provides tools and methods for solving mathematical problems in numerical form. The objective is to develop detailed computational procedures, that can be implemented on electronic computers.

## Bisection Method:

This method is used to find the roots of the polynomial equation. It separates the interval and subdivides the interval in which the roots of the equation lies. The principle behind it is simple, it closes the gap between the positive and negative intervals until it reaches closer to the correct answer. So a better understanding would be through the algorithm and an example:
### Algorithm:
For any continuous function f(x):
```
Step 1: Choose two intervals a and b where f(a) < 0 and f(b) > 0
Step 2: Compute c = (a+b) / 2
Step 3: If f(c) < 0 replace a with c else f(c) > 0 replace b with c
Step 4: Repeat from Step 2 until f(c) reaches near zero.
```

### Example:
```
Given f(x) = x<sup>3</sup> + 3x + 2 = 0
Now, if we take a = -2 and b = 2 we get f(a) = 2 and f(b) = 
