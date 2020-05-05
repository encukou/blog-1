How many ways you know how to convert `int` to `str`? Let's try! Note that complications of the same method don't count.

```python
n = 13

n.__str__()     # 1
str(n)          # 2
'{}'.format(n)  # 3
'%i' % n        # 4
f'{n}'          # 5
format(n, 'd')  # 6

from string import Template
Template('$n').substitute(n=n)  # 7

# similar to other methods:
n.__repr__()
repr(n)
str.format('{}', n)
```

Can you beat it?
