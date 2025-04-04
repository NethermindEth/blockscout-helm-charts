# blockscout-complete

![Version: 0.1.3](https://img.shields.io/badge/Version-0.1.3-informational?style=flat-square) ![Type: application](https://img.shields.io/badge/Type-application-informational?style=flat-square) ![AppVersion: 1.0.0](https://img.shields.io/badge/AppVersion-1.0.0-informational?style=flat-square)

A Helm chart that combines Blockscout stack with Smart Contract Verification services

## Maintainers

| Name | Email | Url |
| ---- | ------ | --- |
| AntiD2ta |  |  |
| nmjustinchan |  |  |

## Requirements

| Repository | Name | Version |
|------------|------|---------|
| file://../blockscout-stack | blockscout-stack | 2.0.6 |
| file://../smart-contract-verification | smart-contract-verification | 0.1.3 |

## Values

| Key | Type | Default | Description |
|-----|------|---------|-------------|
| blockscout-stack.blockscout.enabled | bool | `true` |  |
| blockscout-stack.blockscout.extraEnv[0].name | string | `"VERIFY_WITH_ETHBYTECODE_DB_ENABLED"` |  |
| blockscout-stack.blockscout.extraEnv[0].value | string | `"true"` |  |
| blockscout-stack.blockscout.extraEnv[1].name | string | `"SMART_CONTRACT_VERIFIER_ENABLED"` |  |
| blockscout-stack.blockscout.extraEnv[1].value | string | `"true"` |  |
| blockscout-stack.blockscout.extraEnv[2].name | string | `"SMART_CONTRACT_VERIFIER_URL"` |  |
| blockscout-stack.blockscout.extraEnv[2].value | string | `"http://$(RELEASE_NAME)-smart-contract-verification-verifier:8050"` |  |
| blockscout-stack.blockscout.extraEnv[3].name | string | `"SMART_CONTRACT_VERIFIER_GRPC_URL"` |  |
| blockscout-stack.blockscout.extraEnv[3].value | string | `"$(RELEASE_NAME)-smart-contract-verification-verifier:8051"` |  |
| blockscout-stack.blockscout.extraEnv[4].name | string | `"ETH_BYTECODE_DB_URL"` |  |
| blockscout-stack.blockscout.extraEnv[4].value | string | `"http://$(RELEASE_NAME)-smart-contract-verification-eth-bytecode-db:8050"` |  |
| blockscout-stack.blockscout.image.pullPolicy | string | `"IfNotPresent"` |  |
| blockscout-stack.blockscout.image.repository | string | `"blockscout/blockscout"` |  |
| blockscout-stack.blockscout.image.tag | string | `"latest"` |  |
| blockscout-stack.blockscout.ingress.annotations | object | `{}` |  |
| blockscout-stack.blockscout.ingress.className | string | `"nginx"` |  |
| blockscout-stack.blockscout.ingress.enabled | bool | `true` |  |
| blockscout-stack.blockscout.ingress.hostname | string | `"blockscout.example.com"` |  |
| blockscout-stack.blockscout.ingress.paths[0].path | string | `"/api"` |  |
| blockscout-stack.blockscout.ingress.paths[0].pathType | string | `"Prefix"` |  |
| blockscout-stack.blockscout.ingress.paths[1].path | string | `"/socket"` |  |
| blockscout-stack.blockscout.ingress.paths[1].pathType | string | `"Prefix"` |  |
| blockscout-stack.blockscout.ingress.paths[2].path | string | `"/sitemap.xml"` |  |
| blockscout-stack.blockscout.ingress.paths[2].pathType | string | `"Prefix"` |  |
| blockscout-stack.blockscout.ingress.paths[3].path | string | `"/public-metrics"` |  |
| blockscout-stack.blockscout.ingress.paths[3].pathType | string | `"Prefix"` |  |
| blockscout-stack.blockscout.ingress.paths[4].path | string | `"/auth/auth0"` |  |
| blockscout-stack.blockscout.ingress.paths[4].pathType | string | `"Exact"` |  |
| blockscout-stack.blockscout.ingress.paths[5].path | string | `"/auth/auth0/callback"` |  |
| blockscout-stack.blockscout.ingress.paths[5].pathType | string | `"Exact"` |  |
| blockscout-stack.blockscout.ingress.paths[6].path | string | `"/auth/logout"` |  |
| blockscout-stack.blockscout.ingress.paths[6].pathType | string | `"Exact"` |  |
| blockscout-stack.blockscout.ingress.tls.enabled | bool | `true` |  |
| blockscout-stack.blockscout.replicaCount | int | `1` |  |
| blockscout-stack.blockscout.service.port | int | `80` |  |
| blockscout-stack.blockscout.service.type | string | `"ClusterIP"` |  |
| blockscout-stack.config.account.enabled | bool | `false` |  |
| blockscout-stack.config.nameService.enabled | bool | `false` |  |
| blockscout-stack.config.nameService.url | string | `""` |  |
| blockscout-stack.config.network.currency.decimals | int | `18` |  |
| blockscout-stack.config.network.currency.dualToken | bool | `false` |  |
| blockscout-stack.config.network.currency.name | string | `"Ether"` |  |
| blockscout-stack.config.network.currency.symbol | string | `"ETH"` |  |
| blockscout-stack.config.network.id | int | `1` |  |
| blockscout-stack.config.network.name | string | `"Ether"` |  |
| blockscout-stack.config.network.shortname | string | `"Ether"` |  |
| blockscout-stack.config.prometheus.blackbox.enabled | bool | `true` |  |
| blockscout-stack.config.prometheus.blackbox.path | string | `"/api/health"` |  |
| blockscout-stack.config.prometheus.enabled | bool | `true` |  |
| blockscout-stack.config.prometheus.ingressWhitelist.annotations."nginx.ingress.kubernetes.io/whitelist-source-range" | string | `"10.0.0.0/8,172.16.0.0/12,192.168.0.0/16"` |  |
| blockscout-stack.config.prometheus.ingressWhitelist.enabled | bool | `true` |  |
| blockscout-stack.config.testnet | bool | `false` |  |
| blockscout-stack.enabled | bool | `true` |  |
| blockscout-stack.frontend.enabled | bool | `true` |  |
| blockscout-stack.frontend.image.pullPolicy | string | `"IfNotPresent"` |  |
| blockscout-stack.frontend.image.repository | string | `"ghcr.io/blockscout/frontend"` |  |
| blockscout-stack.frontend.image.tag | string | `"latest"` |  |
| blockscout-stack.frontend.ingress.annotations | object | `{}` |  |
| blockscout-stack.frontend.ingress.className | string | `"nginx"` |  |
| blockscout-stack.frontend.ingress.enabled | bool | `true` |  |
| blockscout-stack.frontend.ingress.hostname | string | `"blockscout.example.com"` |  |
| blockscout-stack.frontend.ingress.paths[0].path | string | `"/"` |  |
| blockscout-stack.frontend.ingress.paths[0].pathType | string | `"Prefix"` |  |
| blockscout-stack.frontend.ingress.tls.enabled | bool | `true` |  |
| blockscout-stack.frontend.replicaCount | int | `2` |  |
| blockscout-stack.frontend.service.port | int | `80` |  |
| blockscout-stack.frontend.service.type | string | `"ClusterIP"` |  |
| blockscout-stack.stats.enabled | bool | `false` |  |
| blockscout-stack.userOpsIndexer.enabled | bool | `false` |  |
| global.fullnameOverride | string | `""` |  |
| global.imagePullSecrets | list | `[]` |  |
| global.nameOverride | string | `""` |  |
| podMonitor.enabled | bool | `false` |  |
| serviceMonitor.enabled | bool | `false` |  |
| smart-contract-verification.enabled | bool | `true` |  |
| smart-contract-verification.ethBytecodeDb.enabled | bool | `true` |  |
| smart-contract-verification.ethBytecodeDb.extraEnv[0].name | string | `"ETH_BYTECODE_DB__SERVER__HTTP__ADDR"` |  |
| smart-contract-verification.ethBytecodeDb.extraEnv[0].value | string | `"0.0.0.0:8050"` |  |
| smart-contract-verification.ethBytecodeDb.extraEnv[1].name | string | `"ETH_BYTECODE_DB__VERIFICATION__VERIFIER_URLS__0"` |  |
| smart-contract-verification.ethBytecodeDb.extraEnv[1].value | string | `"http://$(RELEASE_NAME)-smart-contract-verification-verifier:8050"` |  |
| smart-contract-verification.ethBytecodeDb.image.pullPolicy | string | `"IfNotPresent"` |  |
| smart-contract-verification.ethBytecodeDb.image.repository | string | `"ghcr.io/blockscout/eth-bytecode-db"` |  |
| smart-contract-verification.ethBytecodeDb.image.tag | string | `"latest"` |  |
| smart-contract-verification.ethBytecodeDb.ingress.annotations | object | `{}` |  |
| smart-contract-verification.ethBytecodeDb.ingress.className | string | `"nginx"` |  |
| smart-contract-verification.ethBytecodeDb.ingress.enabled | bool | `true` |  |
| smart-contract-verification.ethBytecodeDb.ingress.hostname | string | `"bytecode-db.example.com"` |  |
| smart-contract-verification.ethBytecodeDb.ingress.tls.enabled | bool | `true` |  |
| smart-contract-verification.ethBytecodeDb.replicaCount | int | `1` |  |
| smart-contract-verification.ethBytecodeDb.service.port | int | `8050` |  |
| smart-contract-verification.ethBytecodeDb.service.type | string | `"ClusterIP"` |  |
| smart-contract-verification.sigProvider.image.pullPolicy | string | `"IfNotPresent"` |  |
| smart-contract-verification.sigProvider.image.repository | string | `"ghcr.io/blockscout/sig-provider"` |  |
| smart-contract-verification.sigProvider.image.tag | string | `"latest"` |  |
| smart-contract-verification.sigProvider.ingress.annotations | object | `{}` |  |
| smart-contract-verification.sigProvider.ingress.className | string | `"nginx"` |  |
| smart-contract-verification.sigProvider.ingress.enabled | bool | `true` |  |
| smart-contract-verification.sigProvider.ingress.hostname | string | `"sig-provider.example.com"` |  |
| smart-contract-verification.sigProvider.ingress.tls.enabled | bool | `true` |  |
| smart-contract-verification.sigProvider.replicaCount | int | `2` |  |
| smart-contract-verification.sigProvider.service.port | int | `8043` |  |
| smart-contract-verification.sigProvider.service.type | string | `"ClusterIP"` |  |
| smart-contract-verification.smartContractVerifier.grpc.enabled | bool | `true` |  |
| smart-contract-verification.smartContractVerifier.grpc.ingress.annotations | object | `{}` |  |
| smart-contract-verification.smartContractVerifier.grpc.ingress.className | string | `"nginx"` |  |
| smart-contract-verification.smartContractVerifier.grpc.ingress.enabled | bool | `true` |  |
| smart-contract-verification.smartContractVerifier.grpc.ingress.hostname | string | `"grpc-verifier.example.com"` |  |
| smart-contract-verification.smartContractVerifier.grpc.ingress.tls.enabled | bool | `true` |  |
| smart-contract-verification.smartContractVerifier.grpc.port | int | `8051` |  |
| smart-contract-verification.smartContractVerifier.image.pullPolicy | string | `"IfNotPresent"` |  |
| smart-contract-verification.smartContractVerifier.image.repository | string | `"ghcr.io/blockscout/smart-contract-verifier"` |  |
| smart-contract-verification.smartContractVerifier.image.tag | string | `"latest"` |  |
| smart-contract-verification.smartContractVerifier.ingress.annotations | object | `{}` |  |
| smart-contract-verification.smartContractVerifier.ingress.className | string | `"nginx"` |  |
| smart-contract-verification.smartContractVerifier.ingress.enabled | bool | `true` |  |
| smart-contract-verification.smartContractVerifier.ingress.hostname | string | `"verifier.example.com"` |  |
| smart-contract-verification.smartContractVerifier.ingress.tls.enabled | bool | `true` |  |
| smart-contract-verification.smartContractVerifier.replicaCount | int | `2` |  |
| smart-contract-verification.smartContractVerifier.service.port | int | `8050` |  |
| smart-contract-verification.smartContractVerifier.service.type | string | `"ClusterIP"` |  |

----------------------------------------------
Autogenerated from chart metadata using [helm-docs v1.14.2](https://github.com/norwoodj/helm-docs/releases/v1.14.2)
