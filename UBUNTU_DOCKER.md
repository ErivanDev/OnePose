Run Ubuntu (novnc) with nvidia driver

```
sudo docker run --gpus all -p 6080:80 -v /dev/shm:/dev/shm dorowu/ubuntu-desktop-lxde-vnc
```
Access terminal remotely from host

```
sudo docker exec -i -t {CONTAINER_ID} /bin/bash
```

Install Anaconda

```
wget https://repo.anaconda.com/miniconda/Miniconda3-py37_4.8.2-Linux-x86_64.sh
```

```
chmod +x Miniconda3-py37_4.8.2-Linux-x86_64.sh
```

```
bash ./Miniconda3-py37_4.8.2-Linux-x86_64.sh -b -f -p /usr/local
```

```
python

import sys
sys.path.append('/usr/local/lib/python3.7/site-packages/')
```

Install GIT and GCC

```
apt update 

apt install -y git gcc
```

Clone Repository

```
git clone --branch ubuntu_docker https://github.com/ErivanDev/OnePose.git

cd OnePose
```

Create ENV

```
conda env create -f environment.yaml
```

