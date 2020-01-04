# Data Science Environment Setup

Installing on Ubuntu 18.04 LTS (Windows 10)

## Install Python 3 and Compilers
```
sudo apt update && upgrade
sudo apt install python3 python3-pip ipython3
sudo apt-get install build-essential python3-dev python3-pip python3-setuptools python3-wheel python3-cffi libcairo2 libpango-1.0-0 libpangocairo-1.0-0 libgdk-pixbuf2.0-0 libffi-dev shared-mime-info
```
## Setup Virtual Environment
```
sudo apt install virtualenv
pip3 install virtualenv
virtualenv venv --python=python3  
```

## Activate Virtual Environment
```
source /home/cstorm125/venv/bin/activate
```

## Replicate Kaggle Kernel Libraries (as of 2020/01/04)
Install line by line the libraries `pip freeze > requirements.txt` from Kaggle kernel
```
cat requirements.txt | xargs -n 1 pip install
```