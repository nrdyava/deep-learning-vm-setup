# Deep Learning VM Setup Guide

This guide provides step-by-step instructions to set up a Virtual Machine (VM) for deep learning tasks.

## Set Up the Environment

**Update Packages:**
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
   wget https://developer.download.nvidia.com/compute/cuda/12.4.0/local_installers/cuda_12.4.0_550.54.14_linux.run
   sudo sh cuda_12.4.0_550.54.14_linux.run
   ```
   ```sh
   sudo ln -snf /usr/local/cuda-12.4 /usr/local/cuda
   ```
   ```sh
   sudo reboot
   ```
   ```sh
   wget https://developer.download.nvidia.com/compute/cudnn/9.2.1/local_installers/cudnn-local-repo-ubuntu2204-9.2.1_1.0-1_amd64.deb
   sudo dpkg -i cudnn-local-repo-ubuntu2204-9.2.1_1.0-1_amd64.deb
   sudo cp /var/cudnn-local-repo-ubuntu2204-9.2.1/cudnn-*-keyring.gpg /usr/share/keyrings/
   sudo apt-get update
   sudo apt-get -y install cudnn-cuda-12
   ```
   ```sh
   export CUDA_HOME=/usr/local/cuda-12.4
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

**Install Miniconda:**
   ```sh
   mkdir -p ~/miniconda3
   wget https://repo.anaconda.com/miniconda/Miniconda3-latest-Linux-x86_64.sh -O ~/miniconda3/miniconda.sh
   bash ~/miniconda3/miniconda.sh -b -u -p ~/miniconda3
   rm -rf ~/miniconda3/miniconda.sh
   ```
   ```sh
   ~/miniconda3/bin/conda init bash
   ```
