# Writing Helm charts

- [Writing Helm charts](#writing-helm-charts)
  - [Requirements](#requirements)
  - [Submitting a Helm chart](#submitting-a-helm-chart)

A Helm chart should be stored inside the `charts/` directory.

## Requirements

- Installed [helm-docs](https://github.com/norwoodj/helm-docs)

## Submitting a Helm chart

When submitting a Helm chart for a review to publish it, please consider the next:

- A Helm chart has an up to date `README.md` file generated with `helm-docs`
- All the values in `values.yaml` file are commented.
- A `Chart.yaml` file of the Helm chart has a `org.opencontainers.image.source: https://github.com/livewyer-ops/charts` annotation.

An example of annotation:

```yaml
apiVersion: v2
name: hello-world
description: A Helm chart for Kubernetes
annotations:
  org.opencontainers.image.source: https://github.com/livewyer-ops/charts
```
