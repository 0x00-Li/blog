# kubernetes 安装

>  kubernetes 简称 k8s  ; 
>
>  大家认识一下logo，船上的舵的一样的图标

​        ![](img\k8s_logo.jpg) 

​        说来惭愧，最早接触k8s 是在2017年，由于自己眼光的局限性，没有跟进学习docker 和 k8s ；然后从2018年到2021年也有接触和实践私有云的绝佳机会，导致自己在云原生方向，停留在只是想想，而没有落地实践（猛吃后悔药）。。。

​         **任何时候，从现在开始都不算晚！**



## 开始安装

> 先来个参考文档：https://zhuanlan.zhihu.com/p/46341911

**基础准备工作**

官方镜像是在gcr.io(Google Container Registry)上，不会科学上网的，可能就访问不到了，所以有一波牛逼的人就普度众生的解决了这个问题（感谢社区的力量）。。。。

### 安装环境

> centos 7
>
> 网络：国内网络
>
> 目标：单节点集群安装

kubernetes 所需要安装的组件如下：

| Master节点                       | Node节点                         |
| -------------------------------- | -------------------------------- |
| etcd-master                      | Control plane(如：calico,fannel) |
| kube-apiserver                   | kube-proxy                       |
| kube-controller-manager          | other apps                       |
| kube-dns                         |                                  |
| Control plane(如：calico,fannel) |                                  |
| kube-proxy                       |                                  |
| kube-scheduler                   |                                  |





