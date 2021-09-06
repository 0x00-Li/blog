# Kubernetes 基本概念

首先来看下集群的整体的运行时架构

![](E:\ldm-git\blog\tech\kubernetes\img\k8s_arch.png)

核心概念：

- Pod

  - Pod是“容器”的容器，可以包含多个“Container”
  - Pod是K8S最小可部署单元，一个Pod就是一个进程
  - Pod内部容器网络互通，每个Pod都有独立的虚拟IP
  - Pod都是部署完整的应用或模块

  基本机构如下：

  ![](E:\ldm-git\blog\tech\kubernetes\img\pod.png)

  pod的基本设计结构如上，具体使用，公司根据不同的情况而定。可以在一个pod中部署一个完整应用webui和redis，也可以在pod中只部署一个tomcat。在使用上非常灵活

  

  每个Pod中必须包含一个Pause容器，Pause整体的目标是为了让内部的容器形成一个整体，Pause容器的用途：

  1. 存储容器本身的信息
  2. 在网络上共享命名空间

  ![](E:\ldm-git\blog\tech\kubernetes\img\pause.jpg)

- Container(容器)

  在上面概念中已经详细涉及到，不过多介绍

- Label（标签）

  说明性内容，标识一个Pod的名字

- Replication Controller (复制控制器)

  控制副本数量

- Service( 服务)

- Node （节点）

- kubernetes Master(kubernetes 主节点)

- kubelet

  用于执行相应的命令 

- kube-proxy

  是一个代理，通过proxy实现跨节点通信

- docker

  整体容器的运行环境

## 通过kubeadm 安装集群



