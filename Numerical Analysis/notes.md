# Numerical Analysis:

## Contents:
+ [Introduction](#introduction)
+ [Bisection Method](#bisection-method)
+ [Secant Method](#secant-method)

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
### Code:
```python
import math
import matplotlib.pyplot as plt
def fx(x):
    return ((x*x*x) - x - 3)
a = 1
b = 2
i = 0
c = []
fc = []
ax = plt.axes()
while(i != 100 ):
    c.append((a+b)/2)
    fa = fx(a)
    fb = fx(b)
    fc.append(fx(c[i]))
    if fc[i]*fa < 0:
        b = c[i]
    if fc[i]*fb < 0:
        a = c[i]
    i = i+1
plt.plot(c, fc,'r.')
plt.show()
```

### Example:


Given f(x) = $x^3 + 3x - 2 = 0$
Now, if we take a = -1 and b = 1 we get f(a) = -2 and f(b) = 2
Then we compute $c = (-1 + 1) / 2 = 0$
Similarily f(c) = -2. Since it is lesser than 0, we replace b as c. Therefore the roots now become -1 and 0. This process is continued till we reach close to the root, which in this case is approximately $0.596$.



## Secant Method:

This is another root finding procedure used in numerical analysis. It has the following formula:

$c = b - ((f(b)*(b - a))/(f(b)-f(a))$
