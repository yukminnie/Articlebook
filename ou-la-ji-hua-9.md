```py
#!/usr/bin/env python

for a in xrange(1, 334):
    for b in xrange(a, 501):  #由于b大于a，因此这里设计循环最小值等于a
        c = 1000 - a - b
        if c ** 2 == a ** 2 + b ** 2:
            print a, b, c, a * b * c
```



