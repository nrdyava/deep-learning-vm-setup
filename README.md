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
   sudo apt update && sudo apt upgrade -y
   ```
