# Git Installation and Setup Guide

This guide provides step-by-step instructions for installing Git.

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

## 2. Verify Installation
To check if Git is working, run:
```sh
git --version
```
