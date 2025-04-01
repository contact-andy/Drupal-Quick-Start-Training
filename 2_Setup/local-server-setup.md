```md
# 🖥 Local Server Setup Guide  

This guide provides step-by-step instructions for setting up a local development environment for **Drupal 10.4.5** using XAMPP and alternative tools.  

---

## 🚀 1. Install XAMPP (Recommended for Beginners)  

### Step 1: Download & Install XAMPP  
1. Download **XAMPP** from [Apache Friends](https://www.apachefriends.org/).  
2. Run the installer and select:  
   - **Apache** (for the web server)  
   - **MySQL** (for the database)  
   - **phpMyAdmin** (for database management)  
3. Complete the installation and **start Apache & MySQL** from the XAMPP Control Panel.  

### Step 2: Configure Apache (Optional for Virtual Hosts)  
1. Open the **httpd-vhosts.conf** file:  
   - Windows: `C:\xampp\apache\conf\extra\httpd-vhosts.conf`  
   - macOS/Linux: `/opt/lampp/etc/httpd-vhosts.conf`  
2. Add the following virtual host configuration:  
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

### Step 3: Create a Database for Drupal  
1. Open **phpMyAdmin** at `http://localhost/phpmyadmin/`.  
2. Click **Databases** → Enter `drupal_training` → Click **Create**.  

---

## ⚡ 2. Alternative: Install MAMP (For macOS & Windows)  

### Step 1: Download & Install MAMP  
1. Download **MAMP** from [mamp.info](https://www.mamp.info/).  
2. Install and launch **MAMP**.  

### Step 2: Start Web & Database Servers  
1. Open **MAMP** and start **Apache** & **MySQL**.  
2. Access phpMyAdmin via `http://localhost/MAMP/phpMyAdmin.php`.  
3. Create a database named `drupal_training`.  

### Step 3: Configure the Web Server  
1. Go to **Preferences** → **Ports** → Set Apache Port to `80`.  
2. Restart MAMP.  

---

## 🔧 3. Alternative: Install Docker (For Advanced Users)  

### Step 1: Install Docker  
- Download and install **Docker Desktop** from [docker.com](https://www.docker.com/).  

### Step 2: Set Up a Drupal Container  
1. Open **Terminal/Command Prompt** and run:  
   ```sh
   docker run --name drupal -p 8080:80 -d drupal
   ```
2. Open `http://localhost:8080` to access your Drupal site.  

---

## ✅ Final Steps  

✔ Verify **Apache & MySQL** are running.  
✔ Ensure your database (`drupal_training`) exists.  
✔ Proceed with [Drupal Installation](./drupal-installation.md).  

---

🎉 **Your local environment is ready!** You can now install and configure Drupal. 🚀  
```
