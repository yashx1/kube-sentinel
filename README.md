# kube-sentinel

Let's setup kube cluster monitorig, alerting and logging over #kubernetes cluster provided by [Civo](https://www.civo.com/) team.   
Join the #Kube100 beta by #Civo to get free credit to test-drive the world’s first k3s-powered, managed Kubernetes service


**Host machine :** Ubuntu 20.04.1 LTS

**Kube cluster :** 3 node cluster by [Civo](https://www.civo.com/)


## checkout kube-sentinel :

>$ git clone https://github.com/yashx1/kube-sentinel.git  
>$ cd kube-sentinel


## install [kubectl](https://kubernetes.io/docs/tasks/tools/install-kubectl/)

>$ sudo apt-get update && sudo apt-get install -y apt-transport-https gnupg2  
>$ curl -s https://packages.cloud.google.com/apt/doc/apt-key.gpg | sudo apt-key add -  
>$ echo "deb https://apt.kubernetes.io/ kubernetes-xenial main" | sudo tee -a /etc/apt/sources.list.d/kubernetes.list  
>$ sudo apt-get update  
>$ sudo apt-get install -y kubectl


## verify kubectl installation and version

>$ kubectl version  
`Client Version: version.Info{Major:"1", Minor:"19", GitVersion:"v1.19.0", GitCommit:"e19964183377d0ec2052d1f1fa930c4d7575bd50", GitTreeState:"clean", BuildDate:"2020-08-26T14:30:33Z", GoVersion:"go1.15", Compiler:"gc", Platform:"linux/amd64"}
Server Version: version.Info{Major:"1", Minor:"18", GitVersion:"v1.18.6+k3s1", GitCommit:"6f56fa1d68a5a48b8b6fdefa8eb7ead2015a4b3a", GitTreeState:"clean", BuildDate:"2020-07-16T20:46:15Z", GoVersion:"go1.13.11", Compiler:"gc", Platform:"linux/amd64"}
`

## install [Helm](https://helm.sh/docs/intro/install/)

>$ curl -fsSL -o get_helm.sh https://raw.githubusercontent.com/helm/helm/master/scripts/get-helm-3  
>$ chmod 700 get_helm.sh  
>$ ./get_helm.sh 


## verify helm installation and version

>$ helm version   
`version.BuildInfo{Version:"v3.3.0", GitCommit:"8a4aeec08d67a7b84472007529e8097ec3742105", GitTreeState:"dirty", GoVersion:"go1.14.7"}`


## add kube config 

Download kube config file from Civo dashboard and save it as _~/.kube/config_ -
![alt text](https://github.com/yashx1/kube-sentinel/raw/master/civo-dashboard.png "civo dashboard")
