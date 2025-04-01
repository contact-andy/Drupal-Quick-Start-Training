```markdown
# Composer Setup for Drupal

## Introduction

Composer is a dependency manager for PHP that allows you to manage Drupal core, contributed modules, and themes efficiently. This guide will walk you through installing Composer and using it to manage Drupal packages.

---

## Step 1: Install Composer

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

## Step 2: Install Drupal Using Composer

### Create a New Drupal Project

To install Drupal 10.4.5 (or the latest version), run:

```bash
composer create-project drupal/recommended-project drupal_project
```

This will:
- Download Drupal core
- Set up the necessary dependencies
- Create a new Drupal project folder

### Navigate to the Drupal Directory

```bash
cd drupal_project
```

### Start a Local Development Server (Optional)

For quick testing, run:

```bash
php -S localhost:8080 -t web/
```

Now, visit [http://localhost:8080](http://localhost:8080) in your browser to see your Drupal installation.

---

## Step 3: Managing Drupal Modules and Themes

### Install a Module

To install a Drupal module (e.g., Pathauto), run:

```bash
composer require drupal/pathauto
```

### Install a Theme

To install a Drupal theme (e.g., Bootstrap), run:

```bash
composer require drupal/bootstrap
```

### Update Dependencies

To update Drupal core and all installed packages:

```bash
composer update
```

---

## Step 4: Using Drush for Module Management

Drush is a command-line tool for managing Drupal sites. Install it using:

```bash
composer require drush/drush
```

### Enable a Module

```bash
drush en pathauto -y
```

### Clear Cache

```bash
drush cache:rebuild
```

---

## Conclusion
```

You can copy this content into a `.md` file for use!
