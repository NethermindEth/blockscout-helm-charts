# rpc-node

![Version: 0.4.2](https://img.shields.io/badge/Version-0.4.2-informational?style=flat-square) ![Type: application](https://img.shields.io/badge/Type-application-informational?style=flat-square) ![AppVersion: 0.1.0](https://img.shields.io/badge/AppVersion-0.1.0-informational?style=flat-square)

A Helm chart for RPC node and consensus

## Values

| Key | Type | Default | Description |
|-----|------|---------|-------------|
| affinity | object | `{}` |  |
| config.jwtsecret.enabled | bool | `false` |  |
| config.jwtsecret.value | string | `""` |  |
| consensus.args | list | `[]` |  |
| consensus.command | string | `"lighthouse bn"` |  |
| consensus.configFiles.enabled | bool | `false` |  |
| consensus.enabled | bool | `false` |  |
| consensus.env | list | `[]` |  |
| consensus.envFromSecret | list | `[]` |  |
| consensus.extraArgs | list | `[]` |  |
| consensus.image.pullPolicy | string | `"IfNotPresent"` |  |
| consensus.image.repository | string | `"sigp/lighthouse"` |  |
| consensus.image.tag | string | `"latest"` |  |
| consensus.ingress.annotations | object | `{}` |  |
| consensus.ingress.className | string | `""` |  |
| consensus.ingress.enabled | bool | `false` |  |
| consensus.ingress.hosts[0].host | string | `"chart-example.local"` |  |
| consensus.ingress.hosts[0].paths[0].path | string | `"/"` |  |
| consensus.ingress.hosts[0].paths[0].pathType | string | `"ImplementationSpecific"` |  |
| consensus.ingress.hosts[0].port | int | `8545` |  |
| consensus.ingress.tls | list | `[]` |  |
| consensus.livenessProbe.httpGet.path | string | `"/"` |  |
| consensus.livenessProbe.httpGet.port | string | `"rpc"` |  |
| consensus.livenessProbe.initialDelaySeconds | int | `60` |  |
| consensus.livenessProbe.periodSeconds | int | `30` |  |
| consensus.livenessProbe.timeoutSeconds | int | `15` |  |
| consensus.persistence.accessModes[0] | string | `"ReadWriteOnce"` |  |
| consensus.persistence.annotations | object | `{}` |  |
| consensus.persistence.enabled | bool | `false` |  |
| consensus.persistence.mountPath | string | `"/data"` |  |
| consensus.persistence.size | string | `"10Gi"` |  |
| consensus.podAnnotations | object | `{}` |  |
| consensus.podLabels | object | `{}` |  |
| consensus.podSecurityContext | object | `{}` |  |
| consensus.readinessProbe.httpGet.path | string | `"/"` |  |
| consensus.readinessProbe.httpGet.port | string | `"rpc"` |  |
| consensus.readinessProbe.initialDelaySeconds | int | `30` |  |
| consensus.readinessProbe.periodSeconds | int | `30` |  |
| consensus.readinessProbe.timeoutSeconds | int | `15` |  |
| consensus.resources | object | `{}` |  |
| consensus.securityContext | object | `{}` |  |
| consensus.service.cluster.ports[0].name | string | `"rpc"` |  |
| consensus.service.cluster.ports[0].port | int | `5052` |  |
| consensus.service.cluster.ports[0].protocol | string | `"TCP"` |  |
| consensus.service.node.ports[0].name | string | `"p2p-tcp"` |  |
| consensus.service.node.ports[0].port | int | `9909` |  |
| consensus.service.node.ports[0].protocol | string | `"TCP"` |  |
| consensus.service.node.ports[1].name | string | `"p2p-udp"` |  |
| consensus.service.node.ports[1].port | int | `9909` |  |
| consensus.service.node.ports[1].protocol | string | `"UDP"` |  |
| consensus.volumeMounts | list | `[]` |  |
| consensus.volumes | list | `[]` |  |
| execution.args | list | `[]` |  |
| execution.command | string | `nil` |  |
| execution.configFiles.enabled | bool | `false` |  |
| execution.env | list | `[]` |  |
| execution.envFromSecret | list | `[]` |  |
| execution.extraArgs | list | `[]` |  |
| execution.image.pullPolicy | string | `"IfNotPresent"` |  |
| execution.image.repository | string | `"ethereum/client-go"` |  |
| execution.image.tag | string | `"latest"` |  |
| execution.ingress.annotations | object | `{}` |  |
| execution.ingress.className | string | `""` |  |
| execution.ingress.enabled | bool | `false` |  |
| execution.ingress.hosts[0].host | string | `"chart-example.local"` |  |
| execution.ingress.hosts[0].paths[0].path | string | `"/"` |  |
| execution.ingress.hosts[0].paths[0].pathType | string | `"ImplementationSpecific"` |  |
| execution.ingress.hosts[0].port | int | `8545` |  |
| execution.ingress.tls | list | `[]` |  |
| execution.livenessProbe.httpGet.path | string | `"/"` |  |
| execution.livenessProbe.httpGet.port | string | `"rpc"` |  |
| execution.livenessProbe.initialDelaySeconds | int | `60` |  |
| execution.livenessProbe.periodSeconds | int | `30` |  |
| execution.livenessProbe.timeoutSeconds | int | `15` |  |
| execution.persistence.accessModes[0] | string | `"ReadWriteOnce"` |  |
| execution.persistence.annotations | object | `{}` |  |
| execution.persistence.enabled | bool | `true` |  |
| execution.persistence.mountPath | string | `"/data"` |  |
| execution.persistence.size | string | `"10Gi"` |  |
| execution.podAnnotations | object | `{}` |  |
| execution.podLabels | object | `{}` |  |
| execution.podSecurityContext | object | `{}` |  |
| execution.prometheus.enabled | bool | `false` |  |
| execution.prometheus.path | string | `"/debug/metrics/prometheus"` |  |
| execution.prometheus.port | string | `"metrics"` |  |
| execution.readinessProbe.httpGet.path | string | `"/"` |  |
| execution.readinessProbe.httpGet.port | string | `"rpc"` |  |
| execution.readinessProbe.initialDelaySeconds | int | `30` |  |
| execution.readinessProbe.periodSeconds | int | `30` |  |
| execution.readinessProbe.timeoutSeconds | int | `15` |  |
| execution.resources | object | `{}` |  |
| execution.securityContext | object | `{}` |  |
| execution.service.cluster.ports[0].name | string | `"rpc"` |  |
| execution.service.cluster.ports[0].port | int | `8545` |  |
| execution.service.cluster.ports[0].protocol | string | `"TCP"` |  |
| execution.service.cluster.ports[1].name | string | `"rpc-ws"` |  |
| execution.service.cluster.ports[1].port | int | `8546` |  |
| execution.service.cluster.ports[1].protocol | string | `"TCP"` |  |
| execution.service.cluster.ports[2].name | string | `"auth-rpc"` |  |
| execution.service.cluster.ports[2].port | int | `8551` |  |
| execution.service.cluster.ports[2].protocol | string | `"TCP"` |  |
| execution.service.node.ports[0].name | string | `"p2p-tcp"` |  |
| execution.service.node.ports[0].port | int | `30303` |  |
| execution.service.node.ports[0].protocol | string | `"TCP"` |  |
| execution.service.node.ports[1].name | string | `"p2p-udp"` |  |
| execution.service.node.ports[1].port | int | `30303` |  |
| execution.service.node.ports[1].protocol | string | `"UDP"` |  |
| execution.volumeMounts | list | `[]` |  |
| execution.volumes | list | `[]` |  |
| fullnameOverride | string | `""` |  |
| imagePullSecrets | list | `[]` |  |
| nameOverride | string | `""` |  |
| nodeSelector | object | `{}` |  |
| serviceAccount.annotations | object | `{}` |  |
| serviceAccount.automount | bool | `true` |  |
| serviceAccount.create | bool | `true` |  |
| serviceAccount.name | string | `""` |  |
| tolerations | list | `[]` |  |
| updateStrategy | string | `"OnDelete"` |  |

----------------------------------------------
Autogenerated from chart metadata using [helm-docs v1.5.0](https://github.com/norwoodj/helm-docs/releases/v1.5.0)
