# Azure Kubernetes Service (AKS) YAML Files

This repository contains YAML files for configuring and deploying resources on Azure Kubernetes Service (AKS). These files are designed to streamline the deployment and management of your AKS clusters.

## Files

- **`deployment.yaml`**: Configuration for the deployment of your application on AKS.
- **`service.yaml`**: Configuration for creating Kubernetes services to expose your application.

## Prerequisites

Before using these YAML files, make sure you have the following prerequisites in place:

- An active Azure subscription.
- Azure CLI installed: [Install Azure CLI](https://docs.microsoft.com/en-us/cli/azure/install-azure-cli).
- kubectl installed: [Install kubectl](https://kubernetes.io/docs/tasks/tools/install-kubectl/).

## Usage

1. **Deploy to AKS:**

   ```bash
   kubectl apply -f deployments.yaml
   kubectl apply -f services.yaml
   kubectl apply -f configMaps.yaml

2. **Fetch Details**

  ```bash
  kubectl get services
  kubectl get pods
  kubectl get pods -o custom-columns=POD:.metadata.name,CONTAINERS:.spec.containers[*].name --> to get running containers

