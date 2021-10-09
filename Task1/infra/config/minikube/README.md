# First enable virtualization at BIOS

# Update Ubuntu repo
sudo apt update

# make sure to install the following required packages
sudo apt install -y apt-transport-https curl

# Install VirtualBox
sudo apt install -y virtualbox virtualbox-ext-pack

# Install Minikube
wget https://storage.googleapis.com/minikube/releases/latest/minikube-linux-amd64
sudo cp minikube-linux-amd64 /usr/local/bin/minikube
sudo chmod 755 /usr/local/bin/minikube

sudo minikube version

# Install Kubectl
curl -LO https://storage.googleapis.com/kubernetes-release/release/`curl -s https://storage.googleapis.com/kubernetes-release/release/stable.txt`/bin/linux/amd64/kubectl

sudo chmod +x ./kubectl
sudo mv ./kubectl /usr/local/bin/kubectl
kubectl version

# Start minikube using 3 nodes
<<<<<<< HEAD
minikube start --nodes 2

or add node

minikube node add
=======
minikube start --nodes 3
>>>>>>> 7f3a4b1f365acda422aefd61db756224b8346490

or add node
minikube node add

# check K8S Cluster
kubectl get nodes

