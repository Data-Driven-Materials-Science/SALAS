# Satellite Detection Framework Installation Guide:
Note:
To properly install and run the code, there are a couple requirements. This code must be run on a native Linux or mac environment, there must be access to a GPU, and that GPU must not be an NVIDIA Tesla K40. There may be other GPUs that do not work, but that one definitively does not. To perform the installation, you must have access to a terminal AND have sudo permission. Additionally, the example code is stored as a jupyter notebook. 
First you want to install anaconda and git if you don’t have it
 * wget https://repo.continuum.io/archive/Anaconda3-2020.11-Linux-x86_64.sh
 * bash Anaconda3-2020.11-Linux-x86_64.sh
 * conda install -c anaconda git

Clone git repository
 * git clone https://github.com/rccohn/AMPIS.git
 * cd AMPIS
Setup Virtual Environment
 * python3 -m venv ampis_env
 * source ampis_env/bin/activate
Install Requirements File
 * pip install wheel
 * pip install -r requirements.txt
Installing additional requirements not accounted for
 * sudo apt install build-essential
 * conda install gcc_linux-64 
 * sudo apt-get install python3.8-dev
Installing COCO Python API
 * pip install pycocotools
Sometimes, the above doesn’t work so if that is the case, try the following
 * pip install git+https://github.com/cocodataset/cocoapi.git#subdirectory=PythonAPI
Installing PyTorch and TorchVision
 * pip install torch==1.5.0+cu101 torchvision==0.6.0+cu101 -f https://download.pytorch.org/whl/torch_stable.html
Sometimes, the above doesn’t work so if that is the case, try the following
 * TMPDIR=/var/tmp pip install torch torchvision torchaudio
Installing Requirements
 * python -m pip install -U scikit-image
 * pip install seaborn
Installing Detectron2
 * python -m pip install detectron2 -f \ https://dl.fbaipublicfiles.com/detectron2/wheels/cu102/torch1.8/index.html
Sometimes, the above doesn’t work so if that is the case, try the following
 * python -m pip install 'git+https://github.com/facebookresearch/detectron2.git'
Installing AMPIS
 * pip install -e .
Verifying installation
Open a python window in the terminal and try the following. If there are no errors, installation was completed properly

import pycocotools
import torch
import detectron2
import ampis
