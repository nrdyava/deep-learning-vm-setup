# Deep Learning VM Setup Guide

This guide provides step-by-step instructions to set up a Virtual Machine (VM) for deep learning tasks.

## Prerequisites

Before you begin, ensure you have the following:
- An active Google Cloud Platform (GCP) account.
- Basic knowledge of command-line operations.
- SSH client installed on your local machine.

## Step 1: Create a VM Instance

1. **Navigate to the GCP Console:**
   Go to the [Google Cloud Console](https://console.cloud.google.com/).

2. **Create a New Project:**
   If you don't already have a project, create one.

3. **Open the VM Instances Page:**
   Go to the Compute Engine section and click on **VM instances**.

4. **Create a New Instance:**
   - Click on **Create Instance**.
   - Name your instance.
   - Choose the region and zone that best suits your needs.

5. **Configure the Instance:**
   - **Machine Configuration:** Select the machine type. For deep learning, it's recommended to choose a machine with a GPU, such as `n1-standard-4` with a `NVIDIA Tesla T4`.
   - **Boot Disk:** Click on **Change** to select an appropriate image. You can use a Deep Learning VM image provided by GCP. Select an image like `Deep Learning on Ubuntu` and choose the framework you prefer (TensorFlow, PyTorch, etc.).

6. **Firewall Settings:**
   - Allow HTTP and HTTPS traffic if needed.
   - Configure any other necessary firewall rules.

7. **Create the VM:**
   - Click on **Create** to launch the VM instance.

## Step 2: Connect to the VM

1. **SSH into the VM:**
   - Use the SSH button in the GCP console or connect via your terminal:
     ```sh
     gcloud compute ssh [INSTANCE_NAME]
     ```

## Step 3: Set Up the Environment

1. **Update Packages:**
   ```sh
   sudo apt update
   sudo apt upgrade
   ```
   ```sh
   sudo apt update && sudo apt upgrade -y
   ```
   ```sh
   sudo apt update && sudo apt upgrade -y
   ```
   ```sh
   sudo apt update && sudo apt upgrade -y
   ```
   ```sh
   sudo apt update && sudo apt upgrade -y
   ```
   ```sh
   sudo apt update && sudo apt upgrade -y
   ```
