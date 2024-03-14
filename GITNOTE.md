# 1.尚硅谷Git课程笔记

## 1.1 Git课程介绍
1. Git
- Git介绍 分布式版本控制工具 VS 集中式版本控制工具
- Git安装 
- Git命令 基于开发案例，常用GIT命令
- Git分支 分支特性 分支创建 分支转换 分支合并 代码合并冲突解决
- Idea 集成Git

2. GitHub
- 创建远程库
- 代码推送 Push
- 代码拉取 Pull
- 代码克隆 Clone
- SSH免密登录
- Idea集成GitHub

3. GitLab
- GitLab服务器的搭建和部署
- Idea集成GitLab

4. 课程目标：五小时熟练掌握Git GitHub GitLab的使用

## 1.2 Git官网介绍
1. Git概述
- Git是一个免费的、开源的分布式版本控制系统
- 具有廉价的本地库、方便的暂存区域和多个工作流分支等特性
- 熟悉Git官网

## 1.3 Git概述_版本控制介绍
1. 版本控制是一种记录文件内容变化，以便将来查阅特定版本修订情况的系统
2. 版本控制最重要的是可以记录文件修改历史记录，从而让用户可以查看历史版本，方便版本切换
3. 为什么需要版本控制？个人开发过渡到团队协作

## 1.4 Git概述_分布式版本控制VS集中式版本控制
1. 集中式版本控制，一个集中管理的中央服务器
2. Git分布式版本控制，代码托管中心（即远程库）


## 1.5  Git概述_发展历史
1. 2005年，Linus用C语言开发了Git
2. 2008年，GitHub上线

## 1.6 Git概述_工作机制和代码托管中心
1. 工作机制
 ![工作机制流程图](image.png)
2. 代码托管中心（即远程库）是基于网络服务器的远程代码仓库
- 局域网: GitLab
- 互联网： GitHub（外网）；Gitee（国内网站）

## 1.7 Git安装和客户端的使用
1. 根据系统下载对呀的安装包
2. 安装路径不能有中文与空格
3. 推荐D:\Git
4. Git选项配置，推荐默认配置
![配置选项](image-1.png)
5. 编辑器选择
![编辑器选择](image-2.png)
6. 其他默认配置
7. 后台客户端连接协议，使用OpenSSL协议进行连接
8. 安装每个界面都有解释，复习视频即可
9. 在git bash中查询git版本
![查询命令](image-3.png)

## 1.8 Git命令_设置用户签名
1. Git常用命令
![常用命令](image-4.png)
2. 设置用户签名（设置一次即可，不设置的话提交代码会报错）
- git config --global user.name 用户名
- git config --global user.email 邮箱
3. 在桌面打开git客户端，执行以下操作
![设置用户签名](image-5.png)
4. 在C盘下用户目录下的huangweiyuan文件夹中可以看到一个.config文件，文件里记录着配置好的用户签名
5. 注意：用户签名和将来登录GitHUb（或其他代码托管中心）的账号没有任何关系，该处用户只是代表windows的本地Git客户端

## 1.9 Git命令_初始化本地库
1. 基本语法
- git init
![git init](image-6.png)
2. 初始化后会在本地库生成.git文件

## 1.10 Git命令_查看本地库命令
1. 基本语法
- git status
- On branch master 在主分支
- No commits yet 未提交过文件

## 1.11 Git命令_添加暂存区
1. 基本语法
- git add <文件名>，例如：git add GITNOTE.md
- 文件只存在于暂存区里面
- 可以删除暂存区里的文件
- git rm --cached <文件名>

## 1.12 Git命令_提交本地库
1. 基本语法
- git commit -m "日志信息" <文件名>
- 实操示例![git commit](image-7.png)
- 