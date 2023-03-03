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

### 南京邮电大学 本科 自动化系 `2020-recent`

## 工作经验

### [**南京邮电大学 - 青柚工作室 - SRE**](https://qingyou.njupt.edu.cn) `2021-recent`

以SRE的身份解决了小程序开发团队运维理念缺失造成的权限管理粗放，业务部署混乱等问题。个人依据 Google SRE 理论和其他 DevOps 理论，通过不断完善团队基础设施、深度参与项目生命周期管理、依据反馈制定相关规范，带领团队拥抱云原生理念，完成了团队运维体系从零到一的建设。

### [**南京邮电大学 - Apollo 机器人俱乐部 - 2D 仿真组组长**](https://github.com/Apollo2d/) `2021-2022`

个人作为该科研竞赛项目组长，积极与社区交流，深度参与了相关 Cpp 项目的开发，并贡献了一些开源项目。

## 项目经历

### **基础设施建设**

- 搭建了基于 kubeadm + ansible 的一套高可用的 kubernetes 集群。选用了 containerd、rook-ceph、cilium、traefik 等实现了集群中的相关组件。
- 搭建了基于 kube-prometheus-stack（prom-operator、prometheus-adapter）和 grafana-stack （mimir、loki、tempo、phlare）的监控、日志、链路追踪平台，大大提高了对业务与业务链路中基础设施的可观测性。
- 搭建了基于 gitlab runner + kaniko 的流水线，并为各类项目设计了多种流水线模板，保证了业务上线与迭代的敏捷与规范。
- 搭建了基于 gitlab-ci + ansible 的配置分发中心，通过声明式配置降低了 sshd、nginx、grafana-agent、kubernetes CRD、helm value 等配置变更的复杂度。
- 搭建了基于 operator 模式的 mysql innodb cluster 与 sentinel redis cluster，实现了数据库的高可用。

### **[南邮镜像站](https://mirrors.njupt.edu.cn)**

- 完成了镜像站的一次大规模迁移与升级工作，并对nginx配置进行了一定调优，提高了镜像站的用户体验。
- 处理来自多方的[镜像添加请求](https://github.com/NJUPT-Mirrors-Group/issues/issues?q=is%3Aissue+is%3Aclosed)，并及时更新相对应的帮助文档，并申请将镜像站添加至相关[官方源](https://archlinux.org/mirrors/njupt.edu.cn/)。

### **业务生命周期管理**

- 接手并参与了多个业务的迭代与运维工作，通过引入观测工具、优化部署方案等手段提高了已有业务的SLA。
- 及时响应并解决了多次线上故障，通过监控报警、保留现场、事后复盘等方式保证了故障的及时发现与高效解决。
- 参与了多个业务的调研与设计工作，为新业务的架构设计与平稳上线提供了技术支持。
- 为团队运维管理流程制定了一系列规范，并为新旧业务编写了设计与维护文档。

## 相关技能

- 编程语言：能熟练使用编写bash与python脚本，可以使用Go与C/C++进行中间件和底层组件开发。
- 操作系统：使用Arch Linux作为日常使用的操作系统。拥有个人维护的 [AUR 源](https://aur.archlinux.org/packages?O=0&SeB=m&K=kawhicurry&outdated=&SB=m&SO=d&PP=50&submit=Go)。了解systemd，ebpf。
- 性能分析：了解性能分析的基本方法与工具，能熟练使用 sysstat 工具和部分 ebpf 工具。
- 语言能力：良好的中英语阅读能力与文档编写能力。

## 其他技能

- 了解SRE的基本观念，读过 Google 出品的相关书籍。
- 有标准化意识，读过行业相关的常见标准，如 FHS、LSB、OCI。
- 有主动发现问题的意识与独立解决问题的能力，有危机意识与责任感。
