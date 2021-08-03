# Docker-note
## 安裝Docker
### 1. 載舊版Docker，如果沒有舊版Docker不用做此步驟
` $ sudo apt-get remove docker docker-engine docker.io containerd runc`
### 2. 更新與建設環境
####   **apt的更新**
` $  sudo apt-get update`
####   **apt使用http存儲的權限**
` $ sudo apt-get install apt-transport-https ca-certificates curl gnupg lsb-release`
####   **Docker 密鑰**
` $ curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo gpg --dearmor -o /usr/share/keyrings/docker-archive-keyring.gpg `
####   **Docker 存儲庫**
` $ echo \
  "deb [arch=amd64 signed-by=/usr/share/keyrings/docker-archive-keyring.gpg] https://download.docker.com/linux/ubuntu \
  $(lsb_release -cs) stable" | sudo tee /etc/apt/sources.list.d/docker.list > /dev/null`
### 3. **Docker 安裝**
` $ sudo apt-get install docker-ce docker-ce-cli containerd.io`
## Docker 常見使用
### 列出執行中Docker的容器
` $ docker ps `
### 列出所有Docker的容器
` $ docker ps -a`
### 啟動Docker容器
` $ docker start 容器(CONTAINER) ID`
### 建立Docker容器
` $ docker run 建立動作`
### 執行Docker容器
` $ docker run 執行動作`
## Docker tenserflow jupyter
### 檢查顯示卡
` $ lspci | grep -i nvidia`
### 驗證顯示卡
` $ docker run --gpus all --rm nvidia/cuda nvidia-smi`
### 安裝tensorflow
` $ docker pull tensorflow/tensorflow:latest-gpu-jupyter `
` $ docker pull jupyter/tensorflow-notebook `






