### pickle:读写 .pkl 文件[python自带]
```python
import sys
if sys.version_info[0] == 3:
    import _pickle as pkl
else:
    import cPickle as pkl
    
# import cPickle as pkl	#python2
# import _pickle as pkl	#python3

data={
	'width': 100,
	'name': 'nike',
	'px': [173, 168]}

# write
with open("data.pkl", "wb") as fw:
	pkl.dump(data, fw)

# read
data_read = pkl.load(open("data.pkl", "wb"), encoding='utf-8')

print(data_read)
```
**outputs:**
```
{'width': 100, 'name': 'nike', 'px': [173, 168]}
```
### References
> https://docs.python.org/3/library/pickle.html