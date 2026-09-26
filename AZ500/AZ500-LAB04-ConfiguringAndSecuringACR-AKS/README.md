# AZ‑500 LAB04: Configuring and Securing ACR & AKS

## 🎯 Objective
This lab focuses on deploying and securing **Azure Container Registry (ACR)** and **Azure Kubernetes Service (AKS)**. It demonstrates how to build, store, and deploy containerized applications securely in Azure, aligned with the *Implement platform protection* module of the AZ‑500 certification.

## 📚 Context
This lab is based on the official Microsoft Learning exercise *LAB_04_ConfiguringandSecuringACRandAKS*.  
It highlights:

- Building Docker images from a Dockerfile  
- Storing container images securely in ACR  
- Deploying an AKS cluster  
- Enabling secure AKS ↔ ACR integration  
- Deploying internal and external Kubernetes services  
- Validating secure access and container runtime behavior  

## 🧪 Planned Steps

1. Deploy an **Azure Container Registry (ACR)**
2. Build a Docker image and push it to ACR
3. Deploy an **Azure Kubernetes Service (AKS)** cluster
4. Grant AKS permissions to pull images from ACR (AcrPull role)
5. Deploy Kubernetes workloads using YAML manifests:
   - Internal service
   - External service
6. Validate access to both services
7. Review authentication and security mechanisms between ACR and AKS

## 🧠 Personal Notes
Walkthrough steps, command outputs, and observations will be documented in the `notes/` folder.

## 📸 Screenshots
Screenshots will be added to the `screenshots/` folder to illustrate:

- ACR deployment  
- Docker image build & push  
- AKS cluster deployment  
- ACR ↔ AKS integration  
- Kubernetes service deployment  
- Internal/external connectivity tests  

## 🧩 Deployment Files & Scripts

- Kubernetes manifests:
  - `nginxexternal.yaml`
  - `nginxinternal.yaml`

## 📎 References

- Microsoft Learn: Azure Container Registry documentation  
- Microsoft Learn: Azure Kubernetes Service documentation  
- AZ‑500 official learning path: *Implement platform protection*

