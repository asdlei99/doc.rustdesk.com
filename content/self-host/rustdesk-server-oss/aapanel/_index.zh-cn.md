---
title: 宝塔面板
weight: 40
---
本手册基于宝塔面板正式版 9.2.0
## 前提
已安装宝塔面板正式版，前往[宝塔面板](https://www.bt.cn/new/index.html)官网，选择对应的脚本下载安装

## 部署
步骤一：登录宝塔面板，在菜单栏中点击 `Docker`
![](images//Docker.png) 

步骤二：首次会提示安装`Docker`和`Docker Compose`服务，点击立即安装，若已安装请忽略。
![](images/install-Docker.png)

步骤三：安装完成后在`Docker-应用商店-实用工具`中找到 `RustDesk`，点击`安装`
![](images/install-RustDesk.png)

步骤四：设置域名等基本信息，点击`确定`
![](images/config-Rustdesk.png)
- 名称：应用名称，默认`RustDesk-随机字符`
- 版本选择：默认`1.1.11`
- 允许外部访问：请勾选。
- 端口：默认情况下，hbbs 监听21115(tcp), 21116(tcp/udp), 21118(tcp)，hbbr 监听21117(tcp), 21119(tcp)。务必在防火墙开启这几个端口， 请注意21116同时要开启TCP和UDP。其中21115是hbbs用作NAT类型测试，21116/UDP是hbbs用作ID注册与心跳服务，21116/TCP是hbbs用作TCP打洞与连接服务，21117是hbbr用作中继服务, 21118和21119是为了支持网页客户端。如果您不需要网页客户端（21118，21119）支持，对应端口可以不开。
- CPU 核心数限制：0为不限制，可根据需要进行修改
- 内存限制：0为不限制，可根据需要进行修改

步骤五：提交后面板会自动进行应用初始化，大概需要`1-3`分钟，初始化完成后即可使用。