
<div align="center">

<picture>
  <source media="(prefers-color-scheme: dark)" srcset="https://capsule-render.vercel.app/api?type=waving&height=280&color=0:0A0A0E,45:34244F,100:EE924E&text=TDK%20Landscape&fontColor=F7EFE2&fontSize=64&fontAlignY=35&desc=Kubernetes-free%20local%20development%20for%20distributed%20systems&descAlignY=55&descSize=18&animation=twinkling">
  <img src="https://capsule-render.vercel.app/api?type=waving&height=280&color=0:F7EFE2,45:D8D0FF,100:EE924E&text=TDK%20Landscape&fontColor=0A0A0E&fontSize=64&fontAlignY=35&desc=Kubernetes-free%20local%20development%20for%20distributed%20systems&descAlignY=55&descSize=18&animation=twinkling" alt="TDK Landscape. Kubernetes-free local development for distributed systems." width="100%">
</picture>

<h3>Build the service, not the setup.</h3>

<p>
TDK gives teams one manifest-driven workflow for starting the databases, queues, APIs, workers, and frontends that make up a real local stack.
</p>

<p>
  <a href="https://tdk-landscape.github.io/tdk-website/"><strong>Explore TDK CLI</strong></a>
  &nbsp;|&nbsp;
  <a href="https://tdk-landscape.github.io/tdk-website/docs/"><strong>Read the docs</strong></a>
  &nbsp;|&nbsp;
  <a href="https://tdk-landscape.github.io/tdk-website/docs/examples/"><strong>Run an example</strong></a>
</p>

<p>
  <img src="https://img.shields.io/badge/Bun-1.2+-black?logo=bun" alt="Bun">
  <img src="https://img.shields.io/badge/Tilt-latest-blue?logo=tilt" alt="Tilt">
  <img src="https://img.shields.io/badge/Docker-Latest-blue?logo=docker" alt="Docker">
  <img src="https://img.shields.io/badge/TypeScript-5.0+-blue?logo=typescript" alt="TypeScript">
  <img src="https://img.shields.io/badge/Hono-4.0+-orange?logo=hono" alt="Hono">
</p>

</div>

---

## Why TDK exists

Modern services rarely fail because one API is hard to run. They fail locally because every useful workflow needs a cluster of neighbors: a frontend, an API, a worker, a database, a queue, a registry, secrets, generated clients, and health checks.

TDK keeps that topology explicit. Each resource declares what it is in `service.json`; the CLI discovers the landscape, generates the repetitive wiring, and lets developers run the whole system or one stack at a time.

```sh
tdk init
tdk up
tdk status
```

## The Ecosystem

The TDK Landscape isn't just one tool—it's a complete ecosystem for modern microservice development, from CLI to enterprise examples to beautiful documentation.

## Core Infrastructure

### CLI & Platform
<table>
  <tr>
    <td width="50%">
      <h3><a href="https://github.com/tdk-landscape/tdk-cli">tdk-cli</a></h3>
      <p>The command surface for manifest discovery, local generation, stack startup, and developer status.</p>
    </td>
    <td width="50%">
      <h3><a href="https://github.com/tdk-landscape/platform">platform</a></h3>
      <p>Shared packages for eventing, server primitives, Prisma tooling, secrets, and logging.</p>
    </td>
  </tr>
</table>

## Example Projects

### Production-Grade Demonstrations
<table>
  <tr>
    <td width="50%">
      <h3><a href="https://github.com/tdk-landscape/tdk-erp-system">tdk-erp-system</a></h3>
      <p>Enterprise ERP with 100 microservices across 7 domains: Finance, HR, Inventory, Sales, Manufacturing, Supply Chain, and Analytics.</p>
    </td>
    <td width="50%">
      <h3><a href="https://github.com/tdk-landscape/beauty-crm">beauty-crm</a></h3>
      <p>Real-world CRM system for salon management with appointments, inventory, and multi-tenant architecture.</p>
    </td>
  </tr>
  <tr>
    <td width="50%">
      <h3><a href="https://github.com/tdk-landscape/tdk-user-management">tdk-user-management</a></h3>
      <p>Enterprise identity demo with admin, portal, and compliance stacks for SCIM, OIDC, and audit flows.</p>
    </td>
    <td width="50%">
      <h3><a href="https://github.com/tdk-landscape/tdk-restaurant-example">tdk-restaurant-example</a></h3>
      <p>Restaurant operations demo for reservations, kitchen pacing, menu availability, and floor control.</p>
    </td>
  </tr>
