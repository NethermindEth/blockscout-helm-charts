# blockscout-stack

![Version: 2.0.7](https://img.shields.io/badge/Version-2.0.7-informational?style=flat-square) ![Type: application](https://img.shields.io/badge/Type-application-informational?style=flat-square) ![AppVersion: 7.0.0](https://img.shields.io/badge/AppVersion-7.0.0-informational?style=flat-square)

A Helm chart to deploy Blockscout stack

## Maintainers

| Name | Email | Url |
| ---- | ------ | --- |
| AntiD2ta |  |  |
| nmjustinchan |  |  |

## Values

| Key | Type | Default | Description |
|-----|------|---------|-------------|
| affinity | object | `{}` |  |
| blockscout.args[0] | string | `"-c"` |  |
| blockscout.args[1] | string | `"bin/blockscout start"` |  |
| blockscout.command[0] | string | `"/bin/sh"` |  |
| blockscout.enabled | bool | `true` |  |
| blockscout.env | list | `[]` |  |
| blockscout.envFrom | list | `[]` |  |
| blockscout.envFromSecret | list | `[]` |  |
| blockscout.extraEnv | list | `[]` |  |
| blockscout.image.pullPolicy | string | `"IfNotPresent"` |  |
| blockscout.image.repository | string | `"blockscout/blockscout"` |  |
| blockscout.image.tag | string | `"latest"` |  |
| blockscout.ingress.annotations | object | `{}` |  |
| blockscout.ingress.className | string | `""` |  |
| blockscout.ingress.enabled | bool | `false` |  |
| blockscout.ingress.hostname | string | `"chart-example.local"` |  |
| blockscout.ingress.paths[0].path | string | `"/api"` |  |
| blockscout.ingress.paths[0].pathType | string | `"Prefix"` |  |
| blockscout.ingress.paths[1].path | string | `"/socket"` |  |
| blockscout.ingress.paths[1].pathType | string | `"Prefix"` |  |
| blockscout.ingress.paths[2].path | string | `"/sitemap.xml"` |  |
| blockscout.ingress.paths[2].pathType | string | `"Prefix"` |  |
| blockscout.ingress.paths[3].path | string | `"/public-metrics"` |  |
| blockscout.ingress.paths[3].pathType | string | `"Prefix"` |  |
| blockscout.ingress.paths[4].path | string | `"/auth/auth0"` |  |
| blockscout.ingress.paths[4].pathType | string | `"Exact"` |  |
| blockscout.ingress.paths[5].path | string | `"/auth/auth0/callback"` |  |
| blockscout.ingress.paths[5].pathType | string | `"Exact"` |  |
| blockscout.ingress.paths[6].path | string | `"/auth/logout"` |  |
| blockscout.ingress.paths[6].pathType | string | `"Exact"` |  |
| blockscout.ingress.tls.enabled | bool | `false` |  |
| blockscout.init.args[0] | string | `"-c"` |  |
| blockscout.init.args[1] | string | `"bin/blockscout eval \"Elixir.Explorer.ReleaseTasks.create_and_migrate()\""` |  |
| blockscout.init.command[0] | string | `"/bin/sh"` |  |
| blockscout.init.enabled | bool | `true` |  |
| blockscout.livenessProbe.enabled | bool | `true` |  |
| blockscout.livenessProbe.params.initialDelaySeconds | int | `100` |  |
| blockscout.livenessProbe.params.periodSeconds | int | `100` |  |
| blockscout.livenessProbe.params.timeoutSeconds | int | `30` |  |
| blockscout.livenessProbe.path | string | `"/api/health/liveness"` |  |
| blockscout.nftStorage.accessKey | string | `""` |  |
| blockscout.nftStorage.bucketHost | string | `"xxx.r2.cloudflarestorage.com"` |  |
| blockscout.nftStorage.bucketName | string | `"nft"` |  |
| blockscout.nftStorage.bucketUrl | string | `"https://pub-xxx.r2.dev"` |  |
| blockscout.nftStorage.cookie | string | `"secret"` |  |
| blockscout.nftStorage.enabled | bool | `false` |  |
| blockscout.nftStorage.ipfsGateway | string | `"https://ipfs.io/ipfs"` |  |
| blockscout.nftStorage.resources.limits.cpu | int | `2` |  |
| blockscout.nftStorage.resources.limits.memory | string | `"4Gi"` |  |
| blockscout.nftStorage.resources.requests.cpu | int | `1` |  |
| blockscout.nftStorage.resources.requests.memory | string | `"2Gi"` |  |
| blockscout.nftStorage.secretKey | string | `""` |  |
| blockscout.podAnnotations | object | `{}` |  |
| blockscout.podSecurityContext | object | `{}` |  |
| blockscout.readinessProbe.enabled | bool | `true` |  |
| blockscout.readinessProbe.params.initialDelaySeconds | int | `60` |  |
| blockscout.readinessProbe.params.periodSeconds | int | `10` |  |
| blockscout.readinessProbe.params.timeoutSeconds | int | `60` |  |
| blockscout.readinessProbe.path | string | `"/api/health/readiness"` |  |
| blockscout.replicaCount | int | `1` |  |
| blockscout.resources.limits.cpu | int | `2` |  |
| blockscout.resources.limits.memory | string | `"4Gi"` |  |
| blockscout.resources.requests.cpu | int | `1` |  |
| blockscout.resources.requests.memory | string | `"2Gi"` |  |
| blockscout.securityContext | object | `{}` |  |
| blockscout.separateApi.enabled | bool | `false` |  |
| blockscout.separateApi.replicaCount | int | `2` |  |
| blockscout.separateApi.resources.limits.cpu | int | `1` |  |
| blockscout.separateApi.resources.limits.memory | string | `"2Gi"` |  |
| blockscout.separateApi.resources.requests.cpu | string | `"500m"` |  |
| blockscout.separateApi.resources.requests.memory | string | `"1Gi"` |  |
| blockscout.service.port | int | `80` |  |
| blockscout.service.type | string | `"ClusterIP"` |  |
| blockscout.terminationGracePeriodSeconds | int | `300` |  |
| blockscout.volumeMounts | list | `[]` |  |
| blockscout.volumes | list | `[]` |  |
| config.account.enabled | bool | `false` |  |
| config.nameService.enabled | bool | `false` |  |
| config.nameService.url | string | `""` |  |
| config.network.currency.decimals | int | `18` |  |
| config.network.currency.dualToken | bool | `false` |  |
| config.network.currency.name | string | `"Ether"` |  |
| config.network.currency.symbol | string | `"ETH"` |  |
| config.network.id | int | `1` |  |
| config.network.name | string | `"Ether"` |  |
| config.network.shortname | string | `"Ether"` |  |
| config.prometheus.blackbox.enabled | bool | `true` |  |
| config.prometheus.blackbox.path | string | `"/api/health"` |  |
| config.prometheus.enabled | bool | `true` |  |
| config.prometheus.ingressWhitelist.annotations."nginx.ingress.kubernetes.io/whitelist-source-range" | string | `"10.0.0.0/8,172.16.0.0/12,192.168.0.0/16"` |  |
| config.prometheus.ingressWhitelist.enabled | bool | `true` |  |
| config.testnet | bool | `false` |  |
| frontend.enabled | bool | `true` |  |
| frontend.env | list | `[]` |  |
| frontend.envFrom | list | `[]` |  |
| frontend.envFromSecret | list | `[]` |  |
| frontend.extraEnv | list | `[]` |  |
| frontend.image.pullPolicy | string | `"IfNotPresent"` |  |
| frontend.image.repository | string | `"ghcr.io/blockscout/frontend"` |  |
| frontend.image.tag | string | `"latest"` |  |
| frontend.ingress.annotations | object | `{}` |  |
| frontend.ingress.className | string | `""` |  |
| frontend.ingress.enabled | bool | `false` |  |
| frontend.ingress.hostname | string | `"chart-example.local"` |  |
| frontend.ingress.paths[0].path | string | `"/"` |  |
| frontend.ingress.tls.enabled | bool | `false` |  |
| frontend.livenessProbe.enabled | bool | `true` |  |
| frontend.livenessProbe.params.initialDelaySeconds | int | `100` |  |
| frontend.livenessProbe.params.periodSeconds | int | `100` |  |
| frontend.livenessProbe.params.timeoutSeconds | int | `30` |  |
| frontend.livenessProbe.path | string | `"/api/healthz"` |  |
| frontend.podAnnotations | object | `{}` |  |
| frontend.podSecurityContext | object | `{}` |  |
| frontend.port | int | `3000` |  |
| frontend.readinessProbe.enabled | bool | `true` |  |
| frontend.readinessProbe.params.initialDelaySeconds | int | `30` |  |
| frontend.readinessProbe.params.periodSeconds | int | `10` |  |
| frontend.readinessProbe.params.timeoutSeconds | int | `30` |  |
| frontend.readinessProbe.path | string | `"/api/healthz"` |  |
| frontend.replicaCount | int | `2` |  |
| frontend.resources.limits.cpu | string | `"500m"` |  |
| frontend.resources.limits.memory | string | `"1Gi"` |  |
| frontend.resources.requests.cpu | string | `"250m"` |  |
| frontend.resources.requests.memory | string | `"256Mi"` |  |
| frontend.securityContext | object | `{}` |  |
| frontend.service.port | int | `80` |  |
| frontend.service.type | string | `"ClusterIP"` |  |
| fullnameOverride | string | `""` |  |
| imagePullSecrets | list | `[]` |  |
| nameOverride | string | `""` |  |
| nodeSelector | object | `{}` |  |
| serviceAccount.annotations | object | `{}` |  |
| serviceAccount.create | bool | `true` |  |
| serviceAccount.name | string | `""` |  |
| stats.enabled | bool | `false` |  |
| stats.env | list | `[]` |  |
| stats.envFromSecret | list | `[]` |  |
| stats.extraEnv | list | `[]` |  |
| stats.files.enabled | bool | `false` |  |
| stats.files.list | object | `{}` |  |
| stats.files.mountPath | string | `"/tmp/path"` |  |
| stats.image.pullPolicy | string | `"IfNotPresent"` |  |
| stats.image.repository | string | `"ghcr.io/blockscout/stats"` |  |
| stats.image.tag | string | `"v2.4.0"` |  |
| stats.ingress.annotations | object | `{}` |  |
| stats.ingress.className | string | `""` |  |
| stats.ingress.enabled | bool | `false` |  |
| stats.ingress.hostname | string | `"chart-example-stats.local"` |  |
| stats.ingress.paths[0].path | string | `"/"` |  |
| stats.ingress.paths[0].pathType | string | `"Prefix"` |  |
| stats.ingress.tls.enabled | bool | `false` |  |
| stats.livenessProbe.enabled | bool | `true` |  |
| stats.livenessProbe.params.initialDelaySeconds | int | `100` |  |
| stats.livenessProbe.params.periodSeconds | int | `100` |  |
| stats.livenessProbe.params.timeoutSeconds | int | `30` |  |
| stats.livenessProbe.path | string | `"/health"` |  |
| stats.podAnnotations | object | `{}` |  |
| stats.podSecurityContext | object | `{}` |  |
| stats.readinessProbe.enabled | bool | `true` |  |
| stats.readinessProbe.params.initialDelaySeconds | int | `60` |  |
| stats.readinessProbe.params.periodSeconds | int | `10` |  |
| stats.readinessProbe.params.timeoutSeconds | int | `60` |  |
| stats.readinessProbe.path | string | `"/health"` |  |
| stats.replicaCount | int | `1` |  |
| stats.resources.limits.cpu | string | `"250m"` |  |
| stats.resources.limits.memory | string | `"512Mi"` |  |
| stats.resources.requests.cpu | string | `"250m"` |  |
| stats.resources.requests.memory | string | `"512Mi"` |  |
| stats.securityContext | object | `{}` |  |
| stats.service.metricsPort | int | `6060` |  |
| stats.service.port | int | `80` |  |
| stats.service.type | string | `"ClusterIP"` |  |
| tolerations | list | `[]` |  |
| userOpsIndexer.enabled | bool | `false` |  |
| userOpsIndexer.env | list | `[]` |  |
| userOpsIndexer.envFromSecret | list | `[]` |  |
| userOpsIndexer.extraEnv | list | `[]` |  |
| userOpsIndexer.image.pullPolicy | string | `"IfNotPresent"` |  |
| userOpsIndexer.image.repository | string | `"ghcr.io/blockscout/user-ops-indexer"` |  |
| userOpsIndexer.image.tag | string | `"latest"` |  |
| userOpsIndexer.ingress.annotations | object | `{}` |  |
| userOpsIndexer.ingress.className | string | `""` |  |
| userOpsIndexer.ingress.enabled | bool | `false` |  |
| userOpsIndexer.ingress.hostname | string | `"chart-example-stats.local"` |  |
| userOpsIndexer.ingress.paths[0].path | string | `"/"` |  |
| userOpsIndexer.ingress.paths[0].pathType | string | `"Prefix"` |  |
| userOpsIndexer.ingress.tls.enabled | bool | `false` |  |
| userOpsIndexer.livenessProbe.enabled | bool | `false` |  |
| userOpsIndexer.livenessProbe.params.initialDelaySeconds | int | `100` |  |
| userOpsIndexer.livenessProbe.params.periodSeconds | int | `100` |  |
| userOpsIndexer.livenessProbe.params.timeoutSeconds | int | `30` |  |
| userOpsIndexer.livenessProbe.path | string | `"/health"` |  |
| userOpsIndexer.podAnnotations | object | `{}` |  |
| userOpsIndexer.podSecurityContext | object | `{}` |  |
| userOpsIndexer.readinessProbe.enabled | bool | `false` |  |
| userOpsIndexer.readinessProbe.params.initialDelaySeconds | int | `60` |  |
| userOpsIndexer.readinessProbe.params.periodSeconds | int | `10` |  |
| userOpsIndexer.readinessProbe.params.timeoutSeconds | int | `60` |  |
| userOpsIndexer.readinessProbe.path | string | `"/health"` |  |
| userOpsIndexer.replicaCount | int | `1` |  |
| userOpsIndexer.resources.limits.cpu | string | `"250m"` |  |
| userOpsIndexer.resources.limits.memory | string | `"512Mi"` |  |
| userOpsIndexer.resources.requests.cpu | string | `"250m"` |  |
| userOpsIndexer.resources.requests.memory | string | `"512Mi"` |  |
| userOpsIndexer.securityContext | object | `{}` |  |
| userOpsIndexer.service.grpc.enabled | bool | `true` |  |
| userOpsIndexer.service.grpc.port | int | `8051` |  |
| userOpsIndexer.service.metricsPort | int | `6060` |  |
| userOpsIndexer.service.port | int | `80` |  |
| userOpsIndexer.service.type | string | `"ClusterIP"` |  |

----------------------------------------------
Autogenerated from chart metadata using [helm-docs v1.14.2](https://github.com/norwoodj/helm-docs/releases/v1.14.2)
