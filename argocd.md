
kubectl create namespace argocd
kubectl apply -n argocd -f https://raw.githubusercontent.com/argoproj/argo-cd/stable/manifests/install.yaml
k get ns
k get pods -n argocd 
k edit svc argocd-server -n argocd
minikube service list -n argocd

# Part 4 - helm public chart
$ helm install my-release oci://registry-1.docker.io/bitnamicharts/argo-cd
$ helm pull argo-cd my-release oci://registry-1.docker.io/bitnamicharts/argo-cd

# Part 5 - Create own py project  helm chart 
python3 --version

$ cat script.py
import time
print("Py app started ...")
time.sleep(60)
print("Py app terminated")

python3 script.py   

cat dockerfile                        

FROM python:3.8
WORKDIR /app
COPY . /app
CMD ["python3", "script.py"]

# Build Docker image
docker build -t python-app .

# Run Docker image
docker run -p 9001:9001 python-app

docker tag <image-name> <account-name>/<repo-name>:<tag-name>
docker tag python-app arunsre/helm:t-python-app

docker login 

docker push <account-name>/<repo-name>:<tag-name>
docker push arunsre/helm:t-python-app	

k svc svc-name --url 

principles of Gitops

Declarative
Versioned and immuntable
Pulled Automatically 
Continously Reconcilation

GITOPS Tools:
============

argocd
fluxcd
jenkinsx
spinnaker

Argocd Architecture Components:

Reposerver
Application controller 
API server
Dex
Redis 
