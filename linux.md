### 解压
```
tar -jxvf ***.tar.bz2
tar -zxvf ***.tar.gz
```

### 安装
```
# .rpm
sudo apt install yum
sudo yum localinstall xxx.rpm

# .deb
sudo dpkg -i xxx.deb
```

### 查看磁盘空间
```
df -lh
```

### 每隔1秒刷新GPU内存信息
```
watch -n 1 nvidia-smi
```
