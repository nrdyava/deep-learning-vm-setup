# Deep Learning VM Setup Guide

This guide provides step-by-step instructions to set up a Virtual Machine (VM) for deep learning tasks.

## Set Up the Environment

1. **Update Packages:**
   ```sh
   sudo apt update
   sudo apt upgrade
   ```
   ```sh
   lspci | grep -i nvidia
   ```
   ```sh
   sudo apt install build-essential
   ```
   ```sh
   sudo apt install linux-headers-$(uname -r)
   ```
    ```sh
   sudo apt-get install dkms
   ```
   ```sh
   wget https://developer.download.nvidia.com/compute/cuda/11.8.0/local_installers/cuda_11.8.0_520.61.05_linux.run
   sudo sh cuda_11.8.0_520.61.05_linux.run
   ```
   ```sh
   sudo ln -snf /usr/local/cuda-11.8 /usr/local/cuda
   ```
   ```sh
   sudo reboot
   ```
   ```sh
   wget https://developer.download.nvidia.com/compute/cudnn/9.2.1/local_installers/cudnn-local-repo-ubuntu2204-9.2.1_1.0-1_amd64.deb
   sudo dpkg -i cudnn-local-repo-ubuntu2204-9.2.1_1.0-1_amd64.deb
   sudo cp /var/cudnn-local-repo-ubuntu2204-9.2.1/cudnn-*-keyring.gpg /usr/share/keyrings/
   sudo apt-get update
   sudo apt-get -y install cudnn-cuda-11
   ```
   ```sh
   export CUDA_HOME=/usr/local/cuda-11.8
   export LD_LIBRARY_PATH=${CUDA_HOME}/lib64
   export PATH=${CUDA_HOME}/bin:${PATH}
   ```
   ```sh
   source ~/.bashrc
   ```
   ```sh
   nvcc -V
   nvidia-smi
   ```
