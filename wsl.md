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

设置镜像源

```
pip config set global.index-url https://pypi.tuna.tsinghua.edu.cn/simple/
```

# 安装node

安装nvm

```
git clone https://gitee.com/mirrors/nvm .nvm
cd .nvm
bash install.sh
source ~/.bashrc
```

修改源

```
export NVM_NODEJS_ORG_MIRROR=https://npmmirror.com/mirrors/node
```

安装最新的稳定版本

```
nvm install --lts
```

设置镜像源

```
npm config set registry https://registry.npmmirror.com/
```

安装pnpm

```
npm install -g pnpm
```
