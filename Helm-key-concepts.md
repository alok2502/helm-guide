
# Helm and Helm Charts

## Key Concepts
- **Helm**: Package manager for Kubernetes (k8s), similar to `apt` for Linux.
- **Helm Charts**: Bundles of applications that can be shared and used by others.
- **Helm Repo**: Repository where all charts are stored. Bitnami is a popular repo.
- **Release**: Deployed instance of the chart.

## Why Helm?
- Simplifies the installation of third-party applications or controllers related to k8s.
- Without Helm, installing third-party applications involves creating namespaces, service accounts, etc.
- Helm uses the current context from the kubeconfig file to work on the appropriate cluster.

## Helm Commands
- **Add Repo**: `helm repo add <repo_name> <repo_url>`
- **Search**: `helm search <keyword>`
- **Install**: `helm install <release_name> <chart_name>`
- **Create**: `helm create <chart_name>`
- **Package**: `helm package <chart_name>`

## Helm Chart Structure
- **Chart.yaml**: Metadata related to the chart (e.g., creator, version).
- **Values.yaml**: Customization for the templates.
- **Templates Folder**: Contains all YAML manifests like deployment, service, service account, ingress, etc.
- **Charts Folder**: For dependencies (can be ignored).

## Example Commands
- `helm repo add bitnami https://charts.bitnami.com/bitnami`
- `helm search repo bitnami`
- `helm install my-release bitnami/nginx`
- `helm create my-chart`
- `helm package my-chart`
