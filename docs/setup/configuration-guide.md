# Configuration Guide

## Ground Control Configuration

Ground Control, the dedicated portal for managing and visualizing your algorithm deployments, can be enabled or disabled according to your needs.

To enable or disable Ground Control, update the values.yaml file as follows:

```yaml
groundControl:
  enabled: true
```

In this configuration, setting `groundControl.enabled` to `true` will activate Ground Control. If you prefer not to use Ground Control, simply set this value to `false`.

## Database Configuration

OuterSpace Operator relies exclusively on __PostreSQL__. However, you can either utilize a PostgreSQL database that can be managed (like Google Cloud SQL) or directly deployed within your Kubernetes cluster using the Bitnami's PostgreSQL Helm chart. For the latter, you need to enable it in the `values.yaml` file:

```yaml
postgresql:
  enabled: true
```

In this configuration, setting `postgresql.enabled` to `true` will install __PostgreSQL__ directly in your Kubernetes cluster using Bitnami's PostgreSQL Helm chart.

## Monitoring Configuration

When deploying on GKE, OuterSpace Operator can leverage __Managed Prometheus__ for monitoring or pull in Prometheus using its Helm chart. Update the `values.yaml` file with the relevant settings.

```yaml
prometheus:
  managed: false
```

In this configuration, setting `prometheus.managed` to `false` means that __Managed Prometheus__ will not be used. Instead, Prometheus will be pulled in via its Helm chart.

## Ingress Configuration

The OuterSpace Operator provides flexibility when it comes to managing ingress for your algorithms. It can integrate with multiple ingress classes including __NGINX__, __Kong__, or __GCE__. You can specify your choice in the `values.yaml` file:

```yaml

ingress:
  class: "nginx"
```

In this configuration, replace `nginx` with your preferred ingress class (`nginx`, `kong`, or `gce`).

!!! warning "Warning"
    Ensure that the selected ingress controller is properly installed and configured in your Kubernetes cluster.

