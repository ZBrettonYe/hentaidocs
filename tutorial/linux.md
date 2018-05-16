# Linux

## 安装&配置

安装以后可通过　ssr start或者　ssr config　命令运行ssr  
使用root用户登录，运行以下命令：

```text
# wget --no-check-certificate https://www.djangoz.com/ssr 
wget https://onlyless.github.io/ssr
sudo mv ssr /usr/local/bin
sudo chmod 766 /usr/local/bin/ssr
ssr install
ssr config
```

ssr的配置就不说明了，很简单的

## 更新

**该脚本会运行git命令，所以前提先安装git**

```text
sudo apt-get install git
```

## **设置开机自启动**

```text
sudo vim /etc/rc.local
```

里面直接添加要运行的命令

```text
#!/bin/sh -e
#
# rc.local
#
# This script is executed at the end of each multiuser runlevel.
# Make sure that the script will "exit 0" on success or any other
# value on error.
#
# In order to enable or disable this script just change the execution
# bits.
#
# By default this script does nothing.

sudo ssr start
exit 0
```

系统会默认启动，直接实测开机会自动运行  
思想就是直接让系统开机启动一条sudo命令，如果这个不行的话，可以去网上参考自己linux版本的开机启动脚本或命令,然后添加一条命令就可以了

```text
sudo ssr start
```

教程来自：[https://www.djangoz.com/2017/08/16/linux\_setup\_ssr/](https://www.djangoz.com/2017/08/16/linux_setup_ssr/)

