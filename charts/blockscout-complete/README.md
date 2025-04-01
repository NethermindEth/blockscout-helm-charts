# Blockscout Complete Helm Chart

This Helm chart deploys a complete Blockscout setup, including both the Blockscout stack and the Smart Contract Verification services.

## Overview

The chart combines two existing charts:
- `blockscout-stack`: Provides the main Blockscout application, frontend, and optional components
- `smart-contract-verification`: Provides smart contract verification services, including sig-provider, smart-contract-verifier, and eth-bytecode-db

## Prerequisites

- Kubernetes 1.19+
- Helm 3.2.0+
- PV provisioner support in the underlying infrastructure (if persistence is required)

## Installation

```bash
# Add the repository
helm repo add blockscout-complete https://your-repo-url

# Install the chart
helm install my-blockscout blockscout-complete/blockscout-complete
```

Or install from local directory:

```bash
# Install from local directory
helm install my-blockscout ./blockscout-complete
```

## Configuration

The chart combines configuration from both blockscout-stack and smart-contract-verification charts. You can customize the deployment by modifying the values in `values.yaml`.

### Key Parameters

| Parameter | Description | Default |
|-----------|-------------|---------|
| `blockscout-stack.enabled` | Enable/disable blockscout-stack chart | `true` |
| `smart-contract-verification.enabled` | Enable/disable smart-contract-verification chart | `true` |
| `blockscout-stack.config.network.id` | Blockchain network ID | `1` |
| `blockscout-stack.config.network.name` | Blockchain network name | `Ether` |
| `blockscout-stack.blockscout.image.tag` | Blockscout image tag | `latest` |
| `smart-contract-verification.smartContractVerifier.image.tag` | Smart contract verifier image tag | `latest` |

For a complete list of parameters, please refer to the original charts:
- [blockscout-stack documentation](../blockscout-stack/README.md)
- [smart-contract-verification documentation](../smart-contract-verification/README.md)

## Architecture

The combined chart deploys multiple services:

1. **Blockscout Core Components**:
   - Blockscout API & Indexer
   - Frontend UI
   - Stats (optional)
   - User-Ops Indexer (optional)

2. **Smart Contract Verification Services**:
   - Smart Contract Verifier (HTTP & gRPC)
   - Sig Provider
   - Ethereum Bytecode DB (optional)

Each component is exposed via its own service and can be configured independently. The default configuration avoids port conflicts by using different service ports for each component.

## Ingress Configuration

The chart provides ingress configurations for all services. By default, each service gets its own hostname. You can customize these values to configure routing as needed for your environment.

For example:
- blockscout.example.com - Main Blockscout UI and API
- verifier.example.com - Smart Contract Verification API
- bytecode-db.example.com - Bytecode DB UI and API

## Integration

The Blockscout UI is pre-configured to use the Smart Contract Verification services. The connections between services are established using Kubernetes DNS service discovery.

## Troubleshooting

If you encounter issues:

1. Check pod status: `kubectl get pods -l app.kubernetes.io/instance=my-blockscout`
2. Check logs: `kubectl logs -l app.kubernetes.io/instance=my-blockscout -c blockscout`
3. Verify services are running: `kubectl get svc -l app.kubernetes.io/instance=my-blockscout` 