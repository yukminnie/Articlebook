## **素数的和** {#素数的和}

所有小于10的素数的和是2 + 3 + 5 + 7 = 17。

求所有小于两百万的素数的和。



> ## **Summation of primes** {#Summation-of-primes}
>
> The sum of the primes below 10 is 2 + 3 + 5 + 7 = 17.
>
> Find the sum of all the primes below two million.



```
#/usr/bin/env python

from math import sqrt

def isPrime(n):
    for i in xrange(2,int(sqrt(n))+1):
        if n % i == 0:
            return False
    return True

summa = 0
for i in xrange(2,2000000):
    if isPrime(i):
        summa += i

print summa
```



