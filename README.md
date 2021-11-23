#Kubernetes

#history da aula 1
```bash
sudo apt-get update
echo   "deb [arch=$(dpkg --print-architecture) signed-by=/usr/share/keyrings/docker-archive-keyring.gpg] https://download.docker.com/linux/ubuntu $(lsb_release -cs) stable" | sudo tee /etc/apt/sources.list.d/docker.list > /dev/null
sudo apt-get update
sudo groupadd docker
sudo usermod -aG docker danilodorgam
sudo reboot now
docker run hello-world
curl -LO https://storage.googleapis.com/minikube/releases/latest/minikube_latest_amd64.deb
sudo dpkg -i minikube_latest_amd64.deb
minikube start
kubeclt get po -A
kubectl
sudo curl -fsSLo /usr/share/keyrings/kubernetes-archive-keyring.gpg https://packages.cloud.google.com/apt/doc/apt-key.gpg
echo "deb [signed-by=/usr/share/keyrings/kubernetes-archive-keyring.gpg] https://apt.kubernetes.io/ kubernetes-xenial main" | sudo tee /etc/apt/sources.list.d/kubernetes.list
sudo apt-get update
sudo apt-get install -y kubectl
kubectl
kubectl get po -A
minikube dashboard &
sudo service ufw status
sudo ufw status
kubectl proxy --address='0.0.0.0' --disable-filter=true
kubectl proxy --address='0.0.0.0' --disable-filter=true &
kubectl create deployment hello-minikube --image=k8s.gcr.io/echoserver:1.4
kubectl expose deployment hello-minikube --type=NodePort --8080
kubectl expose deployment hello-minikube --type=NodePort --port=8080
kubeclt get services hellow-minikube
kubectl get services hello-minikube
```