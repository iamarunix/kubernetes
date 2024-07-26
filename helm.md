# Helm Series

## Offical Helm page 

https://helm.sh/

## Helm installation (Linux)

- $ curl -fsSL -o get_helm.sh https://raw.githubusercontent.com/helm/helm/main/scripts/get-helm-3
- $ chmod 700 get_helm.sh
- $ ./get_helm.sh

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
- helm install webserver --debug --dry-run nginx
- helm pull bitnami/jenkins 
- helm rollback jen 43
- helm upgrade fox 
- helm lint jen
- helm uninstall fox 

## Part 3 - helm repo 

- helm repo list 
- helm repo add bitnami https://charts.bitnami.com/bitnami
- helm search repo # to check all available charts 
- helm search repo mysql # to check particular chart 
- helm repo update
- helm repo remove bitnami
