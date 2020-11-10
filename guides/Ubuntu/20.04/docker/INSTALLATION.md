# Docker Installation

Reference: https://docs.docker.com/engine/install/ubuntu/

Estimated Time: 5 minutes

## Requirements
- Root access to server
- Packages updated (`apt -y update`)

## Steps
1. Install dependencies
```bash
sudo apt-get install \
    apt-transport-https \
    ca-certificates \
    curl \
    gnupg-agent \
    software-properties-common
```

2. Setup the official docker repositories
```bash
curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo apt-key add -
sudo add-apt-repository \
   "deb [arch=amd64] https://download.docker.com/linux/ubuntu \
   $(lsb_release -cs) \
   stable"
```

3. Install docker
```bash
sudo apt-get update
sudo apt-get install docker-ce docker-ce-cli containerd.io
```


4. Setup docker service to start on boot

```bash
sudo systemctl enable --now docker
```

5. (Optional) Setup docker group, and add current user for daemon access
```bash
sudo groupadd docker
sudo usermod -aG docker $USER
newgrp docker
```

6. Test Docker Install

```bash
docker run --rm hello-world
```
