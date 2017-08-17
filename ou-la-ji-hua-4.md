## **最大回文乘积** {#最大回文乘积}

回文数就是从前往后和从后往前读都一样的数。由两个2位数相乘得到的最大回文乘积是 9009 = 91 × 99。

找出由两个3位数相乘得到的最大回文乘积。

> ## **Largest palindrome product** {#Largest-palindrome-product}
>
> A palindromic number reads the same both ways. The largest palindrome made from the product of two 2-digit numbers is 9009 = 91 × 99.
>
> Find the largest palindrome made from the product of two 3-digit numbers.

```py
#!/usr/bin/env python

# 定义回文数判断函数
def palindrome(n):
    lenN = len(str(n))
    for i in xrange(lenN/2):
        if str(n)[i] != str(n)[-1-i]:
            return False
    return True

myList = [i * j for i in xrange(999,99,-1) for j in xrange(999,99,-1)]
myList.sort(reverse=True)    #将myList从大到小排列，方便循环找到答案后跳出程序。

for eachItem in myList:
    if palindrome(eachItem):
        print eachItem
        break
```



