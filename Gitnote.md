# 尚硅谷Git课程笔记

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
 ![工作机制流程图](image\image-0.png)
2. 代码托管中心（即远程库）是基于网络服务器的远程代码仓库
- 局域网: GitLab
- 互联网： GitHub（外网）；Gitee（国内网站）

## 1.7 Git安装和客户端的使用
1. 根据系统下载对呀的安装包
2. 安装路径不能有中文与空格
3. 推荐D:\Git
4. Git选项配置，推荐默认配置
![配置选项](image\image-1.png)
5. 编辑器选择
![编辑器选择](image\image-2.png)
6. 其他默认配置
7. 后台客户端连接协议，使用OpenSSL协议进行连接
8. 安装每个界面都有解释，复习视频即可
9. 在git bash中查询git版本
![查询命令](image\image-3.png)

## 1.8 Git命令_设置用户签名
1. Git常用命令
![常用命令](image\image-4.png)
2. 设置用户签名（设置一次即可，不设置的话提交代码会报错）
- git config --global user.name 用户名
- git config --global user.email 邮箱
3. 在桌面打开git客户端，执行以下操作
![设置用户签名](image\image-5.png)
4. 在C盘下用户目录下的huangweiyuan文件夹中可以看到一个.config文件，文件里记录着配置好的用户签名
5. 注意：用户签名和将来登录GitHUb（或其他代码托管中心）的账号没有任何关系，该处用户只是代表windows的本地Git客户端

## 1.9 Git命令_初始化本地库
1. 基本语法
- git init
![git init](image\image-6.png)
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
- 实操示例![git commit](image\image-7.png)
- git reflog 查看版本信息（版本号前七位）
- git log 查看版本详细信息（完整版本号），提交作者提交时间等

## 1.13 Git命令_修改文件
1. 基本语法
- git add 修改后的文件
- git restore <file> 放弃工作区的修改，回到未修改的状态
- git restore --staged <file>..." to unstage

## 1.14 Git命令_版本穿梭
1. 基本语法
- git reset --hard <版本号前七位>
- 实操示例![git reset](image\image-8.png)
- Git切换版本，底层其实是移动的HEAD指针，原理如下图：![指针移动](image\image-10.png)


## 1.15 Git分支_概述和优点
1. 什么是分支
- 在版本控制过程中，同时推进多个任务，为每个任务，我们可以创建每个任务的单独分支
- 使用分支意味着程序员可以把自己的工作从开发主线上分离开来，开发自己分支的时候，不会影响主线分支的运行
   - 分支底层其实也是指针的引用
2. ![分支流程](image\image-11.png)
3. 分支的好处
- 同时并行推进多个功能开发
- 各个分支在开发过程中，某一个分支开发失败，不会对其他分支有任何影响

## 1.16 Git分支_查看&创建&切换
1. 分支的操作![分支命令](image\image-12.png)
2. 查看分支
- git branch -v
3. 创建分支
- git branch <分支名>
- 实例操作![创建分支](image\image-13.png)
1. 切换分支
- git checkout <分支名>
- 实例操作![切换分支](image\image-14.png)

## 1.17 Git分支_合并分支（正常合并）
1. 合并分支
- 要先切换到master分支上，然后合并其他分支
- git merge <分支名>
- 实例操作![合并分支](image\image-15.png)

## 1.18 Git分支_合并分支（冲突合并）
1. 代码冲突合并
- 冲突产生原因：合并分支时，两个分支在同一个文件的同一个位置有两套完全不同的修改。Git无法替我们决定使用哪一个，必须认为决定新代码内容。
- 合并冲突解决后，git commit -m""后不需要再跟文件名，否则会报错
2. 底层原理也是指针的移动

## 1.19 Git团队协作_团队内协作和跨团队协作
1. 团队内协作
- 本地库1`push`到远程库1
- 远程库1`clone`到本地库2
- 修改过后的本地库2再次`push`到远程库1（经过开发者同意）
- 本地库1从远程库1`pull`更新的代码
- ![流程演示](image\image.png)
2. 跨团队协作
- 远程库1`fork`到远程库2
- 远程库2`clone`到本地库3
- 本地库3修改后`push`到远程库2
- 远程库2发送`pull request`到远程库1
- 远程库1对`pull request`进行审核，审核通过后远程库2可以merge到远程库1
- 本地库1、2从远程库1`pull`更新的代码
- ![流程演示](image\image-16.png)

## 2.1 GitHub_创建远程库&创建别名
1. 创建远程仓库
-![创建远程仓库](image\image-17.png)
- 远程库名字一般和本地库一样
- 远程库连接：HTTPS和SSH。![远程库连接](image\image-18.png)
2. 创建远程库别名
- git remote -v 查看当前所有远程地址别名
- git remote add 别名 远程地址HHTPS
- 后续方便通过别名直接向远程库进行push和pull操作
- ![创建别名](image\image-19.png)

## 2.2 GitHub_推送本地库到远程库
1. 推送代码
- git push 远程库别名 分支
- ![推送代码](image\image-20.png)

## 2.3 GitHub_拉取远程库到本地库
1. 拉取代码
- git pull 远程库别名 分支
- ![拉取代码](image\image-21.png)

## 2.4 GitHub_克隆远程库到本地
1. 克隆远程库
- git clone 远程库HTTPS链接
- 克隆代码不需要登录账号,因为这是开源库
- clone会做如下操作：1.拉取代码 2.初始化本地仓库 3.创建别名 origin

## 2.5 GitHub_团队内协作
1. 团队内推送代码
- git push 远程库链接 分支
- 没有权限给别人的远程库推送代码，需要远程库的开发者邀请其他合作者进来，其他合作者才可以向该该远程库推送代码
- 在settings的manage access处点击invite a collaborator后，输入被邀请合作者的GitHub邮箱，输入邮箱确认后在pending invite处复制链接发给合作者
- 合作者同意申请后成为项目成员，项目成员拥有权限推送代码

## 2.6 GitHub_跨团队协作
1. GitHub左上角可以搜索各种各样的开源库
2. 跨团队协作
- 作为团队外的开发者，首先进入别人 的项目，点击右上角Fork，即可在自己远程库中复制别人的项目，然后在本地库中克隆自己远程库的代码进行修改（也可以通过克隆别人的远程库到本地库进行修改），修改完成后的代码再push到自己的远程库。
- click `Pull request`, then click `New request`, finally click `Create request`.
- 开发者可以在GitHub上看到别人的`Pull request`，然后审核确认后点击merging即可合并代码。

## 2.7 GitHub_SSH免密登录
1. SSH免密登录
- 在C盘打开用户文件夹，再打本地用户文件，打开git bash输入ssh-keygen -t rsa -C 815519343@qq.com，输入后敲三次回车键，会在该目录下生成.ssh文件夹，里面包含两个文件：id_rsa是私钥，id_rsa.pub是公钥
- 打开id_rsa.pub复制内容
- 打开GitHub网站，点击头像下的settings，在左侧点击SSH and GPC keys，创建SSH keys，然后粘贴公钥内容即可。

## 3.1 GitLab_简介和安装环境准备
1. GitLab简介：使用Git左为代码管理工具，并在此基础上搭建起来的web服务
2. 如何搭建GitLab服务器

## 3.2 GitLab_安装&初始化服务&启动服务
## 3.3 GitLab_登录并创建远程库
## 3.4 GitLab_IDEA集成GitLab
- GitLab操作于GitHub类似，不再叙述

## 4.1 Git_课程总结
1. 熟悉常用的Git命令
2. 忘了哪部分内容复习视频
3. IDEA集成GitHub未学习







