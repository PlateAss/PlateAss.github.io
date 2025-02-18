# 首次登录

需要用户名和密码，需要记住密码

首次登录需要更新源：

```
 sudo apt update
```

然后更新组件:

```
sudo apt upgrade
```

然后才能安装python之类的。

# 安装python

```
apt list|grep python3.1
```

看一下最新的是哪个，我这里看到是3.11

然后

```
sudo apt install python3.11
```

# 安装node

先安装curl，然后下载nvm，然后安装node

```
sudo apt-get install curl
```

```
curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/master/install.sh | bash
```

安装最新的稳定版本

```
nvm install --lts
```
