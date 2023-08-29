# Minikube


## 安裝指令
1. 進入minikube網站
https://minikube.sigs.k8s.io/docs/start/

2. 在Installation頁面，根據自身環境點選按鈕
```
curl -LO https://storage.googleapis.com/minikube/releases/latest/minikube-linux-amd64
sudo install minikube-linux-amd64 /usr/local/bin/minikube
```

4. 確認 Minikube 是否成功安
```
minikube version
```

(輸出結果)  
minikube version: v1.31.1

5. 設定權限
```
sudo chmode 666 /var/run/docker.sock
```
6. 確認 Kubectl 是否成功安裝
```
kubectl version --short
```

(輸出結果)  
Client Version: v1.27.2
Kustomize Version: v5.0.1
Server Version: v1.27.4

7. 使用 Minikube 建立 Kubernetes Cluster
```
minikube start --driver=docker --memory 4096
```

8. 啟動！
```
minikube start
```

9. 確認 kubectl 是否能與 Cluster 溝通
```
kubectl cluster-info
```

(輸出結果)  
Kubernetes control plane is running at https://127.0.0.1:53266
CoreDNS is running at https://127.0.0.1:53266/api/v1/namespaces/kube-system/services/kube-dns:dns/proxy
