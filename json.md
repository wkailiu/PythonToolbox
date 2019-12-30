## json
### Example
```python
import json

data = {'width': 100, 'name': 'nike', 'px': [173, 168]}

# write
with open("data.json", "w") as fw:
	json.dump(data, fw)

# read
with open('data.json') as fr:
	data = json.load(fr)
	print(data)

```
### References
> https://www.runoob.com/python/python-json.html