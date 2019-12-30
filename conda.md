## conda

### 基本信息
```
conda --version # 查看版本
conda update conda # 更新conda
conda -h # 查看conda帮助信息
```

### 环境管理
**注意：名称两边不加尖括号“<>”**
```
conda create -n <env_name> <package_names> # 创建环境
conda create -n python3 python=3.5 numpy pandas
activate <env_name> # 切换环境
deactivate # 退出环境
conda env list # 显示已经创建的环境
conda create -n <new_env_name> --clone <copied_env_name> # 复制环境
conda remove -n <env_name> --all # 删除环境
```

### 包管理[在当前环境下]：
```
conda install <package_name> # 安装包
pip install <package_name> # 当使用 conda install 无法进行安装时，可以使用pip进行安装
conda list # 已安装的包信息
conda remove <package_name> # 卸载当前环境中的包
conda update <package_name> # 更新包
conda upgrade <package_name>
conda update --all # 更新所有包
```
### References
> https://zhuanlan.zhihu.com/p/32925500