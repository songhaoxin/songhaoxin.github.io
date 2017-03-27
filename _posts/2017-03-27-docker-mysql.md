---
layout: post
title: 用Docker安装 mysql
categories: 技术
description: 
keywords: Docker mysql
---




![Marathon](/images/posts/mysql/home.png)

本文主要介绍如何在Docker中安装mysql

## 下载 mysql 镜像  

使用下面命令，可以下载到 mysql 镜像 （首次需要下载，后续就不需要执行这个命令了）
> ```docker pull mysql```
  
  执行如下命令，可以启动一个 mysql 容器  
  
  > ``` docker run -d -p 127.0.0.1:3306:3306 --name mysql -v docker/mysql/data:/var/lib/mysql -e MYSQL_ROOT_PASSWORD="111111" mysql:latest ```  
  
  上面命令 docker run 的参数解释如下：  
  
  > ```-d(Detached)```表示容器将以后台模式运行，所有I/O数据只能通过网络资源或者共享卷组来进行交互。  
  > ```-p 127.0.0.1:3306:3306 ```将主机（127.0.0.1）的端口 3306 映射到容器的端口 3306 中。这样访问主机中的 3306 端口就等于访问容器中的 3306 端口。  
  > ```--name mysql```给容器取名为 mysql，这样方便记忆。  
  > ```-v docker/mysql/data:/var/lib/mysql```将本机的文件目录挂载到容器对应的目录（/var/lib/mysql）中。这样可以通过数据卷实现容器中数据的持久化。  
  > ```-e MYSQL_ROOT_PASSWORD="111111"```-e 表示设置环境变量，此处设置了 mysql root 用户的初始密码为 111111。  
  > ```mysql:latest```表示使用 mysql 为 latest 启动一个容器。  
  
  执行完上面的命令，就完成了 mysql 在 Docker 中的虚拟化。此时我们可以利用 mysql 的客户端工具连接到这个 Docker 中的 mysql上。连接配置信息如下：  
  
  > ``` Hostname``` 127.0.0.1
  > ``` Port``` 3306
  > ```Username``` root
  > ```Password``` 111111   
  
  当我们不需要使用这个 mysql 容器时，只需要停掉该容器即可，对主机不会产生任何配置上的影响，非常方便。
在上面的介绍中，我们主要做了 3 件事：第一是 mysql 镜像的下载；第二是 mysql 容器的启动；第三是 利用数据卷实现 mysql 的持久化。

## 连接 mysql 

### 命令终端
![](/images/posts/mysql/mysqlcmd.png)  

### 其他可视化工具
![](/images/posts/mysql/mysqltool1.png)   

![](/images/posts/mysql/mysqltool2.png) 


