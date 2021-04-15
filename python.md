# python

## 安装

查看python指向

```
ls -l /usr/bin | grep python
```

直接安装

```
apt-get install python3.7
```

提示失败，手动安装

```
wget https://www.python.org/ftp/python/3.7.1/Python-3.7.1.tgz	# python官网找到对应的版本
tar -zxvf Python-3.7.1.tgz
cd Python-3.7.1
./confiure 或者 ./configure --prefix=/usr/local(推荐)
make&&sudo make install
```

验证

```
python3 -V
```

修改指向

```
sudo unlink /usr/bin/python
sudo ln -s /usr/bin/python3.7 /usr/bin/python
```



make test报错ModuleNotFoundError: No module named ‘_ctypes’ 

```
sudo apt-get update
sudo apt-get upgrade
sudo apt-get dist-upgrade
sudo apt-get install build-essential python-dev python-setuptools python-pip python-smbus
sudo apt-get install build-essential libncursesw5-dev libgdbm-dev libc6-dev
sudo apt-get install zlib1g-dev libsqlite3-dev tk-dev
sudo apt-get install libssl-dev openssl
sudo apt-get install libffi-dev
重复操作./configure....
```
