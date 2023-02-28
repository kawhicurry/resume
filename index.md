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

# 于思远

{% include cv-contact.html %}

## 教育经历

{% include cv-education.html %}

## 工作经验

### [**南京邮电大学 - 青柚工作室 - SRE**](https://qingyou.njupt.edu.cn) `2021-recent`

解决了小程序开发团队没有专职运维造成的服务器权限管理粗放，业务部署混乱等问题。依据 Google SRE 理论和其他 DevOps 理论，通过现代化运维手段，带领团队拥抱  DevOps 理念，完成了团队运维体系从零到一的建设，通过不断完善团队基础设施，为团队可靠性工程提供理论、数据、技术支持。

### [**南京邮电大学 - Apollo 机器人俱乐部 - 2D 仿真组组长**](https://github.com/Apollo2d/) `2021-2022`

竞赛项目，Cpp 开发。

## 项目经历

### 基础设施维护

- 基于 kubeadm+ansible（自行编写的 playbook）搭建了一套 kubernetes 集群。
  - 使用 containerd 实现 CRI。
  - 使用 cilium 实现 CNI。(strict no kube-proxy)
  - 使用 rook-ceph 实现 CSI。
  - 使用 traefik 和 cilium envoy 作为 ingress controller。
- 基于 kube-prometheus-stack+grafana-stack 的监控、日志、链路追踪平台。
- 基于 mysql-operator 的 innodb cluster。为 mysql 集群设置了基于 s3 的定时全量备份。
- 基于 redis-operator 的哨兵模式 redis 集群。

### DevOps 相关工作

- 基于 gitlab runner+kaniko 为多模块项目设计了一套动态流水线。
- 基于 ansible 的 nginx、sshd 与 grafana-agent 配置分发中心。
- 通用的 helm chart 部署模板与流水线模板

### [南邮镜像站](https://mirrors.njupt.edu.cn)

- 完成了镜像站的小规模迁移。
- 处理[镜像添加请求](https://github.com/NJUPT-Mirrors-Group/issues/issues?q=is%3Aissue+is%3Aclosed)，定时更新帮助文档。
- 向社区提交申请，将镜像站加入到[官方源](https://archlinux.org/mirrors/njupt.edu.cn/)中。

## 相关技能

- 编程语言：能熟练使用编写bash与python脚本，可以使用Go与C/C++进行中间件和底层组件开发。
- 操作系统：使用Arch Linux作为日常使用的操作系统。拥有个人维护的 [AUR 源](https://aur.archlinux.org/packages?O=0&SeB=m&K=kawhicurry&outdated=&SB=m&SO=d&PP=50&submit=Go)。了解systemd，btrfs，ebpf。
- 性能分析：了解性能分析的基本方法与工具，能熟练使用 sysstat 工具和部分 ebpf 工具。
- 语言能力：良好的中英语阅读能力与文档编写能力。

## 其他技能

- 了解SRE的基本观念，读过 Google 出品的相关书籍
- 有标准化意识，读过部分标准如 FHS、LSB、OCI
- 有独立面对问题和解决问题的能力
- 有充足的危机意识与责任感
