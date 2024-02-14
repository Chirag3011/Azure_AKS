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
  kubectl get all --all-namespaces --> to list everything
  kubectl config view  ---> get congiguration of cluster
  kubectl cluster-info ---> Display endpoint information about the master and services in the cluster
  kubectl get deployment
  kubectl describe deployment/pod/svc/ingress/ingreclass/ingresscontroller <name>  ---> Display the detailed state of one or more deployments/resource/objects..
  kubectl logs <pod_name> 
  kubectl logs --since=1h <pod_name> 
  kubectl logs --tail=20 <pod_name
  kubectl logs -f <service_name> [-c <$container>]
  kubectl logs -f <pod_name>
  kubectl top node  ---> Display Resource usage (CPU/Memory/Storage) for nodes
  kubectl describe nodes | grep Allocated -A 5  ---> Resource allocation per node
  kubectl exec <pod_name> -c <container_name> <command> ---> Execute a command against a container in a pod


