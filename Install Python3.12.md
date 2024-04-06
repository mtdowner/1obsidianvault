---
Type:
---
[[Install Python3.12]]
```bash
apt update && apt upgrade -y
apt install software-properties-common -y
add-apt-repository ppa:deadsnakes/ppa

apt update
apt install python3.12

python3.12 --version
# 3.12.0

curl -sS https://bootstrap.pypa.io/get-pip.py | python3.12 
- [ ] - [ ] 

pip3.12 -V
# pip 23.2.1 from /usr/local/lib/python3.12/site-packages/pip (python 3.12)
```
