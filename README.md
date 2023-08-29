# Minikube


## 安裝指令
1. 進入minikube網站
https://minikube.sigs.k8s.io/docs/start/

2. 在Installation頁面，根據自身環境點選按鈕
curl -LO https://storage.googleapis.com/minikube/releases/latest/minikube-linux-amd64
sudo install minikube-linux-amd64 /usr/local/bin/minikube

3. 確認 Minikube 是否成功安
minikube version

(輸出結果)
minikube version: v1.31.1

4. sudo chmode 666 /var/run/docker.sock

5. 確認 Kubectl 是否成功安裝
kubectl version --short

(輸出結果)
Client Version: v1.27.2
Kustomize Version: v5.0.1
Server Version: v1.27.4

6. 使用 Minikube 建立 Kubernetes Cluster
minikube start --driver=docker --memory 4096

7. minikube start

8. 確認 kubectl 是否能與 Cluster 溝通
kubectl cluster-info

(輸出結果)
Kubernetes control plane is running at https://127.0.0.1:53266
CoreDNS is running at https://127.0.0.1:53266/api/v1/namespaces/kube-system/services/kube-dns:dns/proxy

10. kubectl run nginx --image=nginx --restart=Never
(輸出結果)
pod/nginx created

11. kubectl get pods
(輸出結果)
NAME    READY   STATUS    RESTARTS   AGE
nginx   1/1     Running   0          39s

12. kubectl port-forward nginx 8080:80
8080:80: 將主機 Port 8080 的流量轉移到 Container 的 Port 80

11.在瀏覽器輸入http://127.0.0.1:8080/
