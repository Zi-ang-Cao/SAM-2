# Installation Guide
> SAM2 requires CUDA 12.1 and PyTorch 2.3.1. CUDA 11.8 is not working at all!

See how to install `cuDNN` for both CUDA 11.8 and 12.1 in the [verfied tutorial](https://gist.github.com/garg-aayush/156ec6ddda3d62e2c0ddad00b7e66956#3-install-cudnn-library).
Then, add the following into your `~/.zshrc` or `~/.bashrc`:
```Shell
# ### Specify the cuda 11.8
# export PATH=/usr/local/cuda-11.8/bin:$PATH
# export LD_LIBRARY_PATH=/usr/local/cuda-11.8/lib64:$LD_LIBRARY_PATH
# export LD_LIBRARY_PATH=/usr/local/cuda-11.8/extras/CUPTI/lib64:$LD_LIBRARY_PATH

### Specify the cuda 12.1
export PATH=/usr/local/cuda-12.1/bin:$PATH
export LD_LIBRARY_PATH=/usr/local/cuda-11.8/lib64:$LD_LIBRARY_PATH
export LD_LIBRARY_PATH=/usr/local/cuda-11.8/extras/CUPTI/lib64:$LD_LIBRARY_PATH
```


```Shell
conda create -n SAM2 python=3.10
conda activate SAM2

# It requires CUDA 12.1 !
pip install torch==2.3.1 torchvision==0.18.1 torchaudio==2.3.1 --index-url https://download.pytorch.org/whl/cu121
pip install --no-build-isolation -e .
```
