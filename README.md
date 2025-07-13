# minikube-project
# K8s Minikube Setup Commands on Rocky Linux9

```bash
# 1. Install Yum utils
sudo yum install -y yum-utils

# 2. Add Docker repository
sudo yum-config-manager --add-repo https://download.docker.com/linux/centos/docker-ce.repo

# 3. Install Docker and Docker Compose plugin
sudo yum install docker-ce docker-ce-cli containerd.io docker-compose-plugin

# 4. Start Docker
sudo systemctl start docker

# 5. Download and install Minikube RPM
curl -LO https://storage.googleapis.com/minikube/releases/latest/minikube-latest.x86_64.rpm
sudo rpm -Uvh minikube-latest.x86_64.rpm

# 6. Start Minikube
minikube start

# Additional helpful kubectl and minikube commands:
kubectl get pods
kubectl get nodes
kubectl get svc
kubectl create deployment <name> --image=<image>
kubectl expose deployment <name> --type=NodePort --port=80
minikube service <service-name>
minikube dashboard
minikube dashboard --url <to get the link for your dashboard>
kubectl apply -f <manifest.yaml>
kubectl delete -f <manifest.yaml>
kubectl logs <pod-name>
kubectl describe pod <pod-name>
```
