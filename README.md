# Description

Ethereum Helm charts for Kubernetes - select your choice of `elc` and `clc` client and you can deploy it to K8S. This also supports `aws` and `azure` so you can pick the appropriate provider. If you are running this locally, please make sure you have a lot of resources avialable ie. disk space, cpu and RAM

## Values

| Key      | Type   | Default     | Description |
|----------|--------|-------------|-------------|
| provider | string | `"local"`   |             |
| network  | string | `"sepolia"` |             |
| env      | string | `"dev"`     |             |
| elc      | string | `"besu"`    |             |
| clc      | string | `"teku"`    |             |



### Test the charts:
local
```
helm template jl ./ --namespace ethereum --create-namespace --values ./examples/mainnet/besu-teku-local.yaml > /tmp/besu-teku-mainnet-local.yml
```
aws
```
helm template jw ./ --namespace ethereum --create-namespace --values ./examples/mainnet/besu-teku-aws.yaml > /tmp/besu-teku-mainnet-aws.yml
```
azure
```
helm template jz ./ --namespace ethereum --create-namespace --values ./examples/mainnet/besu-teku-azure.yaml > /tmp/besu-teku-mainnet-azure.yml
```

## TODO
- support for validators + w3s
- add on other clients