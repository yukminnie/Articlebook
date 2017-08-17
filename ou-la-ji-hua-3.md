## **最大质因数** {#最大质因数}

13195的所有质因数为5、7、13和29。

600851475143最大的质因数是多少？

> ## **Largest prime factor** {#Largest-prime-factor}
>
> The prime factors of 13195 are 5, 7, 13 and 29.
>
> What is the largest prime factor of the number 600851475143 ?

```py
def eula(s):
    i = 2
    while s != 1:
        if not s % i:
            s = s / i
            maxPrime = i
        else:
            i += 1
    return maxPrime

print eula(600851475143)
```



