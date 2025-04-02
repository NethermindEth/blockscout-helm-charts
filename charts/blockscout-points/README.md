# blockscout-points

![Version: 0.2.2](https://img.shields.io/badge/Version-0.2.2-informational?style=flat-square) ![Type: application](https://img.shields.io/badge/Type-application-informational?style=flat-square) ![AppVersion: 0.1.0](https://img.shields.io/badge/AppVersion-0.1.0-informational?style=flat-square)

A Helm chart for Kubernetes

## Maintainers

| Name | Email | Url |
| ---- | ------ | --- |
| AntiD2ta |  |  |
| nmjustinchan |  |  |

## Values

| Key | Type | Default | Description |
|-----|------|---------|-------------|
| backend.affinity | object | `{}` |  |
| backend.config.auth.adminApiKey | string | `"key"` |  |
| backend.config.auth.jwtSecret | string | `"secret"` |  |
| backend.config.database.createDatabase | bool | `true` |  |
| backend.config.database.db | string | `"points"` |  |
| backend.config.database.existingSecret | string | `nil` |  |
| backend.config.database.existingSecretPasswordKey | string | `nil` |  |
| backend.config.database.existingSecretUsernameKey | string | `nil` |  |
| backend.config.database.host | string | `"postgres"` |  |
| backend.config.database.pass | string | `"password"` |  |
| backend.config.database.port | int | `5432` |  |
| backend.config.database.runMigrations | bool | `true` |  |
| backend.config.database.user | string | `"username"` |  |
| backend.config.grpc.enabled | bool | `false` |  |
| backend.config.grpc.port | int | `8051` |  |
| backend.env | list | `[]` |  |
| backend.envFromSecret | list | `[]` |  |
| backend.image.pullPolicy | string | `"IfNotPresent"` |  |
| backend.image.repository | string | `"ghcr.io/blockscout/points"` |  |
| backend.image.tag | string | `"latest"` |  |
| backend.imagePullSecrets | list | `[]` |  |
| backend.ingress.annotations | object | `{}` |  |
| backend.ingress.className | string | `""` |  |
| backend.ingress.enabled | bool | `false` |  |
| backend.ingress.hosts[0].host | string | `"chart-example.local"` |  |
| backend.ingress.hosts[0].paths[0].path | string | `"/"` |  |
| backend.ingress.hosts[0].paths[0].pathType | string | `"ImplementationSpecific"` |  |
| backend.ingress.tls | list | `[]` |  |
| backend.livenessProbe.httpGet.path | string | `"/health?service="` |  |
| backend.livenessProbe.httpGet.port | string | `"http"` |  |
| backend.metrics.enabled | bool | `false` |  |
| backend.metrics.port | int | `6060` |  |
| backend.metrics.prometheus.enabled | bool | `false` |  |
| backend.nodeSelector | object | `{}` |  |
| backend.readinessProbe.httpGet.path | string | `"/health?service="` |  |
| backend.readinessProbe.httpGet.port | string | `"http"` |  |
| backend.replicaCount | int | `1` |  |
| backend.resources.limits.cpu | string | `"500m"` |  |
| backend.resources.limits.memory | string | `"1Gi"` |  |
| backend.resources.requests.cpu | string | `"200m"` |  |
| backend.resources.requests.memory | string | `"256Mi"` |  |
| backend.service.port | int | `8050` |  |
| backend.service.type | string | `"ClusterIP"` |  |
| backend.tolerations | list | `[]` |  |
| backend.volumeMounts | list | `[]` |  |
| backend.volumes | list | `[]` |  |
| frontend.affinity | object | `{}` |  |
| frontend.config | string | `nil` |  |
| frontend.env | list | `[]` |  |
| frontend.envFromSecret | list | `[]` |  |
| frontend.image.pullPolicy | string | `"IfNotPresent"` |  |
| frontend.image.repository | string | `"ghcr.io/blockscout/blockscout-merits-website"` |  |
| frontend.image.tag | string | `"latest"` |  |
| frontend.imagePullSecrets | list | `[]` |  |
| frontend.ingress.annotations | object | `{}` |  |
| frontend.ingress.className | string | `""` |  |
| frontend.ingress.enabled | bool | `false` |  |
| frontend.ingress.hosts[0].host | string | `"chart-example.local"` |  |
| frontend.ingress.hosts[0].paths[0].path | string | `"/"` |  |
| frontend.ingress.hosts[0].paths[0].pathType | string | `"ImplementationSpecific"` |  |
| frontend.ingress.tls | list | `[]` |  |
| frontend.livenessProbe.httpGet.path | string | `"/"` |  |
| frontend.livenessProbe.httpGet.port | string | `"http"` |  |
| frontend.metrics.enabled | bool | `false` |  |
| frontend.metrics.port | int | `6060` |  |
| frontend.metrics.prometheus.enabled | bool | `false` |  |
| frontend.nodeSelector | object | `{}` |  |
| frontend.readinessProbe.httpGet.path | string | `"/"` |  |
| frontend.readinessProbe.httpGet.port | string | `"http"` |  |
| frontend.replicaCount | int | `1` |  |
| frontend.resources.limits.cpu | string | `"500m"` |  |
| frontend.resources.limits.memory | string | `"1Gi"` |  |
| frontend.resources.requests.cpu | string | `"200m"` |  |
| frontend.resources.requests.memory | string | `"256Mi"` |  |
| frontend.service.port | int | `3000` |  |
| frontend.service.type | string | `"ClusterIP"` |  |
| frontend.tolerations | list | `[]` |  |
| frontend.volumeMounts | list | `[]` |  |
| frontend.volumes | list | `[]` |  |
| fullnameOverride | string | `""` |  |
| nameOverride | string | `""` |  |
| podAnnotations | object | `{}` |  |
| podLabels | object | `{}` |  |
| podSecurityContext | object | `{}` |  |
| securityContext | object | `{}` |  |
| serviceAccount.annotations | object | `{}` |  |
| serviceAccount.automount | bool | `true` |  |
| serviceAccount.create | bool | `true` |  |
| serviceAccount.name | string | `""` |  |

----------------------------------------------
Autogenerated from chart metadata using [helm-docs v1.14.2](https://github.com/norwoodj/helm-docs/releases/v1.14.2)
