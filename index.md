---
layout: home

hero:
  name: "FerrusGate"
  text: "The Iron Gate to Modern Identity"
  tagline: 使用 Rust 编写的现代身份网关，支持 OAuth2、OIDC、SAML、Passkey 等协议
  image:
    src: /logo.svg
    alt: FerrusGate
  actions:
    - theme: brand
      text: 快速开始
      link: #快速开始
    - theme: alt
      text: 查看源码
      link: https://github.com/AptS-1547/FerrusGate

features:
  - icon: 🔐
    title: 多协议支持
    details: 支持 OAuth2、OIDC、SAML、Passkey（FIDO2）等现代身份认证协议
  - icon: 🧩
    title: 可插拔架构
    details: 认证方式、存储后端、策略管理均可替换，适应不同业务需求
  - icon: 🏢
    title: 多租户支持
    details: 企业级多租户架构，支持组织隔离和统一管理
  - icon: ⚡
    title: 高性能 Rust 实现
    details: 基于 Rust 构建，提供快速、安全、线程安全的并发处理能力
  - icon: 🛠️
    title: 易于部署
    details: 支持 Docker、Kubernetes 等多种部署方式，快速集成到现有系统
  - icon: 🖥️
    title: 管理后台
    details: 提供完整的用户、应用、租户、策略等统一管理界面
---

## 架构概览

```
┌────────────┐        ┌────────────┐
│   Client   │──────▶ │ Ferrus Gate│──────▶ Downstream Services
│  (Browser) │◀────── │   (SSO)    │
└────────────┘        └────────────┘
                           │
              ┌────────────▼────────────┐
              │    Identity Providers   │
              │ (OAuth, SAML, Passkey)  │
              └─────────────────────────┘
```

## 快速开始

### 1. 拉取项目

```bash
git clone https://github.com/AptS-1547/FerrusGate.git
cd FerrusGate
```

### 2. 编译 & 运行（开发模式）

```bash
cargo run
```

或者使用 Docker（推荐生产环境）：

```bash
docker-compose up -d
```

## 项目结构

| 目录         | 功能说明              |
| ---------- | ----------------- |
| `core/`    | 核心身份协议实现          |
| `gate/`    | API 接入层，处理路由与网关逻辑 |
| `console/` | Web 管理后台          |
| `store/`   | 存储后端接口            |
| `config/`  | 配置与初始化            |
| `tests/`   | 测试用例与集成测试         |

## 路线图

- [ ] OAuth2 / OIDC 网关接入
- [ ] 初步 Passkey 支持（WebAuthn）
- [ ] 多租户数据库结构
- [ ] 管理后台 UI（进行中）
- [ ] 策略引擎（基于 Rego / CEL）
- [ ] 插件系统（认证流程自定义）

## 命名由来

> *Ferrus*（拉丁语：铁质的）象征 Rust 的力量与安全性，  
> *Gate* 表示统一的身份入口。

Ferrus Gate 是你系统中的**身份守卫者**，让安全认证不再是负担。
