---
layout: home

hero:
  name: "FerrusGate"
  text: "The Iron Gate to Modern Identity"
  tagline: A modern identity gateway built with Rust, supporting OAuth2, OIDC, SAML, Passkey and other protocols
  image:
    src: /logo.svg
    alt: FerrusGate
  actions:
    - theme: brand
      text: Quick Start
      link: #quick-start
    - theme: alt
      text: View on GitHub
      link: https://github.com/AptS-1547/FerrusGate

features:
  - icon: 🔐
    title: Multi-Protocol Support
    details: Support for OAuth2, OIDC, SAML, Passkey (FIDO2) and other modern identity authentication protocols
  - icon: 🧩
    title: Pluggable Architecture
    details: Authentication methods, storage backends, and policy management are all replaceable to adapt to different business needs
  - icon: 🏢
    title: Multi-Tenant Support
    details: Enterprise-grade multi-tenant architecture with organization isolation and unified management
  - icon: ⚡
    title: High-Performance Rust Implementation
    details: Built with Rust for fast, secure, and thread-safe concurrent processing capabilities
  - icon: 🛠️
    title: Easy Deployment
    details: Support for Docker, Kubernetes and other deployment methods for quick integration into existing systems
  - icon: 🖥️
    title: Management Console
    details: Complete unified management interface for users, applications, tenants, policies and more

---

## Architecture Overview

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

## Quick Start

### 1. Clone Repository

```bash
git clone https://github.com/AptS-1547/FerrusGate.git
cd FerrusGate
```

### 2. Build & Run (Development Mode)

```bash
cargo run
```

Or use Docker (recommended for production):

```bash
docker-compose up -d
```

## Project Structure

| Directory  | Description                                    |
| ---------- | ---------------------------------------------- |
| `core/`    | Core identity protocol implementation          |
| `gate/`    | API gateway layer handling routing and logic   |
| `console/` | Web management console                         |
| `store/`   | Storage backend interfaces                     |
| `config/`  | Configuration and initialization               |
| `tests/`   | Test cases and integration tests               |

## Roadmap

- [ ] OAuth2 / OIDC gateway integration
- [ ] Initial Passkey support (WebAuthn)
- [ ] Multi-tenant database structure
- [ ] Management console UI (in progress)
- [ ] Policy engine (based on Rego / CEL)
- [ ] Plugin system (custom authentication flows)

## Etymology

> *Ferrus* (Latin: made of iron) symbolizes the strength and security of Rust,  
> *Gate* represents the unified identity entry point.

Ferrus Gate is the **identity guardian** of your system, making secure authentication no longer a burden.
