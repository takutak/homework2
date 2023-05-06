### インストール方法
! git clone 
%cd homework2
%mkdir checkpoints
%cd checkpoints
! wget https://datarelease.blob.core.windows.net/grit/models/grit_b_densecap_objectdet.pth
%cd ..

detectron2のインストールは面倒なので、ここでインストール
!python -m pip install pyyaml==5.1
import sys, os, distutils.core
!git clone 'https://github.com/facebookresearch/detectron2'
dist = distutils.core.run_setup("./detectron2/setup.py")
!python -m pip install {' '.join([f"'{x}'" for x in dist.install_requires])}
sys.path.insert(0, os.path.abspath('./detectron2'))


# 1. Installment

### 1.1 Download Pretrained Model
First cd in the project path, then download the pretrained model from grit.

```bash
cd [YOUR_PATH_TO_THIS_PROJECT]
mkdir checkpoints
cd checkpoints
wget -c https://datarelease.blob.core.windows.net/grit/models/grit_b_densecap_objectdet.pth
cd ..
```

### 1.2 Install Enviornment

Run

```
conda create -n -y vlog python=3.8
conda activate vlog
pip install -r requirements.txt
```
