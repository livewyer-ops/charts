<!-- markdownlint-disable MD033 MD041 -->

![LiveWyer Banner](./.github/img/github-banner.png?raw=true)

<p align="center">
    <a href="https://livewyer.io"><img src="https://badgen.net/badge/Website/livewyer.io" alt="LiveWyer Website badge" /></a>
    <a href="https://github.com/orgs/livewyer-ops/packages?repo_name=charts"><img src="https://badgen.net/badge/GHCR/GitHub%20Container%20Registry" alt="LiveWyer Website badge" /></a>
    <a href="https://twitter.com/LiveWyerUK"><img src="https://badgen.net/badge/X/@LiveWyerUK" alt="Twitter badge" /></a>
    <a href="https://www.linkedin.com/company/livewyer"><img src="https://badgen.net/badge/LinkedIn/LiveWyer" alt="LinkedIn badge" /></a>
</p>

<h1 align="center">LiveWyer Helm Charts Repository</h1>

You can find our Helm charts on GitHub Container Registry (GHCR): <https://github.com/orgs/livewyer-ops/packages?repo_name=charts>

## Overview

LiveWyer Helm chart repository offers a diverse collection of Helm charts designed to streamline the deployment process and accelerate your Kubernetes journey.

> Refer to [CONTRIBUTING.md](./CONTRIBUTING.md) for guidance how to contribute to the project.

### CI/CD

We enabled `Tekton` [CI](https://tekton.dev) with [PaC](https://pipelinesascode.com) on this repo to execute the following pipelines:

* [Chart package](./.tekton/chart-package.yaml) that packages your Helm chart and pushed to `livewyer-ops` GHCR
* [Markdown lint](./.tekton/markdown-lint.yaml) that lints all markdown files in this repository

> A `markdown` [configuration file](./.markdownlint-cli2.yaml) is applied.

## Documentation

For detailed information on each Helm chart and configuration options, please refer to the respective Helm chart and `README` in the corresponding directory.

---

Copyright © 2024 LiveWyer, Licensed under the `MIT` License; you may not use this file except in compliance with the [License](LICENSE).

Unless required by applicable law or agreed to in writing, software distributed under the License is distributed on an "AS IS" BASIS,
WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
See the License for the specific language governing permissions and limitations under the [License](LICENSE).
