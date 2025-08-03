1 Introduction to ArgoCD
  ArgoCD UI

2 Problem Statement syncup, memory, configmap 
  Solution 

3 Gitops principles

4 ArgoCD Architecture
  Repository Server
  Application Controller
  API Server
  Redis
  Dex 
  
  5 Lab Setup: Installation of ArgoCD (yaml manifest, operator, helm )
  Prerequisites: AWS (EC2.t2.medium) Instance, KIND, Docker, kubectl, Argocd 
  Exposing the ArgoCD UI

6 ArgoCD Applications
  Deployment of applications in UI(Application YAML)
  Deployment of applications in CLI (Application YAML)
  Deployment of applications in UI (Application HELM CHART)
  Deployment of applications in CLI (Application HELM CHART)
  
7 Managing application lifecycle: Create, Sync, Delete 
  Sync strategies: Manual, Automatic, Prune, Self healing 
  
8 Managing Multiple Environments
  Using Git branches for different environments (Dev, Staging, Production)

9 Multi-cluster support in ArgoCD

10 ArgoCD CLI commands walkthrough - Troubleshooting  
