---
title: 安装JDK
date: 2016-08-16 13:15:51
tags: 
- java
- 安装
---

## 下载

到 [官网](http://www.oracle.com/technetwork/java/javase/downloads/index-jsp-138363.html) 下载JDK, 默认是最新版本, 以前版本的可以到 [这里](http://www.oracle.com/technetwork/java/javase/archive-139210.html) 选择相应的版本, 下载到本地中.  
我安装的版本是1.7.0_80版本

## 安装

双击下载的exe文件, 运行安装程序.

### 1. 向导
直接点下一步即可
![向导](/images/jdk-setup/setup1.png)

### 2. 定制安装
选择安装的程序, 安装的地址
![定制安装](/images/jdk-setup/setup2.jpg)

### 3. 安装进度
![安装进度](/images/jdk-setup/setup3.png)

### 4. 选择jre安装的地址
![选择jre安装的地址](/images/jdk-setup/setup4.png)
![选择jre安装的地址](/images/jdk-setup/setup5.png)

### 5. 完成
![完成](/images/setup6.png)

### 6. 测试安装是否完成
打开cmd, 敲入`java -version` 看到下图就说明安装成功了.
![测试安装是否完成](/images/jdk-setup/setup7.png)

## 设置
### 1. 设置环境变量
找到我的电脑, 右键->属性->高级系统变量->高级->环境变量
新建变量(系统变量或者用户变量都可以)  
1. 变量名: JAVA_HOME 变量值: 安装目录
2. 变量名: CLASSPATH 变量值: `.;%JAVA_HOME%\lib\dt.jar;%JAVA_HOME%\lib\tools.jar;`
3. 在变量Path中加入`%JAVA_HOME%\bin;%JAVA_HOME%\jre\bin;`记得用英文分号分隔

### 2. 测试环境变量是否设置完成
打开cmd, 敲入`javac -version` 看到下图就说明环境变量设置成功了.
![测试环境变量是否设置完成](/images/jdk-setup/setup8.png)