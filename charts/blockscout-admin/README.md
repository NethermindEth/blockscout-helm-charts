# blockscout-admin

![Version: 1.3.2](https://img.shields.io/badge/Version-1.3.2-informational?style=flat-square) ![Type: application](https://img.shields.io/badge/Type-application-informational?style=flat-square) ![AppVersion: 1.1.0](https://img.shields.io/badge/AppVersion-1.1.0-informational?style=flat-square)

A Helm chart for Blockscout admin services - admin-rs, admin-ts, contracts-info, metadata, token-info-extractor

## Maintainers

| Name | Email | Url |
| ---- | ------ | --- |
| AntiD2ta |  |  |
| nmjustinchan |  |  |

## Values

| Key | Type | Default | Description |
|-----|------|---------|-------------|
| adminRs.config.databaseUrl | string | `""` |  |
| adminRs.envFromSecret | object | `{}` |  |
| adminRs.environment | object | `{}` |  |
| adminRs.image.pullPolicy | string | `"IfNotPresent"` |  |
| adminRs.image.repository | string | `"ghcr.io/blockscout/admin-rs"` |  |
| adminRs.image.tag | string | `""` |  |
| adminRs.ingress.annotations | object | `{}` |  |
| adminRs.ingress.className | string | `""` |  |
| adminRs.ingress.enabled | bool | `false` |  |
| adminRs.ingress.hosts[0].host | string | `"chart-example.local"` |  |
| adminRs.ingress.hosts[0].paths[0].path | string | `"/"` |  |
| adminRs.ingress.hosts[0].paths[0].pathType | string | `"ImplementationSpecific"` |  |
| adminRs.ingress.tls | list | `[]` |  |
| adminRs.replicaCount | int | `1` |  |
| adminRs.resources.limits.cpu | string | `"250m"` |  |
| adminRs.resources.limits.memory | string | `"512Mi"` |  |
| adminRs.resources.requests.cpu | string | `"100m"` |  |
| adminRs.resources.requests.memory | string | `"256Mi"` |  |
| adminRs.service.port | int | `80` |  |
| adminRs.service.targetPort | int | `8050` |  |
| adminRs.service.type | string | `"ClusterIP"` |  |
| adminTs.envFromSecret | object | `{}` |  |
| adminTs.environment | object | `{}` |  |
| adminTs.image.pullPolicy | string | `"IfNotPresent"` |  |
| adminTs.image.repository | string | `"ghcr.io/blockscout/admin-ts"` |  |
| adminTs.image.tag | string | `""` |  |
| adminTs.ingress.annotations | object | `{}` |  |
| adminTs.ingress.className | string | `""` |  |
| adminTs.ingress.enabled | bool | `false` |  |
| adminTs.ingress.hosts[0].host | string | `"chart-example.local"` |  |
| adminTs.ingress.hosts[0].paths[0].path | string | `"/"` |  |
| adminTs.ingress.hosts[0].paths[0].pathType | string | `"ImplementationSpecific"` |  |
| adminTs.ingress.tls | list | `[]` |  |
| adminTs.replicaCount | int | `1` |  |
| adminTs.resources.limits.cpu | string | `"500m"` |  |
| adminTs.resources.limits.memory | string | `"2Gi"` |  |
| adminTs.resources.requests.cpu | string | `"250m"` |  |
| adminTs.resources.requests.memory | string | `"256Mi"` |  |
| adminTs.service.port | int | `80` |  |
| adminTs.service.targetPort | int | `8080` |  |
| adminTs.service.type | string | `"ClusterIP"` |  |
| affinity | object | `{}` |  |
| config.network | list | `[]` |  |
| config.prometheus.enabled | bool | `false` |  |
| config.prometheus.path | string | `"/metrics"` |  |
| config.prometheus.port | int | `6060` |  |
| contractsInfo.config.apiKeys.adminjs | string | `"default-api-key"` |  |
| contractsInfo.config.apiKeys.extractor1 | string | `"default-extractor-key"` |  |
| contractsInfo.config.databaseUrl | string | `""` |  |
| contractsInfo.envFromSecret | list | `[]` |  |
| contractsInfo.environment | object | `{}` |  |
| contractsInfo.image.pullPolicy | string | `"IfNotPresent"` |  |
| contractsInfo.image.repository | string | `"ghcr.io/blockscout/contracts-info"` |  |
| contractsInfo.image.tag | string | `""` |  |
| contractsInfo.ingress.annotations | object | `{}` |  |
| contractsInfo.ingress.className | string | `""` |  |
| contractsInfo.ingress.enabled | bool | `false` |  |
| contractsInfo.ingress.hosts[0].host | string | `"chart-example.local"` |  |
| contractsInfo.ingress.hosts[0].paths[0].path | string | `"/"` |  |
| contractsInfo.ingress.hosts[0].paths[0].pathType | string | `"ImplementationSpecific"` |  |
| contractsInfo.ingress.tls | list | `[]` |  |
| contractsInfo.replicaCount | int | `1` |  |
| contractsInfo.resource.limits.cpu | string | `"100m"` |  |
| contractsInfo.resource.limits.memory | string | `"256Mi"` |  |
| contractsInfo.resource.requests.cpu | string | `"50m"` |  |
| contractsInfo.resource.requests.memory | string | `"96Mi"` |  |
| contractsInfo.service.port | int | `80` |  |
| contractsInfo.service.targetPort | int | `8050` |  |
| contractsInfo.service.type | string | `"ClusterIP"` |  |
| fullnameOverride | string | `""` |  |
| imagePullSecrets | list | `[]` |  |
| livenessProbe.params.initialDelaySeconds | int | `100` |  |
| livenessProbe.params.periodSeconds | int | `100` |  |
| livenessProbe.params.timeoutSeconds | int | `30` |  |
| metadata.envFromSecret | object | `{}` |  |
| metadata.environment | object | `{}` |  |
| metadata.image.pullPolicy | string | `"IfNotPresent"` |  |
| metadata.image.repository | string | `"ghcr.io/blockscout/metadata"` |  |
| metadata.image.tag | string | `""` |  |
| metadata.ingress.annotations | object | `{}` |  |
| metadata.ingress.className | string | `""` |  |
| metadata.ingress.enabled | bool | `false` |  |
| metadata.ingress.hosts[0].host | string | `"chart-example.local"` |  |
| metadata.ingress.hosts[0].paths[0].path | string | `"/"` |  |
| metadata.ingress.hosts[0].paths[0].pathType | string | `"ImplementationSpecific"` |  |
| metadata.ingress.tls | list | `[]` |  |
| metadata.replicaCount | int | `1` |  |
| metadata.resource.limits.cpu | string | `"100m"` |  |
| metadata.resource.limits.memory | string | `"256Mi"` |  |
| metadata.resource.requests.cpu | string | `"50m"` |  |
| metadata.resource.requests.memory | string | `"96Mi"` |  |
| metadata.service.port | int | `80` |  |
| metadata.service.targetPort | int | `8050` |  |
| metadata.service.type | string | `"ClusterIP"` |  |
| nameOverride | string | `""` |  |
| nodeSelector | object | `{}` |  |
| podSecurityContext.fsGroup | int | `1000` |  |
| poolsExtractor.enabled | bool | `false` |  |
| poolsExtractor.envFromSecret | object | `{}` |  |
| poolsExtractor.environment | object | `{}` |  |
| poolsExtractor.image.repository | string | `"ghcr.io/blockscout/pools-extractor"` |  |
| poolsExtractor.image.tag | string | `""` |  |
| poolsExtractor.resources.limits.cpu | string | `"250m"` |  |
| poolsExtractor.resources.limits.memory | string | `"256Mi"` |  |
| poolsExtractor.resources.requests.cpu | string | `"100m"` |  |
| poolsExtractor.resources.requests.memory | string | `"96Mi"` |  |
| poolsExtractor.schedule | string | `"0 0 * * *"` |  |
| readinessProbe.params.initialDelaySeconds | int | `60` |  |
| readinessProbe.params.periodSeconds | int | `10` |  |
| readinessProbe.params.timeoutSeconds | int | `60` |  |
| securityContext.capabilities.drop[0] | string | `"ALL"` |  |
| securityContext.readOnlyRootFilesystem | bool | `true` |  |
| securityContext.runAsNonRoot | bool | `true` |  |
| securityContext.runAsUser | int | `1000` |  |
| serviceAccount.annotations | object | `{}` |  |
| serviceAccount.create | bool | `true` |  |
| serviceAccount.name | string | `""` |  |
| tokenInfoExtractor.config.databaseUrl | string | `nil` |  |
| tokenInfoExtractor.enabled | bool | `false` |  |
| tokenInfoExtractor.envFromSecret | object | `{}` |  |
| tokenInfoExtractor.environment | object | `{}` |  |
| tokenInfoExtractor.image.repository | string | `"ghcr.io/blockscout/token-info-extractor"` |  |
| tokenInfoExtractor.image.tag | string | `""` |  |
| tokenInfoExtractor.resources.limits.cpu | string | `"250m"` |  |
| tokenInfoExtractor.resources.limits.memory | string | `"256Mi"` |  |
| tokenInfoExtractor.resources.requests.cpu | string | `"100m"` |  |
| tokenInfoExtractor.resources.requests.memory | string | `"96Mi"` |  |
| tokenInfoExtractor.schedule | string | `"0 20 * * *"` |  |
| tolerations | list | `[]` |  |

----------------------------------------------
Autogenerated from chart metadata using [helm-docs v1.14.2](https://github.com/norwoodj/helm-docs/releases/v1.14.2)
