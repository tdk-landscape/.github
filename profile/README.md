
<div align="center">

<picture>
  <source media="(prefers-color-scheme: dark)" srcset="https://capsule-render.vercel.app/api?type=waving&height=240&color=0:0A0A0E,45:34244F,100:EE924E&text=TDK&fontColor=F7EFE2&fontSize=72&fontAlignY=35&desc=Local%20development%20on%20your%20laptop.%20Not%20Helm.&descAlignY=58&descSize=18">
  <img src="https://capsule-render.vercel.app/api?type=waving&height=240&color=0:F7EFE2,45:D8D0FF,100:EE924E&text=TDK&fontColor=0A0A0E&fontSize=72&fontAlignY=35&desc=Local%20development%20on%20your%20laptop.%20Not%20Helm.&descAlignY=58&descSize=18" alt="TDK. Local development on your laptop. Not Helm." width="100%">
</picture>

<h3>Build the service, not the setup.</h3>

<p>
TDK is a local development kit. It scaffolds services and runs a stack on your laptop with Docker and <a href="https://tilt.dev">Tilt</a> (hot reload, health, Traefik, Postgres).
</p>

<p>
It is not a Kubernetes packager. It does not replace Helm, Argo CD, Kustomize, or your production charts.
</p>

<p>
Use TDK when local bring-up of many services is painful and you do not want a cluster on the laptop. Skip TDK if <code>helm install</code> (or your existing compose/Tilt/Skaffold) already gives you a working local or shared-dev environment.
</p>

<p>
  <a href="https://github.com/tdk-landscape/tdk-cli-core"><img src="https://img.shields.io/github/stars/tdk-landscape/tdk-cli-core?style=for-the-badge&logo=github&label=Star%20tdk-cli-core&color=EE924E" alt="Star tdk-cli-core on GitHub"></a>
  <a href="https://www.npmjs.com/package/@tdk-landscape/tdk-cli-core"><img src="https://img.shields.io/npm/v/@tdk-landscape/tdk-cli-core?style=for-the-badge&logo=npm&color=34244F" alt="npm version"></a>
  <a href="https://github.com/tdk-landscape"><img src="https://img.shields.io/github/followers/tdk-landscape?style=for-the-badge&logo=github&label=Follow&color=D8D0FF&labelColor=0A0A0E" alt="Follow tdk-landscape on GitHub"></a>
  <a href="https://github.com/tdk-landscape/tdk-cli-core/blob/main/LICENSE"><img src="https://img.shields.io/github/license/tdk-landscape/tdk-cli-core?style=for-the-badge&color=0A0A0E" alt="MIT license"></a>
</p>

<p>
  <a href="https://tdk-landscape.github.io/tdk-website/"><strong>Website</strong></a>
  &nbsp;·&nbsp;
  <a href="https://github.com/tdk-landscape/awesome-tdk-framework"><strong>Awesome TDK</strong></a>
  &nbsp;·&nbsp;
  <a href="https://tdk-landscape.github.io/tdk-website/docs/quickstart/"><strong>Quickstart</strong></a>
  &nbsp;·&nbsp;
  <a href="https://tdk-landscape.github.io/tdk-website/docs/examples/"><strong>Examples</strong></a>
  &nbsp;·&nbsp;
  <a href="https://tdk-landscape.github.io/tdk-demo-animation/"><strong>Demo</strong></a>
</p>

</div>

---

## Try it in 30 seconds

```sh
npm install -g @tdk-landscape/tdk-cli-core
tdk project --yes                                      # set up the project
tdk resource orders-api --type backend --stack shop    # scaffold a service
tdk up shop                                            # run it with hot reload
```

⭐ **If TDK saves you from writing another `docker-compose.yml`, [star tdk-cli-core](https://github.com/tdk-landscape/tdk-cli-core).** Stars help other developers find it.

## Why TDK

| | docker-compose | Local Kubernetes | Plain Tilt | **TDK** |
|---|---|---|---|---|
| Scaffold a new service in one command | ❌ | ❌ | ❌ | ✅ |
| Hot reload on file change | ⚠️ | ⚠️ | ✅ | ✅ |
| Health-checked startup order | ⚠️ | ✅ | ⚠️ | ✅ |
| Proxy, Postgres, monitoring included | ❌ | ❌ | ❌ | ✅ |
| Needs a cluster | No | Yes | Optional | **No** |
| Start one stack of a large system | ⚠️ | ⚠️ | ⚠️ | ✅ `tdk up <stack>` |

<p><small>Fixture benchmark only: 100 generated services, all healthy in 112 s, 1.6 GiB total memory, 0 OOM kills on a 16 GB machine. This is a scale fixture, not the TDK product example. <a href="https://github.com/tdk-landscape/tdk-cli-core#fixture-bench-100-generated-services-on-one-laptop">See the benchmark →</a></small></p>

## Repositories

| Repo | What it is |
| --- | --- |
| ⭐ [**tdk-cli-core**](https://github.com/tdk-landscape/tdk-cli-core) | **The TDK CLI, Tilt engine, and service discovery. Start here.** |
| [tdk-example](https://github.com/tdk-landscape/tdk-example) | Smallest useful example: 2 stacks, 4 services, one `service.json` each |
| [tdk-saas-starter](https://github.com/tdk-landscape/tdk-saas-starter) | SaaS account dashboard with a working checkout button |
| [tdk-restaurant-example](https://github.com/tdk-landscape/tdk-restaurant-example) | Reservations, kitchen pacing, menu availability, floor control |
| [tdk-user-management](https://github.com/tdk-landscape/tdk-user-management) | Identity demo: admin, portal, and compliance stacks (SCIM, OIDC, audit) |
| [tdk-erp-system](https://github.com/tdk-landscape/tdk-erp-system) | Generated service-scale fixture used for laptop benchmarks |
| [tdk-docker-compose-example](https://github.com/tdk-landscape/tdk-docker-compose-example) | Run the TDK CLI from Docker Compose without installing it |
| [create-tdk-stack](https://github.com/tdk-landscape/create-tdk-stack) | create-t3-app–style landing page for the TDK stack |
| [tdk-cli-releases](https://github.com/tdk-landscape/tdk-cli-releases) | Prebuilt binaries for Linux and macOS |
| [tdk-website](https://github.com/tdk-landscape/tdk-website) | Docs, comparisons, and the public site |

## How it works

```text
Project                 one repo, one local landscape
  Stack                 a business slice: shop, identity, kitchen…  →  tdk up <stack>
    Resource            one API, frontend, worker, or database
      service.json      what it is and what it depends on
      .autogenerated/   Docker, Vite, env, Tilt, TypeScript wiring (generated)
```

Generated files are plain local plumbing you can read, not a hidden platform.

## Contributing

Issues labeled [`good first issue`](https://github.com/tdk-landscape/tdk-cli-core/labels/good%20first%20issue) are the best place to start. See [CONTRIBUTING.md](https://github.com/tdk-landscape/tdk-cli-core/blob/main/CONTRIBUTING.md). Built something with TDK? [Open an issue](https://github.com/tdk-landscape/tdk-cli-core/issues/new/choose) and we'll add it here.

<div align="center">

**Declare the landscape. Generate the boring parts.**

<a href="https://github.com/tdk-landscape/tdk-cli-core"><img src="https://img.shields.io/badge/Get_started-tdk--cli--core-EE924E?style=for-the-badge&logo=github" alt="Get started with tdk-cli-core"></a>

</div>
