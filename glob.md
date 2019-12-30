## glob
### 文件名模式匹配
* *匹配任意
* []匹配包含的值
### Example
```python
import os
from glob import glob

segm_files = sorted(glob(os.path.join(segm_dir, '*.png')))
pose_files = sorted(glob(os.path.join(pose_dir, '*.json')))

>>> glob('./[0-9].*')
['./1.gif', './2.txt']
```

### References
> https://docs.python.org/2/library/glob.html