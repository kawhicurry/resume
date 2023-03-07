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

### 南京邮电大学 本科 自动化系 `2020-至今`

## 工作经验

[**南京邮电大学 - 青柚工作室 - linux运维**](https://qingyou.njupt.edu.cn) `2021-至今`

青柚工作室团队主营小程序开发业务，代表业务有南邮小程序、邮你来办、南邮镜像站等。个人作为运维及后端负责人，主导了团队运维体系从零到一的建设。

[**南京邮电大学 - Apollo机器人俱乐部 - 2D仿真组组长**](https://github.com/Apollo2d/) `2021-2022`

个人作为该科研竞赛项目组长，参与了相关Cpp项目的开发，并贡献了HFO Trainer等开源项目。

## 项目经历

### **Saas平台维护与改造** `2022/01-2022/07`

接手运维工作后，发现原有运维架构存在权限管理粗放、业务部署混乱、应用配置变更困难、服务可拓展性差等问题。为提高基础设施的可用性与稳定性，我采取了以下措施：

- 以gitlab-ci为中心，结合ansible，将业务运维操作自动化。该系统在保证业务CI/CD的同时，允许使用声明式配置对基础服务（如nginx、sshd）进行配置变更，进而保障业务迭代与配置变更的规范与敏捷。
- 建立基于prometheus+loki+tempo的监控、日志、链路分析平台，结合grafana与alertmanager，为业务与基础设施提供基本观测能力与告警能力，在为业务开发与迭代的调试与性能优化提供便利的同时，将故障发现时间由数小时缩减到5分钟以内。
- 通过主动发现业务异常和及时响应报警，处理过多起线上事故。并在事后通过复盘、整理、归纳并解决相关问题，最终将整个基础设施的故障率由每月10次以上降低到2次以下。
- 回收所有服务器与数据库的登陆权限后，基于最小权限原则重新进行了权限划分，同时为服务器建立了基于CA的ssh登陆认证体系，从而大大提升服务器与数据库的安全性。

### **云基础设施建设** `2023/02-至今`

随着业务规模的扩大，团队已有的基础设施已不能满足业务增长的需求，为进一步将运维工作自动化、平台化，团队决定建设一套私有云平台，并结合公有云一同为新老业务提供可拓展性和治理能力更强的运行环境。我的工作成果如下：

- 基于kubeadm+ansible搭建了一套高可用的kubernetes集群，选用containerd、rook-ceph、cilium、traefik等来实现集群中的相关组件，以此作为私有云平台的基础设施。
- 建设基于kube-prometheus-stack与grafana-stack的全链路可观测性平台，基于此平台为基础设施及业务项目提供包括监控指标、日志分析、链路追踪、性能分析的全面观测能力。
- 部署基于operator模式的mysql innodb cluster与sentinel redis cluster，进而实现数据库的高可用。
- 结合实际需求与Google Borg论文，对业务进行整理、分类与改造，如将spring定时任务转换为cronjob，将前端静态产物转为使用公有云OSS+CDN部署等，从而确保业务完美融入混合云平台。

## 相关技能

- 编程语言：能熟练使用编写bash与python脚本，可以使用Go与C/C++进行中间件和底层组件开发。
- 操作系统：使用Arch Linux作为日常使用的操作系统，拥有个人维护的[AUR 源](https://aur.archlinux.org/packages?O=0&SeB=m&K=kawhicurry&outdated=&SB=m&SO=d&PP=50&submit=Go)。了解systemd，ebpf。
- 性能分析：了解性能分析的基本方法与工具，能熟练使用sysstat、ebpf工具对系统性能问题进行分析。
- 语言能力：良好的中英语阅读能力与文档编写能力。

## 其他能力

- 了解SRE的基本观念，读过Google出品的相关书籍。
- 有标准化意识，了解行业相关的常见标准，如FHS、LSB、OCI。
- 有主动发现问题的意识与独立解决问题的能力，有危机意识与责任感。
