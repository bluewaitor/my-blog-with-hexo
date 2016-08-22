---
title: MongoDB
date: 2016-08-22 10:39:34
tags:
- mongodb
- 安装
- robomongo
---


# 下载

[传送门](https://www.mongodb.com/download-center?jmp=nav#community)

# 安装
傻瓜式安装

到下面步骤的时候:
![选择安装类型](/images/mongodb/mongo1.png)
选择Complete就直接安装, 选择Custom, 则可以自己选择安装什么安装在什么位置.

我选择的是Custom, 到如下步骤:
![选择安装的地址](/images/mongodb/mongo2.jpg)
选择安装的位置, 以及要安装的组件, 点击下一步.

安装完成!

# 配置

1. 在安装目录下新建两个目录, 分别是db和log(在哪里新建可以自己选择, 名字也可以随意取)
![新建文件夹](/images/mongodb/mongo3.png)

2. 在安装目录下新建一个`mongod.cfg`文件, 在里面输入一下内容:

        systemLog:
            destination: file
            path: D:\MongoDB\log\mongod.log
        storage:
            dbPath: D:\MongoDB\db
        processManagement:
           windowsService:
              serviceName: MongoDB
              displayName: blueMongoDB

3. 使配置文件生效
使用管理员权限打开cmd.exe, 输入 `"D:\MongoDB\Server\3.2\bin\mongod.exe" --config "D:\MongoDB\mongod.cfg" --install`
如果没有报错, 则说明配置成功了

4. 输入 `net start MongoDB` 如果显示 `blueMongoDB 服务已经启动成功。` 则说明配置成功且服务已经启动, 此时可以使用 `mongo` 命令连接到 mongodb.

5. `net stop MongoDB` 是停止服务命令.

# 环境变量

`我的电脑->右键->属性->高级系统变量->高级->环境变量`
在 `Path` 中加入MongoDB安装目录下的bin目录.
这样以后在哪个目录都可以使用mongo这个命令了.

# 图形化工具

我使用的是`robomongo`, 挺好用的.
[传送门](https://robomongo.org/)

