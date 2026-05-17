---
layout: cv
title: KawhiCurry's Resume
email:
  url: mailto:kawhicurry@foxmail.com
  text: kawhicurry@foxmail.com
homepage:
  url: https://kawhicurry.github.io
  text: kawhicurry.github.io
---

# 于思远

{% include cv-contact.html %}

## 教育经历

### 南京邮电大学 本科 自动化系 `2020-2024`

## 工作经验

### 腾讯云 - SRE 稳定性工程师 `2024-至今`

负责云基础设施的稳定性保障，涵盖 on-call 响应、分布式治理、变更管控、可观测性建设。

**常态 on-call 与故障响应**

- 参与日常 on-call 轮值，负责线上故障的发现、定位与恢复
- 建设基于 **LLM Agent 的自动分析流程**，提升故障定位效率

**条带化（Set 化）治理**

- 开发元数据管理系统，管理多个条带的差异化配置与共性部分
- 推进服务 Set 化部署，降低故障爆炸半径

**变更流程与流水线建设**

- 建设 **SQL 变更流程**，覆盖审批、灰度、回滚全链路，兼顾稳定性与效率
- 搭建发布流水线，推进变更的标准化与自动化

**可观测性治理**

- 治理**监控、日志、Tracing** 三大可观测支柱，统一数据标准与接入规范
- 提升全链路观测能力，支撑故障定位与容量分析

### 腾讯音乐娱乐集团 - 基础平台部 - 业务运维 `2023/06-2024`

**统一接入层系统建设**

接入层链路信息分散于多个子系统，配置手工操作、效率低下。主导建设统一接入层管理系统：

- 与团队制定配置规范，对现网存量配置进行**采集入库、规范化和再下发**，推进组件标准化
- 基于 **Django + Vue.js** 开发，打通从域名到真实服务的全链路信息，将查询、变更、下发收敛至单一系统
- 接入审批流系统，兼顾配置变更的灵活与合规

### 南京邮电大学 - 青柚工作室 - 运维负责人 `2021/08-2023/05`

从零搭建团队运维体系，支撑校内多款服务（南邮小程序、邮你来办、南邮镜像站等）的稳定运行。

**基础设施标准化**

- 回收并重构全部服务器与数据库权限，基于 **CA 证书** 建设 SSH 登录认证体系
- 搭建私有 **Kubernetes** 集群，对存量服务容器化改造并迁移

**GitOps 体系建设**

- 以 **GitLab CI** 为中心，结合 **Ansible、Helm** 推进声明式配置管理
- 实现配置变更的**版本化、可审计、可回滚**

**全链路可观测平台**

- 围绕 **Prometheus + Grafana** 建设覆盖监控、日志、链路追踪的可观测平台
- **故障发现时间从数小时缩减至 5 分钟内**，团队故障频率从 **每月 10+ 次降至 2 次以下**

## 项目经历

### SRE-agent — 稳定性工程方法论探索 `2026`

- 研究稳定性、成本、效率三者平衡的理论框架
- 探索 LLM Agent 在故障定位与可观测数据分析中的应用

### OpenTelemetry SKB `Go` — Linux 内核网络可观测性 `2024`

基于 OpenTelemetry 协议对 Linux 内核 `struct skb` 进行链路追踪，实践 eBPF 与可观测性结合。

### Hermes 客户端 `TypeScript, React Native` — AI Agent 移动应用 `2026`

基于 Expo + AI SDK 的移动端 AI Agent 客户端，实践跨平台开发与 LLM 集成。

### 2D 足球仿真 — RoboCup 竞赛 `2021-2022`

担任 Apollo 机器人俱乐部 2D 仿真组组长，贡献 HFO Trainer（半场进攻训练器）等开源项目。

## 相关技能

- **编程语言**：Go（主力）、Python（熟练）、Bash（熟练）、C（底层开发）、React / Vue.js（前端）
- **SRE & 可观测**：on-call 与故障响应、监控/日志/Tracing 治理、Prometheus、Grafana、eBPF
- **分布式治理**：条带化/Set 化部署、元数据管理、故障爆炸半径控制
- **基础设施**：Kubernetes、Docker、Ansible、GitLab CI、Nginx
- **变更管理**：SQL 变更流程、发布流水线、审批流与灰度策略
- **操作系统**：Arch Linux 日常使用，维护个人 [AUR 包](https://aur.archlinux.org/packages?O=0&SeB=m&K=kawhicurry)，熟悉 systemd
