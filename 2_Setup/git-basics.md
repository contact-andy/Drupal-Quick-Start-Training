# Git Installation and Setup Guide

This guide provides step-by-step instructions for installing Git and configuring it for use in your projects.

---

## 1. Download and Install Git

### **Windows**
1. Go to the [official Git website](https://git-scm.com/downloads).
2. Click on **Windows** to download the installer.
3. Run the downloaded `.exe` file.
4. Follow the installation wizard:
   - Choose the default editor (recommended: VS Code or Nano).
   - Keep other options as default unless needed.
5. Click **Finish** to complete the installation.

### **MacOS**
1. Open **Terminal**.
2. Run the following command:
   ```sh
   git --version
   ```
3. If Git is not installed, install it using Homebrew:
   ```sh
   brew install git
   ```
4. Verify the installation:
   ```sh
   git --version
   ```

### **Linux (Ubuntu/Debian)**
1. Open a terminal.
2. Update package lists:
   ```sh
   sudo apt update
   ```
3. Install Git:
   ```sh
   sudo apt install git -y
   ```
4. Verify installation:
   ```sh
   git --version
   ```

### **Linux (CentOS/RHEL)**
1. Open a terminal.
2. Install Git using:
   ```sh
   sudo yum install git -y
   ```
3. Verify installation:
   ```sh
   git --version
   ```

---

## 2. Configure Git

After installing Git, set up your user information:

### **Set Your Name and Email**
1. Open a terminal and run:
   ```sh
   git config --global user.name "Your Name"
   git config --global user.email "your.email@example.com"
   ```
2. Confirm your settings:
   ```sh
   git config --list
   ```

### **Set Up SSH Authentication (Optional)**
For secure communication with remote repositories:
1. Generate an SSH key:
   ```sh
   ssh-keygen -t rsa -b 4096 -C "your.email@example.com"
   ```
2. Add the key to the SSH agent:
   ```sh
   eval "$(ssh-agent -s)"
   ssh-add ~/.ssh/id_rsa
   ```
3. Copy the key:
   ```sh
   cat ~/.ssh/id_rsa.pub
   ```
4. Add it to your GitHub/GitLab account under **SSH Keys**.

---

## 3. Verify Installation
To check if Git is working, run:
```sh
git --version
```
