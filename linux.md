## Shell

常用Sheel程序 Bash脚本

```
Bourne Shell -> /bin/sh->Bash Bash
```

```
declare -i age=20 # 声明变量
declare -rx OS=LINUX
echo $age
echo $OS
```

### 帮助命令

```
man ls
ls --help | more
```

### 网络操作

```
ifconfig eth0 192.168.1.15 netmask 255.255.255.68 broadcast 192.168.1.158 up
ifconfig eh0 down
ifup eth0
ifdown eth0
```

```
echo $pwd
```

预处理、编译、汇编、连接

### make

```
Makefile
target :dependency
	command
clean:
	rm -f *.o
VARNAME=string //定义变量
${VARNAME}	//引用变量

```



