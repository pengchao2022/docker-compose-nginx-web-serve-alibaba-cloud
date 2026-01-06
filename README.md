# Docker-compose-web-server-alibaba-cloud

In this tutorial, I will use a standalone alibaba ECS server to deploy a website including frontend, backend, database.

## Usage

- As we know, docker hub was block in China, so I need to configure Docker Hub image 

  accelerator on my ECS server.
  - run the scripts on my ubuntu ECS server
  ```shell
sudo mkdir -p /etc/docker
sudo tee /etc/docker/daemon.json <<-'EOF'
{
  "registry-mirrors": ["https://qshjcvem.mirror.aliyuncs.com"]
}
EOF
sudo systemctl daemon-reload
sudo systemctl restart docker
```


