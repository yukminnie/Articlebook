## **第10001个素数** {#第10001个素数}

列出前6个素数，它们分别是2、3、5、7、11和13。我们可以看出，第6个素数是13。

第10,001个素数是多少？

> ## **10001st prime** {#10001st-prime}
>
> By listing the first six prime numbers: 2, 3, 5, 7, 11, and 13, we can see that the 6th prime is 13.
>
> What is the 10 001st prime number?

使用while循环，验证从2开始的每一个正整数是否为质数，若是，则给计数器+1，直到计数器值为10001。

```py
#/usr/bin/env python

from math import sqrt

#质数验证函数
def isPrime(n):
    for i in xrange(2,int(sqrt(n))+1):
        if n % i == 0:
            return False
    return True

i = 1
counter = 0    #计数器初始值为0
while counter < 10001:    #计数器到10001时跳出循环
    i += 1
    if isPrime(i):
        counter += 1
print i
```



