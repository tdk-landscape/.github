<div align="center">

<picture>
  <source media="(prefers-color-scheme: dark)" srcset="https://capsule-render.vercel.app/api?type=waving&height=240&color=0:0A0A0E,45:34244F,100:EE924E&text=TDK&fontColor=F7EFE2&fontSize=72&fontAlignY=35&desc=Run%20100%20microservices%20on%20a%2016%20GB%20laptop.%20No%20Kubernetes.&descAlignY=58&descSize=18">
  <img src="https://capsule-render.vercel.app/api?type=waving&height=240&color=0:F7EFE2,45:D8D0FF,100:EE924E&text=TDK&fontColor=0A0A0E&fontSize=72&fontAlignY=35&desc=Run%20100%20microservices%20on%20a%2016%20GB%20laptop.%20No%20Kubernetes.&descAlignY=58&descSize=18" alt="TDK. Run 100 microservices on a 16 GB laptop. No Kubernetes." width="100%">
</picture>

<h3>Build the service, not the setup.</h3>

<p>
One CLI that scaffolds your services and runs the whole landscape locally (APIs, frontends, workers, Postgres, NATS, proxy) with hot reload and health checks. Built on <a href="https://tilt.dev">Tilt</a>.
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
