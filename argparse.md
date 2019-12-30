## argparse

```python
import argparse
parser = argparse.ArgumentParser()

parser.add_argument('name', type=str, help="Sample name")
parser.add_argument('--opt_steps_pose', '-p', default=5, type=int, help="Optimization steps pose")

args = parser.parse_args()

print(args.name)
print(args.opt_steps_pose)
```

### References
> https://docs.python.org/zh-cn/3/library/argparse.html
> from absl import flags 用途与此相同