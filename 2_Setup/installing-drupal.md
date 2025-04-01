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
