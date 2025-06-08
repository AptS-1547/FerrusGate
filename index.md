# 🛡️ Ferrus Gate

> **The Iron Gate to Modern Identity**

Ferrus Gate 是一个使用 Rust 编写的现代身份网关，支持 OAuth2、OIDC、SAML、Passkey（FIDO2）等协议，为分布式系统提供统一的身份认证入口和账号管理平台。它致力于成为 **安全、高性能、可拓展** 的身份解决方案。

---

## ✨ 特性

- ✅ **支持多种协议**：OAuth2 / OIDC / SAML / Passkey（FIDO2）
- 🔐 **现代认证体验**：支持无密码登录、身份绑定、MFA
- 🧩 **可插拔架构**：认证方式、存储后端、策略管理均可替换
- 🏢 **多租户支持**：适配企业级使用场景
- 🖥️ **管理后台**：用户、应用、租户、策略等统一管理
- ⚙️ **高性能 Rust 实现**：快速、安全、线程安全的并发处理
- 🛠️ **易于部署与集成**：支持 Docker / Podman、Systemd、Kubernetes 部署

---

## 📐 架构概览

```

┌────────────┐        ┌────────────┐
│   Client   │──────▶│ Ferrus Gate│──────▶ Downstream Services
│  (Browser) │◀──────│   (SSO)    │
└────────────┘        └────┬──────┘
│
┌────────────▼────────────┐
│    Identity Providers   │
│ (OAuth, SAML, Passkey)  │
└─────────────────────────┘

````

---

## 🚀 快速开始

### 1. 拉取项目

```bash
git clone https://github.com/your-org/ferrus-gate.git
cd ferrus-gate
````

### 2. 编译 & 运行（开发模式）

```bash
cargo run
```

或者使用 Docker（推荐生产环境）：

```bash
docker-compose up -d
```

---

## ⚙️ 配置说明

项目使用 `config.yaml` 进行配置，支持热加载、环境变量覆盖。

示例配置片段：

```yaml
server:
  bind: 0.0.0.0
  port: 8080

auth:
  providers:
    - type: oidc
      name: Google
      client_id: xxx
      client_secret: xxx
```

---

## 📁 项目结构

| 目录         | 功能说明              |
| ---------- | ----------------- |
| `core/`    | 核心身份协议实现          |
| `gate/`    | API 接入层，处理路由与网关逻辑 |
| `console/` | Web 管理后台          |
| `store/`   | 存储后端接口            |
| `config/`  | 配置与初始化            |
| `tests/`   | 测试用例与集成测试         |

---

## 🧪 路线图

* [x] OAuth2 / OIDC 网关接入
* [x] 初步 Passkey 支持（WebAuthn）
* [x] 多租户数据库结构
* [ ] 管理后台 UI（进行中）
* [ ] 策略引擎（基于 Rego / CEL）
* [ ] 插件系统（认证流程自定义）

---

## 🛡️ 命名由来

> *Ferrus*（拉丁语：铁质的）象征 Rust 的力量与安全性，
> *Gate* 表示统一的身份入口。

Ferrus Gate 是你系统中的**身份守卫者**，让安全认证不再是负担。

---

## 📜 License

MIT © 2025 [AptS:1547](https://github.com/AptS-1547)

