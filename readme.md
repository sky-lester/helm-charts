# Custom Helm Charts for Staffme Applications

This repository contains custom Helm charts to deploy and manage WordPress and Django applications on a Kubernetes cluster.

These charts simplify the deployment process by providing configurable templates for Kubernetes resources such as Deployments, Services, ConfigMaps, Ingress, Persistent Volumes, and more.

## How to add to local repo

```
helm repo add staffme https://sky-lester.github.io/helm-charts/
helm repo update
```

## Install an Application

helm upgrade --install [RELEASE_NAME] [CHART] -f [VALUES_FILE] -n [NAMESPACE] --create-namespace

```
helm upgrade --install dev1 staffme/cswp-chart -f values.yaml -n dev1 --create-namespace
```

## Uninstall an Application

helm uninstall [RELEASE_NAME]

```
helm uninstall dev1
```