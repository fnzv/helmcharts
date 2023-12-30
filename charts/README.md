# helm-charts

## Usage

1. Add or update a Helm chart: push your source code of Helm chart under `charts/<your chart>`
1. New release will be created by [GitHub Actions](https://github.com/fnzv/helmcharts/blob/main/.github/workflows/ci.yaml) (e.g. https://github.com/fnzv/helmcharts/releases/tag/example-0.1.0)
1. Add this helm chart repo to your helm client configuration
    ```
    helm repo add fnzv https://charts.sa.mi.it
    helm repo update
    ```
1. Update repo and search
    ```
    helm search repo fnzv
    NAME                    CHART VERSION   APP VERSION     DESCRIPTION
    fnzv/example            0.1.0           1.16.0          A Helm chart for Kubernetes
    fnzv/fr24feeder         0.1.2                           A Helm chart for deploying fr24feeder
    ```
1. Install
    ```
    helm install example fnzv/example 
    ```
1. Upgrade (optional)
    ```
    helm upgrade example fnzv/example --set ingress=true
    ```
1. Uninstall
    ```
    helm uninstall example
    ```

