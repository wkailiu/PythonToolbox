## conda
### 查看版本
```
conda --version # 查看版本
```
### 更新conda
```
conda update conda
```
### 查看conda帮助信息
```
conda --help == conda -h
```
### 创建环境
```
conda create --name <env_name> <package_names>
conda create -n python3 python=3.5 numpy pandas
```
### 切换环境
```
activate <env_name>
```
### 退出环境
deactivate

### 显示已经创建的环境
conda info --envs
conda info -e
conda env list

### 复制环境
conda create --name <new_env_name> --clone <copied_env_name>

### 删除环境
conda remove -n py36 --all


### 获取当前环境中已安装的包信息
conda list

### 在当前环境中安装包
conda install <package_name>

* 当使用 conda install 无法进行安装时，可以使用pip进行安装
pip install <package_name>

### 卸载当前环境中的包
conda remove <package_name>

### 更新当前环境的包
conda update <package_name>
conda upgrade <package_name>
conda update --all