# Setup

1. Install necessary dependencies:
```
sudo apt-get update
sudo apt-get install virtualbox curl
```
These commands update the packages available on Ubuntu and then install the necessary dependencies to run Minikube: VirtualBox and curl.

2. Download and install Minikube:
```
curl -LO https://storage.googleapis.com/minikube/releases/latest/minikube-linux-amd64
sudo install minikube-linux-amd64 /usr/local/bin/minikube
```
The first command downloads the Minikube executable file for Linux. The second command installs it in the /usr/local/bin directory so that it can be executed from anywhere in the system.

3. Download and install Kubectl:
```
curl -LO "https://dl.k8s.io/release/$(curl -L -s https://dl.k8s.io/release/stable.txt)/bin/linux/amd64/kubectl"
sudo install kubectl /usr/local/bin/kubectl
```
These commands download the latest stable version of Kubectl for Linux and install it in the /usr/local/bin directory so that it can be executed from anywhere in the system.

4. Start Minikube:
```
minikube start
```
This command starts Minikube with default configuration.

5. Verify the cluster status:
```
kubectl cluster-info
```
This command verifies that the Minikube cluster is up and running and displays relevant information about the cluster.

6. Configure Kubectl to use Minikube cluster:
```
kubectl config use-context minikube
```
This command sets the context of Kubectl to the Minikube cluster so that Kubernetes commands are executed on that cluster.


