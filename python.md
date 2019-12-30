# Python内置函数
###  enumerate()
```python
>>>seasons = ['Spring', 'Summer', 'Fall', 'Winter']
>>> list(enumerate(seasons))
[(0, 'Spring'), (1, 'Summer'), (2, 'Fall'), (3, 'Winter')]
>>> list(enumerate(seasons, start=1))       # 下标从 1 开始
[(1, 'Spring'), (2, 'Summer'), (3, 'Fall'), (4, 'Winter')]


>>>seq = ['one', 'two', 'three']
>>> for i, element in enumerate(seq):
...     print i, element
... 
0 one
1 two
2 three
```

### 字符串
```python
str = "this is string example....wow!!!"
print(str.startswith( 'this' ))
print(str.startswith( 'is', 2, 4 ))
print(str.startswith( 'this', 2, 4 ))
```

### python 技巧
```python
# for循环
data = [read_file(f) for f in files]
# 断言
assert(len(a) == 25)
```