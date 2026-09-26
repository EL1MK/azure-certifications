# Exercise 1: Configuring and Securing ACR and AKS

The following architecture will be deployed and used throughout the exercise:

//image

## Task 1: Create an Azure Container Registry

The first step is to create a resource group to be used for the lab and an Azure Container Registry:
```az group create --name AZ500LAB04 --location eastus```

The Container Registry is registered in the lab environment:
```
az provider register --namespace Microsoft.Kubernetes
az provider register --namespace Microsoft.KubernetesConfiguration
az provider register --namespace Microsoft.OperationsManagement
az provider register --namespace Microsoft.OperationalInsights
az provider register --namespace Microsoft.ContainerService
az provider register --namespace Microsoft.ContainerRegistry
```
A new Azure Container Registry (ACR) instance is created:
```az acr create --resource-group AZ500LAB04 --name az500$RANDOM$RANDOM --sku Basic```

## Task 2: Create a Dockerfile, build a container and push it to Azure Container Registry

The goal is to create a Dockerfile

## Task 3: Create an Azure Kubernetes Service cluster

## Task 4: Grant the AKS cluster permissions to access the ACR and manage its virtual network

In this task, you will grant the AKS cluster permission to access the ACR and manage its virtual network.

## Task 5: Deploy an external service to AKS

## Task 6: Verify the you can access an external AKS-hosted service
In this task, verify the container can be accessed externally using the public IP address.

## Task 7: Deploy an internal service to AKS

## Task 8: Verify the you can access an internal AKS-hosted service
