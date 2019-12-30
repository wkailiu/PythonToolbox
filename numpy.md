### Installation
```
pip install numpy
conda install numpy
```
### Example
```python
import numpy as np
# list to numpy
a = np.array([1, 2, 3], dtype=float)
print(a)
a = np.array([[1, 2], [3, 4]])  

# dtype 参数

# 'i1', 'i2','i4','i8' 代替
# int8, int16, int32, int64
# np.int8 = 'i1' = 'int8'
# float = 'f'
a = np.array([1,  2,  3], dtype='int8') 
a = np.array([1,  2,  3], dtype='f') 

## numpy 数组属性
a = np.arange(24).reshape(2, 4, 3)

# 维度
a.ndim # 3
a.shape # (2, 4, 3)
a.dtype

## 创建数组
# 未初始化
np.empty(shape, dtype=None) 
# 全0
np.zeros(shape, dtype=None) 
# 全1
np.ones(shape, dtype=None)
# 序列step
np.arange(start=0, stop, step=1, dtype=None)
# 等差数列
np.linspace(start, stop, num=50, endpoint=True, retstep=False, dtype=None)
# 等比数列
np.logspace(start, stop, num=50, endpoint=True, base=10.0, dtype=None)

## 切片和索引
a = np.arange(10)  
b = a[2:7:2]   # 从索引 2 开始到索引 7 停止，间隔为 2
a[2:7]
a[2:]
# 多维度之间用,隔开 
# ... 表示所有
a = np.array([[1,2,3],[3,4,5],[4,5,6]])
a[..., 1:]
a[1, ...]

```

### References
> * https://www.runoob.com/numpy/numpy-tutorial.html
