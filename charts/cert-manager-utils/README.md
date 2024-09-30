# cert-manager-utils

![Version: 1.0.0](https://img.shields.io/badge/Version-1.0.0-informational?style=flat-square) ![Type: application](https://img.shields.io/badge/Type-application-informational?style=flat-square) ![AppVersion: 1.0.0](https://img.shields.io/badge/AppVersion-1.0.0-informational?style=flat-square)

All Kubernetes Clusters eventually require `TLS`, `Certificates`, `Issuers`, etc.
`cert-manager-utils` helm chart enables you to deploy any type of `Issuers` and `Certificates` in your cluster,
in any quantity, making it easy to manage all your `cert-manager` resources from one place.

## Values

| Key | Type | Default | Description |
|-----|------|---------|-------------|
| certificates | object | `{"apiVersion":"cert-manager.io/v1","commonAnnotations":{},"commonLabels":{},"objects":{"wildcard-tls-production":{"commonName":"*.production.example.com","dnsNames":["*.production.example.com"],"issuerRef":{"kind":"ClusterIssuer","name":"letsencrypt-production"}}}}` | This section manages Certificates |
| certificates.apiVersion | string | `"cert-manager.io/v1"` | Сertificate object version |
| certificates.commonAnnotations | object | see [values](values.yaml) | Annotations to add to all Сertificates |
| certificates.commonLabels | object | see [values](values.yaml) | Labels to add to all Сertificates |
| certificates.objects | object | `{"wildcard-tls-production":{"commonName":"*.production.example.com","dnsNames":["*.production.example.com"],"issuerRef":{"kind":"ClusterIssuer","name":"letsencrypt-production"}}}` | Define number and configuration of your certificates.  Our syntax follows the API Reference, but make sure to review templates/Certificate.yaml template. |
| issuers | object | `{"apiVersion":"cert-manager.io/v1","commonAnnotations":{},"commonLabels":{},"objects":{"letsencrypt-production":{"kind":"ClusterIssuer","spec":{"acme":{"email":"my@email.com","privateKeySecretRef":{"name":"letsencrypt-production"},"server":"https://acme-v02.api.letsencrypt.org/directory","solvers":[{"dns01":{"cloudDNS":{"project":"my-clouddns-project","serviceAccountSecretRef":{"key":"key.json","name":"clouddns-dns01-cert-solver"}}}}]}}},"letsencrypt-staging":{"kind":"ClusterIssuer","spec":{"acme":{"email":"my@email.com","privateKeySecretRef":{"name":"letsencrypt-staging"},"server":"https://acme-staging-v02.api.letsencrypt.org/directory","solvers":[{"http01":{"ingress":{"class":"nginx"}}}]}}}}}` | This section manages Issuers and ClusterIssuers |
| issuers.apiVersion | string | `"cert-manager.io/v1"` | Issuer(ClusterIssuer) object version |
| issuers.commonAnnotations | object | see [values](values.yaml) | Annotations to add to all Issuers(ClusterIssuers) |
| issuers.commonLabels | object | see [values](values.yaml) | Labels to add to all Issuers(ClusterIssuers) |
| issuers.objects | object | `{"letsencrypt-production":{"kind":"ClusterIssuer","spec":{"acme":{"email":"my@email.com","privateKeySecretRef":{"name":"letsencrypt-production"},"server":"https://acme-v02.api.letsencrypt.org/directory","solvers":[{"dns01":{"cloudDNS":{"project":"my-clouddns-project","serviceAccountSecretRef":{"key":"key.json","name":"clouddns-dns01-cert-solver"}}}}]}}},"letsencrypt-staging":{"kind":"ClusterIssuer","spec":{"acme":{"email":"my@email.com","privateKeySecretRef":{"name":"letsencrypt-staging"},"server":"https://acme-staging-v02.api.letsencrypt.org/directory","solvers":[{"http01":{"ingress":{"class":"nginx"}}}]}}}}` | Define number and configuration of your Issuers. templates/Issuer.yaml template uses toYaml function for "spec" section, so make sure to follow API Reference |
| nameOverride | string | `""` | Partially override Chart name |
