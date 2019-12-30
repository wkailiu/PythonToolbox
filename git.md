## git
### Installation
* Windows
https://gitforwindows.org/
* Linux
https://book.git-scm.com/downloads

### Example
```
# 克隆仓库到本地
git clone /path/to/repository

# 添加与提交
git add <filename>
git add *

git commit -m "代码提交信息"

# 推送到远程仓库
git push origin master

## 分支

# 创建分支‘feature_x’并切换过去
git checkout -b feature_x
#切换回主分支
git checkout master
# 再把新建的分支删掉
git branch -d feature_x
# 将分支推送到远程仓库
git push origin <branch>

## 更新本地仓库为最新
git pull
```
### References
> https://www.bootcss.com/p/git-guide/