# Coding Standards

- [Coding Standards](#coding-standards)
  - [Requirements](#requirements)
  - [Submitting a Helm chart](#submitting-a-helm-chart)

A Helm chart should be stored inside a subfolder in the `charts/` directory.

> `hello-world` example could be found [here](https://github.com/livewyer-ops/charts/tree/main/charts/hello-world).

## Requirements

- [helm-docs](https://github.com/norwoodj/helm-docs)

## Submitting a Helm chart

Every Helm chart in the repo should follow [`Helm's` best practices](https://helm.sh/docs/chart_best_practices).

In addition to `Helm's` standards, please make sure to follow the repository's requirements:

- All the values in a `values.yaml` file are commented as it's shown [here](https://github.com/livewyer-ops/charts/blob/main/charts/hello-world/values.yaml).
- A `Chart.yaml` file of the Helm chart has the same template as [here](https://github.com/livewyer-ops/charts/blob/main/charts/hello-world/Chart.yaml).
- A Helm chart has an up to date [README.md](https://github.com/livewyer-ops/charts/blob/main/charts/hello-world/README.md) file generated with `helm-docs` command
