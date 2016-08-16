---
title: 安装maven
date: 2016-08-16 14:00:34
tags: 
- 安装
- maven
---

## 下载

到 [官网](http://maven.apache.org/download.cgi) 下载 Binary zip archive `.zip`格式的文件.

## 安装

安装很简单, 将.zip压缩包解压到要安装的目录即可.

## 环境变量配置

找到我的电脑, `右键->属性->高级系统变量->高级->环境变量`
新建变量(系统变量或者用户变量都可以)  
变量名: M2_HOME 变量值: 安装路径

将`%M2_HOME%\bin;`添加到Path中, 打开cmd, 输入`mvn -v`查看是否成功

![命令行查看版本](/images/maven-setup/maven.png)
