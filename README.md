## Description
Use `kustomize` to DRY Kubernetes manifests.

## Structure
- `base` contains the base manifests. These will be overridden by patches in the `overlay` directory.
- `overlay` contains the environment specific manifests. These will override the base manifests.
- `overlay/staging`, for example, will override the base manifests with the Staging specific manifests.

## Usage
```shell
$ kustomize build overlay/staging
```