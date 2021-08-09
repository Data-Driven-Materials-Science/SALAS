# Satellite Detection Framework Installation Guide:
Note:
 * To properly install and run the code, there are a couple requirements. This code must be run on a native Linux or mac environment, there must be access to a GPU, and that GPU must not be an NVIDIA Tesla K40. There may be other GPUs that do not work, but that one definitively does not. To perform the installation, you must have access to a terminal AND have sudo permission. Additionally, the example code is stored as a jupyter notebook. 
 * This installation process is NOT complete. 
 * There appears to be an issue with cuda being incompatible such that upon final installation, it doesn't run
## First you want to install anaconda and git if you don’t have it
```bash
wget https://repo.continuum.io/archive/Anaconda3-2020.11-Linux-x86_64.sh
```
```bash
bash Anaconda3-2020.11-Linux-x86_64.sh
```
```bash
conda install -c anaconda git
```

## Clone git repository
```bash
https://github.com/Data-Driven-Materials-Science/SALAS
```
```bash
cd SALAS
```

## Setup Virtual Environment
```bash
python3 -m venv salas_env
```
```bash
source salas_env/bin/activate
```

## Install Requirements File
```bash
pip install wheel
```
```bash
pip install -r requirements.txt
```

## Installing additional requirements not accounted for
```bash
sudo apt install build-essential
```
```bash
conda install gcc_linux-64 
```
```bash
sudo apt-get install python3.8-dev
```

## Installing COCO Python API
```bash
pip install pycocotools
```

### Sometimes, the above doesn’t work so if that is the case, try the following
```bash
pip install git+https://github.com/cocodataset/cocoapi.git#subdirectory=PythonAPI
```

## Installing PyTorch and TorchVision
```bash
pip install torch==1.5.0+cu101 torchvision==0.6.0+cu101 -f https://download.pytorch.org/whl/torch_stable.html
```

### Sometimes, the above doesn’t work. If you recieve the error "[Errno 28] No space left on device", try the following
```bash
TMPDIR=/var/tmp pip install torch torchvision torchaudio
```

## Installing Requirements
```bash
python -m pip install -U scikit-image
```
```bash
pip install seaborn
```
```bash
pip install imantics 
```
```bash
python -m pip install -U scikit-image
```
## Installing Detectron2
```bash
python -m pip install detectron2 -f \ https://dl.fbaipublicfiles.com/detectron2/wheels/cu102/torch1.8/index.html
```

### Sometimes, the above doesn’t work so if that is the case, try the following
```bash
python -m pip install 'git+https://github.com/facebookresearch/detectron2.git'
```

### Installing AMPIS
```bash
pip install -e .
```

### Open a python window in the terminal and try the following. If there are no errors, installation was completed properly
```bash
import pycocotools
import torch
import detectron2
import ampis
```
