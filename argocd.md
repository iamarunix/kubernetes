
kubectl create namespace argocd
  k get 
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

~ $ curl --silent --location "https://github.com/weaveworks/eksctl/releases/download/0.26.0-rc.1/eksctl_Linux_amd64.tar.gz" | tar xz -C /tmp
~ $ sudo mv /tmp/eksctl /usr/local/bin
~ $ export PATH=$PATH:/usr/local/bin/
~ $ eksctl version
0.26.0-rc.1

# eksctl get clusters
NAME                    REGION
serious-indie-sheepdog  us-east-1

aws eks --region us-east-1 update-kubeconfig --name serious-indie-sheepdog 

   33  k port-forward argocd-server-5c768cdd96-9jdgf 8080:80 -n argocd
   34  k port-forward argocd-server-5c768cdd96-9jdgf 8080:8080 -n argocd
