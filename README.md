# minikube

<img src="https://github.com/kubernetes/minikube/raw/master/images/logo/logo.png" width="100" alt="minikube logo">

由于网络原因 Minikube 往往无法正常使用，所以我对 Minikube 进行了一些修改，使其可以正常使用。

<img src="https://raw.githubusercontent.com/kubernetes/minikube/master/site/static/images/screenshot.png" width="575" height="322" alt="screenshot">

## Features

经测试可不受国外网络影响，可正常使用的功能有

* dashboard
* metrics server
* ingress
* portainer

未经测试理论可用的功能有

* efk
* istio
* istio-provisioner
* kong
* olm
* registry

部分镜像含有 sha256 docker 戳，不含版本标签，导致国内环境无法正常拉取，故在此处使用了非官方镜像，还请谨慎使用。

* gpu

## 编译与安装

deb 格式

```shell
make debs
```

linux 二进制格式

```shell
make linux
```

## 使用指南

使用 docker cri

```shell
minikube start --driver=docker
```

使用 calico cni

```shell
minikube start --cni=calico
```

开启高可用集群

```shell
minikube start --ha=true 
```

开启 dashboard

```shell
minikube dashboard
```

开启 efk addon

```shell
minikube addons enable efk
```

## 官方文档连接

https://minikube.sigs.k8s.io/docs/

## 反馈方式

如果你有任何问题，可以通过以下方式联系我

email: douzengrui@gmail.com

