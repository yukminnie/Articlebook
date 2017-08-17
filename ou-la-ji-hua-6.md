## **平方的和与和的平方之差** {#平方的和与和的平方之差}

前十个自然数的平方的和是

1

2

+ 2

2

+ … + 10

2

= 385

前十个自然数的和的平方是

\(1 + 2 + … + 10\)

2

= 55

2

= 3025

因此前十个自然数的平方的和与和的平方之差是 3025 − 385 = 2640。

求前一百个自然数的平方的和与和的平方之差。

> ## **Sum square difference** {#Sum-square-difference}
>
> The sum of the squares of the first ten natural numbers is,
>
> 1
>
> 2
>
> + 2
>
> 2
>
> + … + 10
>
> 2
>
> = 385
>
> The square of the sum of the first ten natural numbers is,
>
> \(1 + 2 + … + 10\)
>
> 2
>
> = 55
>
> 2
>
> = 3025
>
> Hence the difference between the sum of the squares of the first ten natural numbers and the square of the sum is 3025 − 385 = 2640.
>
> Find the difference between the sum of the squares of the first one hundred natural numbers and the square of the sum.

递归

```py
#!/usr/bin/env python

def sum(n):
    if n == 0:
        sumN = 0
    else:
        sumN = sum(n-1) + n
    return sumN

def square(n):
    if n == 0:
        squareN = 0
    else:
        squareN = square(n-1) + n ** 2
    return squareN

print sum(100) ** 2 - square(100)
```







