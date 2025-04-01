# Pre-configured Project Files for Drupal Quick Start Training

## Overview

This guide provides the necessary files and instructions to quickly set up Drupal 10.4.5 for training purposes. The pre-configured project files include the Drupal 10.4.5 ZIP archive and the steps for installation. This setup is ideal for beginners who want to get started with Drupal without worrying about configuration issues.

---

## Files Included

- **Drupal 10.4.5 ZIP Package**: A pre-configured ZIP archive containing the full Drupal 10.4.5 package.
- [Download Drupal 10.4.5 Package](https://ftp.drupal.org/files/projects/drupal-10.4.5.zip)

---

## Installation Steps

Follow the instructions below to install Drupal 10.4.5 using the provided ZIP package.

### Step 1: Download and Extract the Drupal ZIP Package

1. Download the **Drupal 10.4.5 ZIP** file from the provided link.
2. Extract the ZIP file to your local web server directory:
   - **XAMPP**: `htdocs/drupal`
   - **MAMP**: `htdocs/drupal`
   - **WAMP**: `www/drupal`

### Step 2: Set Up the Database

1. Open **phpMyAdmin** by navigating to `http://localhost/phpmyadmin` in your browser.
2. Create a new database named **drupal_training**.
3. Set the database collation to **utf8_general_ci** for compatibility.

### Step 3: Configure Apache and PHP Settings

1. Ensure that **Apache** and **MySQL** are running on your local server (e.g., XAMPP, MAMP, WAMP).
2. Increase the following values in your `php.ini` file:
   - `max_execution_time`: 300
   - `memory_limit`: 256M
3. Enable necessary PHP extensions:
   - `intl`
   - `gd`
   - `pdo_mysql`

### Step 4: Run the Drupal Installation

1. Open your browser and navigate to `http://localhost/drupal`.
2. Select **Standard Installation**.
3. Choose **English** as the language.
4. Enter the database details:
   - Database Name: `drupal_training`
   - Username: `root`
   - Password: (Leave empty if using default XAMPP/WAMP settings)
5. Click **Save and Continue**.
6. Once the installation is complete, enter the site name, admin username, and password.

### Step 5: Finalize Setup

1. After installation, log in with the admin account credentials you set during the installation process.
2. You now have a fully functional Drupal 10.4.5 site ready for training.

---

## Conclusion

With these pre-configured project files, you can quickly set up Drupal 10.4.5 and begin your training. The installation steps are simple, and this setup ensures that you can focus on learning Drupal rather than spending time on configuration. Happy learning!

