# Company Standard Helm Library: Keycloak Config CLI

This chart provides a reusable, standardized mechanism for application repositories to publish and synchronize their Keycloak clients, roles, and scopes declaratively using [keycloak-config-cli](https://github.com/adorsys/keycloak-config-cli).

### How Application Repositories Use This Chart

Application charts can include this chart as a subchart dependency in `Chart.yaml`:

```yaml
dependencies:
  - name: keycloak-config-cli
    version: "1.0.0"
    repository: "file://../../company-helm-charts/keycloak-config-cli"
```

Or by mounting their `keycloak/*.yaml` files into a ConfigMap and executing the Job.