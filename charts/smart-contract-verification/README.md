# smart-contract-verification

![Version: 0.1.1](https://img.shields.io/badge/Version-0.1.1-informational?style=flat-square) ![Type: application](https://img.shields.io/badge/Type-application-informational?style=flat-square) ![AppVersion: 1.0.0](https://img.shields.io/badge/AppVersion-1.0.0-informational?style=flat-square)

A Helm chart for Kubernetes

## Maintainers

| Name | Email | Url |
| ---- | ------ | --- |
| AntiD2ta |  |  |
| nmjustinchan |  |  |

## Values

| Key | Type | Default | Description |
|-----|------|---------|-------------|
| affinity | object | `{}` |  |
| ethBytecodeDb.enabled | bool | `false` |  |
| ethBytecodeDb.env | list | `[]` |  |
| ethBytecodeDb.envFromSecret | list | `[]` |  |
| ethBytecodeDb.image.pullPolicy | string | `"IfNotPresent"` |  |
| ethBytecodeDb.image.repository | string | `"ghcr.io/blockscout/eth-bytecode-db"` |  |
| ethBytecodeDb.image.tag | string | `"latest"` |  |
| ethBytecodeDb.ingress.annotations | object | `{}` |  |
| ethBytecodeDb.ingress.className | string | `""` |  |
| ethBytecodeDb.ingress.enabled | bool | `false` |  |
| ethBytecodeDb.ingress.hostname | string | `"eth-bytecode-db.local"` |  |
| ethBytecodeDb.ingress.tls.enabled | bool | `false` |  |
| ethBytecodeDb.livenessProbe.httpGet.path | string | `"/health?service="` |  |
| ethBytecodeDb.livenessProbe.httpGet.port | string | `"http"` |  |
| ethBytecodeDb.livenessProbe.initialDelaySeconds | int | `100` |  |
| ethBytecodeDb.livenessProbe.periodSeconds | int | `100` |  |
| ethBytecodeDb.livenessProbe.timeoutSeconds | int | `30` |  |
| ethBytecodeDb.podAnnotations | object | `{}` |  |
| ethBytecodeDb.podLabels | object | `{}` |  |
| ethBytecodeDb.podSecurityContext | object | `{}` |  |
| ethBytecodeDb.readinessProbe.httpGet.path | string | `"/health?service="` |  |
| ethBytecodeDb.readinessProbe.httpGet.port | string | `"http"` |  |
| ethBytecodeDb.readinessProbe.initialDelaySeconds | int | `100` |  |
| ethBytecodeDb.readinessProbe.periodSeconds | int | `100` |  |
| ethBytecodeDb.readinessProbe.timeoutSeconds | int | `30` |  |
| ethBytecodeDb.replicaCount | int | `1` |  |
| ethBytecodeDb.resources.limits.cpu | string | `"500m"` |  |
| ethBytecodeDb.resources.limits.memory | string | `"1Gi"` |  |
| ethBytecodeDb.resources.requests.cpu | string | `"250m"` |  |
| ethBytecodeDb.resources.requests.memory | string | `"512Mi"` |  |
| ethBytecodeDb.securityContext | object | `{}` |  |
| ethBytecodeDb.service.port | int | `8050` |  |
| ethBytecodeDb.service.type | string | `"ClusterIP"` |  |
| ethBytecodeDb.volumeMounts | list | `[]` |  |
| ethBytecodeDb.volumes | list | `[]` |  |
| fullnameOverride | string | `""` |  |
| imagePullSecrets | list | `[]` |  |
| metrics.enabled | bool | `false` |  |
| metrics.port | int | `6060` |  |
| metrics.prometheus.enabled | bool | `false` |  |
| nameOverride | string | `""` |  |
| nodeSelector | object | `{}` |  |
| serviceAccount.annotations | object | `{}` |  |
| serviceAccount.automount | bool | `true` |  |
| serviceAccount.create | bool | `true` |  |
| serviceAccount.name | string | `""` |  |
| sigProvider.env | list | `[]` |  |
| sigProvider.image.pullPolicy | string | `"IfNotPresent"` |  |
| sigProvider.image.repository | string | `"ghcr.io/blockscout/sig-provider"` |  |
| sigProvider.image.tag | string | `"latest"` |  |
| sigProvider.ingress.annotations | object | `{}` |  |
| sigProvider.ingress.className | string | `""` |  |
| sigProvider.ingress.enabled | bool | `false` |  |
| sigProvider.ingress.hostname | string | `"sig-provider.local"` |  |
| sigProvider.ingress.tls.enabled | bool | `false` |  |
| sigProvider.livenessProbe.httpGet.path | string | `"/health?service="` |  |
| sigProvider.livenessProbe.httpGet.port | string | `"http"` |  |
| sigProvider.podAnnotations | object | `{}` |  |
| sigProvider.podLabels | object | `{}` |  |
| sigProvider.podSecurityContext | object | `{}` |  |
| sigProvider.readinessProbe.httpGet.path | string | `"/health?service="` |  |
| sigProvider.readinessProbe.httpGet.port | string | `"http"` |  |
| sigProvider.replicaCount | int | `2` |  |
| sigProvider.resources.limits.cpu | string | `"250m"` |  |
| sigProvider.resources.limits.memory | string | `"256Mi"` |  |
| sigProvider.resources.requests.cpu | string | `"100m"` |  |
| sigProvider.resources.requests.memory | string | `"128Mi"` |  |
| sigProvider.securityContext | object | `{}` |  |
| sigProvider.service.port | int | `8043` |  |
| sigProvider.service.type | string | `"ClusterIP"` |  |
| sigProvider.volumeMounts | list | `[]` |  |
| sigProvider.volumes | list | `[]` |  |
| smartContractVerifier.env | list | `[]` |  |
| smartContractVerifier.envFromSecret | list | `[]` |  |
| smartContractVerifier.grpc.enabled | bool | `true` |  |
| smartContractVerifier.grpc.ingress.annotations | object | `{}` |  |
| smartContractVerifier.grpc.ingress.className | string | `""` |  |
| smartContractVerifier.grpc.ingress.enabled | bool | `false` |  |
| smartContractVerifier.grpc.ingress.hostname | string | `"grpc-smart-contract-verifier.local"` |  |
| smartContractVerifier.grpc.ingress.tls.enabled | bool | `false` |  |
| smartContractVerifier.grpc.port | int | `8051` |  |
| smartContractVerifier.image.pullPolicy | string | `"IfNotPresent"` |  |
| smartContractVerifier.image.repository | string | `"ghcr.io/blockscout/smart-contract-verifier"` |  |
| smartContractVerifier.image.tag | string | `"latest"` |  |
| smartContractVerifier.ingress.annotations | object | `{}` |  |
| smartContractVerifier.ingress.className | string | `""` |  |
| smartContractVerifier.ingress.enabled | bool | `false` |  |
| smartContractVerifier.ingress.hostname | string | `"smart-contract-verifier.local"` |  |
| smartContractVerifier.ingress.tls.enabled | bool | `false` |  |
| smartContractVerifier.livenessProbe.httpGet.path | string | `"/health?service="` |  |
| smartContractVerifier.livenessProbe.httpGet.port | string | `"http"` |  |
| smartContractVerifier.podAnnotations | object | `{}` |  |
| smartContractVerifier.podLabels | object | `{}` |  |
| smartContractVerifier.podSecurityContext | object | `{}` |  |
| smartContractVerifier.readinessProbe.httpGet.path | string | `"/health?service="` |  |
| smartContractVerifier.readinessProbe.httpGet.port | string | `"http"` |  |
| smartContractVerifier.replicaCount | int | `2` |  |
| smartContractVerifier.resources.limits.cpu | string | `"1"` |  |
| smartContractVerifier.resources.limits.memory | string | `"8Gi"` |  |
| smartContractVerifier.resources.requests.cpu | string | `"250m"` |  |
| smartContractVerifier.resources.requests.memory | string | `"1Gi"` |  |
| smartContractVerifier.securityContext | object | `{}` |  |
| smartContractVerifier.service.port | int | `8050` |  |
| smartContractVerifier.service.type | string | `"ClusterIP"` |  |
| smartContractVerifier.volumeMounts | list | `[]` |  |
| smartContractVerifier.volumes | list | `[]` |  |
| tolerations | list | `[]` |  |

----------------------------------------------
Autogenerated from chart metadata using [helm-docs v1.5.0](https://github.com/norwoodj/helm-docs/releases/v1.5.0)
