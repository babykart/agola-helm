# agola-helm

[![Artifact Hub](https://img.shields.io/endpoint?url=https://artifacthub.io/badge/repository/agola)](https://artifacthub.io/packages/search?repo=agola)
[![License](https://img.shields.io/badge/License-MIT-blue)](https://opensource.org/licenses/MIT)

## Usage

[Helm](https://helm.sh) must be installed to use the charts. Please refer to
Helm's [documentation](https://helm.sh/docs) to get started.

Once Helm has been set up correctly, add the repo as follows:

```sh
helm repo add agola-helm https://babykart.github.io/agola-helm
```

If you had already added this repo earlier, run `helm repo update` to retrieve
the latest versions of the packages. You can then run `helm search repo
agola-helm` to see the charts.

To install the agola chart:

```sh
helm upgrade --install agola agola-helm/agola
```

Using an OCI-based registry:

```sh
helm upgrade --install agola oci://ghcr.io/babykart/helm-charts/agola
 ```

To uninstall the chart:

```sh
helm delete agola
```
