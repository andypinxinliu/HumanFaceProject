# 📝 Release Plans

- [x] Project Page
- [ ] Presentation video.
- [ ] Inference codes
- [ ] Pretrained models
- [ ] Training scripts
- [ ] New Technical Report
- [ ] Plug and play GaussianStyle to any 3D Gaussian Head Models

# ⚒️ Installation

## Build Environtment

We Recommend a python version `==3.9` and cuda version `>=2.0.0`. Then build environment as follows:

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