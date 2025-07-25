# Kubernetes Learning Notes

A comprehensive collection of Kubernetes learning materials covering core concepts, advanced features, and practical implementations.

## Contents

### Part 8: Helm & Monitoring
**File:** `Custom_RunningNotes_k8s_8`

#### Helm Package Management
- Chart structure and templating
- Values.yaml configuration
- Service and Ingress templates
- Value overriding with `--set` flags
- Advanced templating (conditionals, loops, named templates)

#### Monitoring & Logging Stack
- **Prometheus** - Metrics collection and alerting
- **Grafana** - Visualization and dashboards
- **Loki** - Log aggregation
- **Kube-state-metrics** - Kubernetes object metrics
- **Alertmanager** - Alert handling

#### Quick Start Commands

**Install monitoring stack:**
```bash
kubectl create namespace monitoring
helm repo add prometheus-community https://prometheus-community.github.io/helm-charts
helm install prometheus prometheus-community/prometheus --namespace monitoring
helm repo add grafana https://grafana.github.io/helm-charts
helm install grafana grafana/grafana --namespace monitoring
```

**Access dashboards:**
```bash
# Prometheus
kubectl port-forward svc/prometheus-server 9090:80 --namespace monitoring

# Grafana
kubectl port-forward svc/grafana 3000:80 --namespace monitoring
```

## Usage

These notes serve as both learning material and quick reference for Kubernetes implementations. Each section includes practical examples and working commands.

## Structure

- Conceptual explanations
- YAML configuration examples
- Command-line instructions
- Real-world implementation patterns