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

# KawhiCurry

{% include cv-contact.html %}

## 个人情况

{% include cv-person.html %}

## 教育经历

{% include cv-education.html %}

### [**南京邮电大学青柚工作室**](https://qingyou.njupt.edu.cn) `2021-recent`

**linux 运维**

进入团队之前，团队没有专职运维，一直由后端同学兼职，服务器权限管理粗放。
业务部署混乱。进入团队之后，个人通过不断学习与思考，依据 Google SRE 理论
和其他 DevOps 理论，通过现代化运维手段，带领团队拥抱 DevOps 与云原生概念，
完成了团队运维体系从零到一的建设，为团队可靠性工程提供理论、数据、技术
支持。

### [**南京邮电大学 Apollo 机器人俱乐部**](https://github.com/Apollo2d/) `2021-2022`

**2D 仿真组组长**

项目本身为对 multi-agent 这一学术问题的具象实现。主要工作为对球队 Cpp 代码
及相关项目进行二次开发，期望仿真足球队在比赛中取得更好成绩。个人主要工
作成果为将团队十年未变的底层库升级为最新版本，并独立开发了部分相关工具。

## 项目经历

### 南邮小程序 4.0

新版本小程序后端为基于 spring 的**多模块**项目。作为 linux 运维，我为该项目做了
以下工作。

- 基于 kubeadm+ansible（自行编写的 playbook）搭建了一套 kubernetes 集群。
- 基于 gitlab runner 设计的一套动态流水线。该流水线拥有动态检测、自动回滚、并行打包、多层缓存等功能。
- 基于 kube-prometheus-stack+grafana-stack 的监控、日志与链路追踪平台。
- 基于 rook 的 ceph 集群。
- 基于 mysql-operator 的 innodb cluster。
- 基于 redis-operator 的sential-redisfailover cluster。
- 基于 traefik 和 cilium envoy 的 ingress controller。
- 为模块设计的 helm chart 模板。

### [南邮镜像站](https://mirrors.njupt.edu.cn)

南邮镜像站为全校师生及社会提供各类镜像分发服务。接手镜像站后，个人工作成果如下：

- 完成了镜像站从旧机器到新机器的迁移。
- 处理[镜像添加请求](https://github.com/NJUPT-Mirrors-Group/issues/issues?q=is%3Aissue+is%3Aclosed)，定时更新帮助文档。
- 扩大影响力，向社区提交申请，将镜像站加入到[官方源](https://archlinux.org/mirrors/njupt.edu.cn/)中。

### 其他运维工作

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

- 拥有个人维护的 [AUR 源](https://aur.archlinux.org/packages?O=0&SeB=m&K=kawhicurry&outdated=&SB=m&SO=d&PP=50&submit=Go)。
- 熟悉 systemd 相关生态，能熟练编写 systemd.service,systemd.path 等一系列配置文件。
- 了解 btrfs ,使用 btrfs 管理本地与服务器磁盘。
- 了解 kernel 的编译与 linux 的启动过程。了解 grub2 与 uefi。
- 了解 linux 编程技术，读过 APUE 的一部分。
- 了解 ebpf 技术，实现过简单的 xdp 防火墙。
- 了解性能分析的基本方法与工具，能熟练使用 sysstat 工具和部分 ebpf 工具

### 计算机网络

拥有基础的计算机网络知识体系，但在以下方面略有深入：

- BGP 路由协议
- VRRP 协议
- gRPC 协议
- HTTP 协议

## 其他技能

### 语言能力

- 良好的中文表达能力与交流能力
- 良好的英语阅读能力与书面表达能力
- 良好的中英文文档编写能力

### 运维体系能力

- 有现代运维技术的基本观念，读过 Google SRE 相关书籍
- 有标准化意识，读过部分标准如 FHS、LSB
- 有充足的危机意识与责任感
- 有独立思考的能力

---
