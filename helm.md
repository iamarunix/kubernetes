#  What is Helm 

It is like a package manager EXE in Windows and YUM in Linux 
It is a package manager in Linux that container lots of YAML files 

# Install Helm

  - curl -fsSL -o get_helm.sh https://raw.githubusercontent.com/helm/helm/master/scripts/get-helm-3
  - chmod 700 get_helm.sh
  - ./get_helm.sh
  - helm version

    helm create helloworld
    change SVC to nodeport in values.yaml
    hellom install helloworld 





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

PS1='\[\033[0;32m\]\u@\h:\[\033[0;34m\]\w\[\033[0m\]\$ '





