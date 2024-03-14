
# 下面设置Git Bash中使用vscode命令打开文件。

## 1. 创建gitbash命令文件

- 新建一个文件，以要使用的命令命名，比如vscode(不要有其他后缀)。内容如下：

>#!/bin/sh
 "C:\vscode\Code.exe" $1 &

 - C:\vscode\Code.exe是vscode可执行文件的路径

- 将新建的文件保存到D:Git\mingw64\bin目录下。即Git安装目录下的文件夹内。

## 2. 命令说明
- 第一行#!/bin/sh，说明这是个shell脚本
- 第二行，指定所要配置的程序的安装目录，此处为我的电脑上vscode软件所在路径
- 第二行$1是获取vscode命令后的第一个参数，即输入参数
- 第二行&指定命令在后台打开。这样文件不会在gitbash内打开
- 使用`vscode`命令打开vscode
- 直接使用`vscode命令加文件名`，打开指定的文件。例如：`vscode debug.tcl`
