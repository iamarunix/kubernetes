< What is Helm? /b>

It is like a package manager EXE in Windows and YUM in Linux 
It is a package manager in Linux that container lots of YAML files 




  - curl -fsSL -o get_helm.sh https://raw.githubusercontent.com/helm/helm/master/scripts/get-helm-3
  - chmod 700 get_helm.sh
  - ./get_helm.sh
  - helm version 



# Where Helm is used?

In Kuberenetes, it used to deploy a service/application

**- Why Helm?**
While compared to basic model of deployment in Kubernetes, Helm is easy and faster in deployments.

2.1 Download eksctl

curl --silent --location "https://github.com/weaveworks/eksctl/releases/latest/download/eksctl_$(uname -s)_amd64.tar.gz" | tar xz -C /tmp

2.2 Move eksctl to /usr/local/bin or /home/cloudshell-user/bin folder

sudo mv /tmp/eksctl /usr/local/bin

2.3 Test the installation by checking the version

eksctl version

Step 3 : Create Key Pair

Note : You can use existing key pairs as well so replace the key apprpriately.

This key is used to connect to EC2 nodes created by EKS cluster.

aws ec2 create-key-pair --key-name eksKeyPair --query 'KeyMaterial' --output text > eksKeyPair.pem

Step 4 : Create EKS Cluster

Create cluster with the default settings. This may take around 15–20 minutes so take a cup of coffee !

eksctl create cluster \
--name test-cluster \
--region ap-south-1 \
--with-oidc \
--ssh-access \
--ssh-public-key eksKeyPair

5.1 Download kubectl

curl -o kubectl https://amazon-eks.s3.us-west-2.amazonaws.com/1.21.2/2021-07-05/bin/linux/amd64/kubectl

5.2 Apply execute permission

chmod +x ./kubectl


5.3 Move the kubectl to different folder and add it to the path

mkdir -p $HOME/bin && cp ./kubectl $HOME/bin/kubectl && export PATH=$PATH:$HOME/bin

5.4 (Optional) Add the $HOME/bin path to your shell initialization file so that it is configured when you open a shell.

echo 'export PATH=$PATH:$HOME/bin' >> ~/.bashrc


5.5 Verify kubectl

kubectl version --short --client


Step 6 : View Resources using kubectl

kubectl get nodes -o wide



To get the pods running in the cluster

kubectl get pods --all-namespaces -o wide



Step 9 : Delete EKS Cluster

If you do not want to use the EKS cluster then it is recommended to delete the cluster to avoid any charges.

eksctl delete cluster --name test-cluster

====

https://helm.sh/docs/intro/quickstart/#install-an-example-chart

# Commands

\# helm list  <br />
\# helm repo add bitnami https://charts.bitnami.com/bitnami  <br />
\# helm search repo bitnami  <br />
\# helm repo update      <br />
\# helm install mydb bitnami/mysql --generate-name #install mysql chart  <br />
\# helm install --ns teamtwo mydb bitnami/mysql  <br />
\# helm search repo mysql  <br />
\# helm remove repo mysql   <br />
\# helm repo list  <br />





