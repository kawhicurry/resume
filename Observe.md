---
layout: cv
title: KawhiCurry's Resume
email:
  url: mailto:1145315261@qq.com
  text: 1145315261@qq.com
homepage:
  url: https://kawhicurry.github.io
  text: kawhicurry.github.io
---

# 简历

{% include cv-contact.html %}

## 个人情况

姓名：于思远

邮箱：[1145315261@qq.com](mailto:1145315261@qq.com)

个人博客：[kawhicurry.github.io](https://kawhicurry.github.io)

Github 地址：[https://github.com/kawhicurry](https://github.com/kawhicurry)

完整简历地址： [https://kawhicurry.github.io/resume](https://kawhicurry.github.io/resume)

## 教育经历

**南京邮电大学,本科在读**; 自动化系 `2020-2024`

## 工作经验

### [**南京邮电大学青柚工作室**](https://qingyou.njupt.edu.cn) `2021-recent`

**linux 运维**

进入团队之前，团队没有专职运维，一直由后端同学兼职，服务器权限管理粗放。
业务部署混乱。进入团队之后，个人通过不断学习与思考，依据 Google SRE 理论
和其他 DevOps 理论，通过现代化运维手段，带领团队拥抱 DevOps 与云原生概念，
完成了团队运维体系从零到一的建设，为团队可靠性工程提供理论、数据、技术
支持。

- [技术博客]()
- [个人思考]()

### [**南京邮电大学 Apollo 机器人俱乐部**](https://github.com/Apollo2d/) `2021-2022`

**2D 仿真组组长**

项目本身为对 multi-agent 这一学术问题的具象实现。主要工作为对球队 Cpp 代码
及相关项目进行二次开发，期望仿真足球队在比赛中取得更好成绩。个人主要工
作成果为将团队十年未变的底层库升级为最新版本，并独立开发了部分相关工具。

- [南京邮电大学 Apollo 俱乐部 2023 年校队选拔题目](https://github.com/Apollo2d/NJUPT-2022-apollo2d)
- [Apollo2D 自动比赛脚本](https://github.com/Apollo2d/AutoGame)
- [Apollo2D 比赛环境自动安装脚本](https://github.com/Apollo2d/Apollo_env_install)

## 项目经历

### 南邮小程序 4.0

新版本小程序后端为基于 spring 的**多模块**项目。作为 linux 运维，我为该项目做了
以下工作。

- 基于 kubeadm+ansible（自行编写的 playbook）搭建了一套 kubernetes 集
  群。相关组件的选型如下：
  - 使用 containerd 实现 CRI。
  - 使用 cilium 实现 CNI。(strict no kube-proxy)
  - 使用 rook-ceph 实现 CSI。
- 基于 gitlab runner 设计的一套动态流水线。该流水线拥有以下能力：
  - 持续部署，任何变更都可以直接部署到测试环境。
  - 动态检测，只更新代码有变更的模块。
  - 自动回滚，当部署后容器运行不正常时，有能力自动回滚至上一个版
    本。
  - 效率较高，一方面使用 kubernetes executor 提供的可拓展能力，允许
    多个打包过程同时运行，另一方面为流水线提供了基于 ceph s3 API 的
    shared cache。
  - 镜像缓存，使用 kaniko 进行容器镜像打包时，使用 s3 API 提供自动镜
    像缓存。
- 基于 kube-prometheus-stack+grafana-stack 的全方位观测性平台。
  - 使用 prom-operator 与 CRDs 提供 prometheus 生态本身的各类资源。
  - 使用 prometheus-adapter 提供\*.metrics API。
  - 使用 mimir 对 prometheus 采集的监控数据进行处理并存储至 s3 bucket
    中，同时提供了多种缓存来进行查询优化。
  - 使用 loki+promtail 提供基于 label 的日志采集。
  - 使用 tempo 提供基于 otlp 的链路追踪。
  - 对 alertmanger 进行了一系列配置，使用 Watchdog 功能保证其存活，
    并配置了基本的报警收敛。
  - 使用配置文件申明了一个完全无状态的 grafana。
  - 配置了专用于该业务的 grafana 面板，涵盖 jvm 信息，pod 运行状态，日志查询
    等多个功能。
  - 所有核心组件均开启 HPA。
- 基于 rook 的 ceph 集群，该集群为 k8s 提供了多套 storage class 。也为 mimir、
  loki、tempo、gitlab 等业务提供基于 s3 接口的持久化存储。
- 基于 mysql-operator 的 innodb cluster。为 mysql 集群设置了基于 s3 的
  定时全量备份。
- 基于 redis-operator 的哨兵模式 redisfailover 集群。
- 基于 traefik 的七层负载均衡（少部分业务使用 cilium 的 envoy 作为七层
  负载）。
- 完整的 helm chart 模板。在提供基础的 depolyment、cronjob 与 service 等
  资源的同时，将 jvm 启动参数、模块 resource request 等参数的配置权通过
  value.yaml 交还给开发。

### [南邮镜像站](https://mirrors.njupt.edu.cn)

南邮镜像站最早由南邮 NMG 小组创建，为全校师生及社会提供各类镜像分发
服务。接手镜像站后，个人工作成果如下：

- 完成了镜像站从旧机器到新机器的迁移。
- 处理[镜像添加请求](https://github.com/NJUPT-Mirrors-Group/issues/issues?q=is%3Aissue+is%3Aclosed)，定时更新帮助文档。
- 向社区提交申请，将镜像站加入到[官方源](https://archlinux.org/mirrors/njupt.edu.cn/)中。

### 其他运维工作

在完全迁移到 k8s 之前，许多业务仍然直接部署在 linux 机器上，以下是有关
此类业务的一些工作。

- 基于 CA 的 ssh 认证，保证开发在一定时间内拥有对服务器的登陆权限。
- 基于 grafana-agent 的监控、日志、链路追踪功能。
- 基于 ansible 的 nginx、sshd 与 grafana-agent 配置分发。
- 迁移与维护私有 gitlab。
- 搭建私有 meterspher，nextcloud。
- 编写了成体系的运维文档。

## 相关技能

### 编程语言

按个人常用程度排名：

bash(5.0+) > C > Go > C++ > Python3

### 操作系统

个人以 Arch Linux 作为日常使用操作系统。相关技能如下：

- 了解各类包管理工具，包括但不限于 apt、yum、pacman。拥有个人维
  护的 [AUR 源](https://aur.archlinux.org/packages?O=0&SeB=m&K=kawhicurry&outdated=&SB=m&SO=d&PP=50&submit=Go)。
- 熟悉 systemd 相关生态，能熟练编写 systemd.service,systemd.path 等
  一系列配置文件。
- 了解 btrfs ,使用 btrfs 管理本地与服务器磁盘。
- 了解 kernel 的编译与 linux 的启动过程。了解 grub2 与 uefi。
- 了解 linux 编程技术，读过 APUE 的一部分。
- 了解 ebpf 技术，实现过简单的 xdp 防火墙。
- 了解性能分析的基本方法与工具，能熟练使用 sysstat 工具和部分 ebpf
  工具

### 计算机网络

拥有基础的计算机网络知识体系，但在以下方面略有深入：

- BGP 路由协议
- ARRP 路由协议
- gRPC 协议
- HTTP 协议

## 其他技能

### 语言能力

- 良好的中文表达能力与交流能力
- 良好的英语阅读能力与书面表达能力
- 良好的中英文文档编写能力

### 运维体系能力

- 有现代运维技术的基本观念，读过 The Site Reliability Workbook, Site
  Reliability Enginerring ,Time managerment of System Administrator
- 有标准化意识，读过部分标准如 FHS、LSB
- 有独立思考能力的能力
- 有充足的危机意识与责任感
- 有强大的学习能力

---
