# Drupal 10.4.5 Installation Guide

This guide provides step-by-step instructions to install **Drupal 10.4.5** using two methods:

✅ **Method 1**: Manual installation using **ZIP package**  
✅ **Method 2**: Recommended **Composer installation** (for development)  

---

## 🚀 Method 1: Installing Drupal 10.4.5 Using ZIP Package

### Step 1: Download Drupal  
1. Visit the official [Drupal website](https://www.drupal.org/download).  
2. Download the **Drupal 10.4.5 ZIP** package.  
3. Extract the ZIP file to your local web server directory:
   - **XAMPP**: `htdocs/drupal`
   - **MAMP**: `htdocs/drupal`
   - **WAMP**: `www/drupal`

### Step 2: Set Up the Database  
1. Open **phpMyAdmin** (`http://localhost/phpmyadmin`).  
2. Click **New** and create a database named `drupal_training`.  
3. Set the database collation to **utf8_general_ci**.  

### Step 3: Configure Apache & PHP Settings  
1. Ensure **Apache** and **MySQL** are running in **XAMPP**.  
2. Increase **max_execution_time** and **memory_limit** in `php.ini`.  
3. Enable necessary PHP extensions:
   - `intl`
   - `gd`
   - `pdo_mysql`

### Step 4: Install Drupal via Web Installer  
1. Open a browser and go to `http://localhost/drupal`.  
2. Select **Standard Installation**.  
3. Choose **English** as the language.  
4. Enter the database details:  
   - **Database Name**: `drupal_training`  
   - **Username**: `root`  
   - **Password**: *(leave empty if using XAMPP/WAMP default settings)*  
5. Click **Save and Continue**.  
6. After installation, set up the **site name, admin username, and password**.  

---

## ⚡ Method 2: Installing Drupal 10.4.5 Using Composer (Recommended)

This method is recommended for **developers** because it provides easy updates and dependency management.  

### Step 1: Install Required Tools  
Ensure you have:  
✅ **Composer** → Download from [getcomposer.org](https://getcomposer.org/)  
✅ **Git** → Download from [git-scm.com](https://git-scm.com/)  
✅ **PHP 8.1+** installed  

Verify installation by running:  
```sh
composer -V
php -v
git --version


## Step 2: Create a New Drupal Project

1. Open **Command Prompt** (Windows) or **Terminal** (Mac/Linux).
2. Navigate to your web server directory (e.g., `htdocs` for XAMPP):
    ```bash
    cd /path/to/htdocs
    ```
3. Run the following command to install Drupal:
    ```bash
    composer create-project drupal/recommended-project drupal_training
    ```
4. Once the installation completes, go into the project folder:
    ```bash
    cd drupal_training
    ```

---

## Step 3: Set Up Apache Virtual Host (Optional, Recommended for Local Development)

1. Open Apache’s `httpd-vhosts.conf` file.
2. Add the following virtual host entry:
    ```apache
    <VirtualHost *:80>
        DocumentRoot "C:/xampp/htdocs/drupal_training/web"
        ServerName drupal.local
        <Directory "C:/xampp/htdocs/drupal_training/web">
            AllowOverride All
            Require all granted
        </Directory>
    </VirtualHost>
    ```
3. Restart Apache.

---

## Step 4: Set Up the Database

1. Open **phpMyAdmin** (`http://localhost/phpmyadmin`).
2. Create a database `drupal_training`.

---

## Step 5: Install Drupal

1. Run the installation script:
    ```bash
    php -S localhost:8080 -t web
    ```
2. Open `http://localhost:8080` in a browser.
3. Follow the Drupal installation wizard, enter database details, and set up the admin account.
