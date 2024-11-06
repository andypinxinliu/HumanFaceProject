# 📝 Release Plans

- [] Project Page
- [] Inference codes and pretrained Weights
- [] Training scripts
- [] Plug and play GaussianStyle to any 3D Gaussian Head Models with new Technical Report


# ⚒️ Installation

## Build Environtment

We Recommend a python version `==3.8` and cuda version `==12.2`. Then build environment as follows:

```shell
# [Optional] Create a virtual env
git clone https://github.com/andypinxinliu/HumanFaceProject.git
conda create -n gaussianstyle python==3.9
conda activate gaussianstyle
# Install ffmpeg for media processing and libstdcxx-ng for rendering
conda install -c conda-forge libstdcxx-ng ffmpeg
# Install with pip:
pip install -r ./scripts/GaussianStyle/requirements.txt
pip install 'git+https://github.com/facebookresearch/pytorch3d.git@stable'
# install stylegan modules
cd ./scripts/GaussianStyle/xxx
pip install -e .
# install gaussian splatting

cd path/to/gaussian-splatting

# Modify "submodules/diff-gaussian-rasterization/cuda_rasterizer/config.h", by changing "NUM_CHANNELS 3" to "NUM_CHANNELS 32" in "diff-gaussian-rasterization/cuda_rasterizer/config.h".

pip install submodules/diff-gaussian-rasterization
pip install submodules/simple-knn

```

# 🚀 Quick Start