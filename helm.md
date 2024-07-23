# Helm Series

## Offical Helm page 

https://helm.sh/

## Helm installation (Linux)

$ curl -fsSL -o get_helm.sh https://raw.githubusercontent.com/helm/helm/main/scripts/get-helm-3
$ chmod 700 get_helm.sh
$ ./get_helm.sh

## Part 1 - helm intro 

- why helm
- what is helm chart
- Advantages of helm chart
- Architecture of helm chart
- Use Cases
   
## Part 2 - helm chart 

- helm list 
- helm create hotel 
- helm install hotel-hilton hotel
- helm install --ns hotel-hilton hotel
- helm install jen bitnami/jenkins 
- helm pull bitnami/jenkins 
- helm rollback jen 43
- helm repo update
- helm upgrade hotel-hilton 
- helm lint jen
- helm install webserver --debug --dry-run nginx

## Part 3 - helm repo 

- helm repo list 
- helm repo add bitnami https://charts.bitnami.com/bitnami
- helm search repo # to check all available charts 
- helm search repo mysql # to check particular chart 
- helm repo update