</table>

### Learning & Starter Projects
<table>
  <tr>
    <td width="50%">
      <h3><a href="https://github.com/tdk-landscape/tdk-example">tdk-example</a></h3>
      <p>The smallest useful PSR reference: identity and appointment stacks with Hono, Vite, Bun, and Tilt.</p>
    </td>
    <td width="50%">
      <h3><a href="https://github.com/tdk-landscape/create-tdk-stack">create-tdk-stack</a></h3>
      <p>Polished landing page and starter surface for the TDK CLI—like create-t3-app for microservice systems.</p>
    </td>
  </tr>
  <tr>
    <td width="50%">
      <h3><a href="https://github.com/tdk-landscape/tdk-docker-compose-example">tdk-docker-compose-example</a></h3>
      <p>Docker Compose reference implementation for teams preferring container orchestration over Tilt.</p>
    </td>
    <td width="50%">
      <h3><a href="https://github.com/tdk-landscape/identity">identity</a></h3>
      <p>Identity management microservice with authentication, authorization, and user profile capabilities.</p>
    </td>
  </tr>
</table>

## Documentation & Tools

<table>
  <tr>
    <td width="50%">
      <h3><a href="https://github.com/tdk-landscape/tdk-website">tdk-website</a></h3>
      <p>The public site: docs, comparison pages, fit checks, examples, and launch content.</p>
    </td>
    <td width="50%">
      <h3><a href="https://github.com/tdk-landscape/tdk-demo-animation">tdk-demo-animation</a></h3>
      <p>Interactive animations and visual demonstrations of TDK capabilities and workflows.</p>
    </td>
  </tr>
  <tr>
    <td width="50%">
      <h3><a href="https://github.com/tdk-landscape/tdk-github-pages">tdk-github-pages</a></h3>
      <p>GitHub Pages deployment setup and workflow configuration for TDK ecosystem projects.</p>
    </td>
    <td width="50%">
      <h3><a href="https://github.com/tdk-landscape/tdk-cli-releases-public">tdk-cli-releases-public</a></h3>
      <p>Public release artifacts and version management for TDK CLI distributions.</p>
    </td>
  </tr>
</table>

## The PSR model

```text
Project
  Stack
    Resource
      service.json
      src/
      .autogenerated/
```

| Layer | What it means | How it helps |
| --- | --- | --- |
| Project | The cloneable repo that owns the local landscape | One command can start the system |
| Stack | A business slice such as identity, guest, kitchen, or compliance | Teams can boot only what they need |
| Resource | One API, frontend, worker, database, queue, or infra unit | Each service keeps its own runtime contract |

## Quick Start

### Choose Your Starting Point

