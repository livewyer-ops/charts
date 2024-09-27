# cluster-issuers

![Version: 1.0.3](https://img.shields.io/badge/Version-1.0.3-informational?style=flat-square) ![Type: application](https://img.shields.io/badge/Type-application-informational?style=flat-square) ![AppVersion: 1.0.0](https://img.shields.io/badge/AppVersion-1.0.0-informational?style=flat-square)

A Helm chart for Kubernetes Cert-manager ClusterIssuers

## Values

| Key | Type | Default | Description |
|-----|------|---------|-------------|
| clusterIssuer.production.cloudDNS.key | string | `"key.json"` |  |
| clusterIssuer.production.cloudDNS.projectName | string | `"mgmt-wyer-live"` |  |
| clusterIssuer.production.cloudDNS.secretName | string | `"clouddns-dns01-cert-solver"` |  |
| vaultSecrets.dns01solverSAJSON.name | string | `"clouddns-dns01-cert-solver"` |  |
| vaultSecrets.dns01solverSAJSON.path | string | `"projects/lwde/shared/clouddns-dns01-cert-solver"` |  |
