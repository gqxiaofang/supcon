# ubuntu-git
安装git
```
sudo apt-get install git
```
生成密钥 ->  yes ->  生成~/.ssh/id_rsa.pub

```
ssh-keygen -t rsa -C "1813298696@qq.com"
```
设置密钥
github -> Account Setting -> SSH Keys -> Add SSH

验证是否连接

```
ssh -T git@github.com
```

设置username和email 

```
git config --global user.name "gqxiaofang"
git config --global user.email 1813298696@qq.com
```

添加远程仓库

```
git remote add origin git@github.com:yourName/yourRepo.git
```

```

```

