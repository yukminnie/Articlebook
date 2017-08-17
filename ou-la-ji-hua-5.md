## **最小倍数** {#最小倍数}

2520是最小的能够被1到10整除的数。

最小的能够被1到20整除的正数是多少？

> ## **Smallest multiple** {#Smallest-multiple}
>
> 2520 is the smallest number that can be divided by each of the numbers from 1 to 10 without any remainder.
>
> What is the smallest positive number that isevenly divisibleby all of the numbers from 1 to 20?

用循环做，由于答案太大（9位数），等解释器转了半天都没结果.

如果一个数n能被20以内的整数整除，应当满足以下条件：

假设一个质数i，并且i的j次方不大于20，则这个数应当能被i的j次方整除，即：n % \(i \*\* j\) == 0

这样，不用编程的方法可以求得：n = \(2 \*\* 4\) \* \(3 \*\* 2\) \* 5 \* 7 \* 11 \* 13 \* 17 \* 19

```py
#!/usr/bin/env python

from math import sqrt

#将不大于20的所有质数放入列表myPrime中
myPrime = [n for n in xrange(2,21) if 0 not in [n % i for i in xrange(2,int(sqrt(n))+1)]]

#循环求得每一个质数的次方值j，并将结果加乘到result中去
result = 1
for i in myPrime:
    j = 1
    while i ** j <= 20:
        j += 1
    result = result * i ** (j - 1)

print result
```