| If you want | Clone this |
| --- | --- |
| The smallest PSR walkthrough | [`tdk-example`](https://github.com/tdk-landscape/tdk-example) |
| Enterprise ERP with 100 services | [`tdk-erp-system`](https://github.com/tdk-landscape/tdk-erp-system) |
| Real-world CRM system | [`beauty-crm`](https://github.com/tdk-landscape/beauty-crm) |
| Enterprise identity and governance | [`tdk-user-management`](https://github.com/tdk-landscape/tdk-user-management) |
| Restaurant operations and service pacing | [`tdk-restaurant-example`](https://github.com/tdk-landscape/tdk-restaurant-example) |
| Beautiful starter landing page | [`create-tdk-stack`](https://github.com/tdk-landscape/create-tdk-stack) |

```sh
git clone https://github.com/tdk-landscape/tdk-restaurant-example.git
cd tdk-restaurant-example
tdk up
```

## What TDK generates

TDK is intentionally inspectable. Generated files are local development plumbing, not a hidden platform.

```text
service.json       -> resource intent
tdk up             -> discovery, validation, generation
.autogenerated/    -> Docker, Vite, env, Tilt, TypeScript wiring
tdk status         -> running topology and health
```

## Tech Stack

The TDK ecosystem is built on modern, developer-friendly technologies:

| Layer | Technology | Purpose |
|-------|------------|---------|
| **Runtime** | Bun 1.2+ | Fast JavaScript runtime with built-in tooling |
| **Framework** | Hono 4+ | Lightweight, type-safe web framework |
| **Build** | Vite 5+ | Fast build tool with HMR support |
| **Database** | Prisma 7+ | Type-safe ORM with PostgreSQL |
| **Orchestration** | Tilt | Local development orchestration |
| **Containerization** | Docker | Container runtime and images |
| **Messaging** | NATS JetStream | Event-driven architecture |
| **Secrets** | Infisical | Secure secrets management |
| **Testing** | Vitest + Playwright | Fast unit and E2E testing |
| **Type Safety** | TypeScript 5+ | End-to-end type safety |

## Key Features

### ✅ Manifest-Driven Development
- Single `service.json` file per resource
- Automatic discovery and validation
- No hand-wiring of Docker, Vite, or Tilt configs

### ✅ Stack-Based Organization
- Group related services by business domain
- Start only what you need (`tdk up finance`)
- Clear team boundaries and ownership

### ✅ Zero-Configuration Local Stack
- Automatic port allocation
- Health check generation
- Environment variable management
- Hot reload on file changes

### ✅ Production-Ready Patterns
- Multi-tenant architecture support
- Event-driven messaging
- Secret management integration
- Comprehensive testing setup

## Community & Contributing

We welcome contributions to the TDK ecosystem! Whether you're fixing a bug, adding a feature, or improving documentation, we'd love your help.

### Ways to Contribute
- 🐛 Report bugs and request features
- 📝 Improve documentation
- 💻 Submit pull requests
- 🎨 Share your TDK-based projects
- 💬 Participate in discussions

### Getting Started
1. Pick a repository that interests you
2. Read the contributing guidelines
3. Fork and create a feature branch
4. Make your changes with tests
5. Submit a pull request

## Useful links

- [Website](https://tdk-landscape.github.io/tdk-website/)
- [Quickstart](https://tdk-landscape.github.io/tdk-website/docs/quickstart/)
- [Examples](https://tdk-landscape.github.io/tdk-website/docs/examples/)
- [No Vendor Lock-in](https://tdk-landscape.github.io/tdk-website/no-lock-in/)
- [GitHub organization](https://github.com/tdk-landscape)

## Stats & Activity

<div align="center">

![GitHub Stars](https://img.shields.io/github/stars/tdk-landscape?style=social)
![GitHub Forks](https://img.shields.io/github/forks/tdk-landscape?style=social)
![GitHub Issues](https://img.shields.io/github/issues/tdk-landscape)
![GitHub License](https://img.shields.io/github/license/tdk-landscape)

</div>

## Ecosystem Overview

| Category | Repositories | Description |
|----------|-------------|-------------|
| **Core** | 2 | CLI and platform packages |
| **Examples** | 6 | Production demos and learning projects |
| **Documentation** | 4 | Websites, animations, and deployment tools |
| **Total** | 12+ | Complete microservice development ecosystem |

---

<div align="center">

## 🚀 Ready to transform your local development?

**Declare the landscape. Generate the boring parts. Keep the stack close enough to understand.**

<div align="center">

<a href="https://github.com/tdk-landscape/tdk-cli"><img src="https://img.shields.io/badge/Get_Started-tdk_cli-green?style=for-the-badge" alt="Get Started"></a>

</div>

<div align="center">

Made with 💚 by the TDK Landscape community

</div>

</div>


