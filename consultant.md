---
layout: cv
title: KawhiCurry's Resume
email:
  url: mailto:1145315261@qq.com
  text: 1145315261@qq.com
phone:
  url: tel:+8617374668647
  text: 17374668647
homepage:
  url: https://kawhicurry.github.io
  text: kawhicurry.github.io
---

# 于思远

{% include cv-contact.html %}

## 教育经历

### 南京邮电大学 本科 自动化系 `2020-至今`

## 工作经验

[**腾讯音乐集团 - 基础平台部 - 业务运维**](https://join.tencentmusic.com/campus/post-details/?id=12187&refer_code) `2023/06-至今`

个人以业务运维的身份参与路由变更、配置变更等日常运维工作，同时参与开发和建设TME集团接入层相关基础设施。

[**南京邮电大学 - 青柚工作室 - linux运维**](https://qingyou.njupt.edu.cn) `2021/08-至今`

青柚工作室团队主营校内小程序开发业务，代表业务有南邮小程序、南邮镜像站等。个人作为运维负责人，主导了团队运维体系从零到一的建设。在校期间，受学校信息化建设办公室邀请，参与学校基建设施采购招标、服务方案制定等工作。

<!-- [**南京邮电大学 - Apollo机器人俱乐部 - 2D仿真组组长**](https://github.com/Apollo2d/) `2021-2022`

个人作为该科研竞赛项目组长，参与了相关Cpp项目的开发，并贡献了HFO Trainer等开源项目。 -->

## 项目经历

### **统一域名系统**  *腾讯音乐集团* `2023/06-至今`

集团域名接入有多个配置分散在多个系统中。变更大量依靠运维同学手动操作。为此，我们解设了一套统一域名系统，着重解决这一链路上配置不透明与变更困难的问题。

- 对标腾讯IAS，对接GSLB、CLB等上游数据源，打通GSLB-Polaris-RS这一链路
- 自建tnginx集群，通过开源crossplane库维护nginx配置
- 对齐内部运维平台权限、成本等信息，接入平台审批流

### **基础设施维护与运维体系建设** *青柚工作室* `2022/01-2023/05`

接手工作室运维工作后，发现原有运维架构存在权限管理粗放、业务部署混乱、应用配置变更困难、服务可靠性差等问题。为提高业务与基础设施的可用性与稳定性，我采取了以下措施：

- 回收所有服务器与数据库权限，并依据最小权限原则进行权限再分配，为服务器集群开发和建设了基于CA的ssh登录认证体系，结束了权限管理粗放的问题。
- 建设团队私有kubernetes集群，依据Google Borg论文对各类存量服务整理、分类和改造并逐步迁移至集群中，从而保证基础设施的标准统一与部署规范。
- 以gitlab-ci为中心，结合ansible、helm等工具推进gitops体系建设，允许以声明式配置对nginx、sshd、k8s等基础设施进行变更，从而保证了业务迭代的敏捷与配置变更的规范。
- 围绕kube-prometheus-stack与grafana-stack，建设包含监控、日志、链路追踪、性能分析的全链路可观测平台，为业务和基础设施提供完整的可观测能力和基本的告警能力，在为业务开发提供便利便利的同时，将故障发现时间由数小时缩减到五分钟内，进而大幅提升服务可靠性。
- 通过主动发现业务异常和及时响应报警，解决过多起线上事故。并在事后通过复盘、整理、归纳并优化相关问题，最终将整个团队的故障频率由每月10次以上降低到2次以下。

## 相关技能

- 编程语言：能熟练编写bash与python脚本，可以使用Go与C进行中间件和底层组件开发，可以使用vue进行前端开发。
- 操作系统：使用Arch Linux作为日常使用的操作系统，拥有个人维护的[AUR包](https://aur.archlinux.org/packages?O=0&SeB=m&K=kawhicurry&outdated=&SB=m&SO=d&PP=50&submit=Go)。了解systemd，ebpf。
- 性能分析：了解性能分析的基本方法与工具，能熟练使用sysstat、ebpf工具对系统性能问题进行分析。
- 语言能力：良好的中英语阅读能力与文档编写能力。
- 其他能力：了解SRE的基本观念，有标准化意识，有主动发现与解决问题的能力
