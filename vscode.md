下载vsix老版本

比如jupyter

通过下面这个网站找到版本号2024.2.2024022001

https://www.vsixhub.com/vsix/

修改下面的链接对应的位置，就可以下载了

linux_amd64版本

https://marketplace.visualstudio.com/_apis/public/gallery/publishers/ms-toolsai/vsextensions/jupyter/2024.2.2024022001/vspackage?targetPlatform=linux-x64

linux_arm64版本

https://marketplace.visualstudio.com/_apis/public/gallery/publishers/ms-toolsai/vsextensions/jupyter/2024.2.2024022001/vspackage?targetPlatform=linux-arm64

编译vscode插件
1.使用pnpm
2.修改插件目录的package.json中的npm为pnpm
3.安装vsce
4.运行vsce package --no-dependencies
