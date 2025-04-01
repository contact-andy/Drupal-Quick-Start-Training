# Composer Setup for Drupal

## Introduction

Composer is a dependency manager for PHP that allows you to manage Drupal core, contributed modules, and themes efficiently. This guide will walk you through installing Composer and using it to manage Drupal packages.

---

## Install Composer

### Windows

1. Download the Composer Windows Installer from [getcomposer.org](https://getcomposer.org).
2. Run the installer and follow the setup wizard.
3. Verify the installation by running the following command in **Command Prompt (CMD)**:
    ```bash
    composer -V
    ```

### macOS/Linux

1. Open a terminal and run the following command to install Composer globally:
    ```bash
    curl -sS https://getcomposer.org/installer | php
    sudo mv composer.phar /usr/local/bin/composer
    ```
2. Verify the installation:
    ```bash
    composer -V
    ```

---
