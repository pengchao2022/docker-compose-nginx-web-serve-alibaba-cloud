# Docker-compose-web-server-alibaba-cloud

In this tutorial, I will use a standalone alibaba ECS server to deploy a website including frontend, backend, database.

## Usage

- As we know, docker hub was blocked in China, so I need to configure Docker Hub image accelerator on my ECS server.
  
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
- This is a container environment, on your ECS server you need to install

   - docker
   ```shell
   sudo apt install docker.io -y
   sudo usermod -aG docker ecs-user
   newgrp docker
   ```
   - docker-compose
   ```shell
   sudo apt install docker-compose -y
   ```

   

