# PHP Project Setup Guide (Windows & Ubuntu)

This guide explains how to install PHP and run your PHP project on both **Windows** and **Ubuntu**.

---

## 🚀 Windows Setup

### 1. Install PHP
1. Download the **Windows ZIP (Thread Safe)** from:  
   https://www.php.net/downloads  
2. Extract it to:
   ```
   C:\php
   ```
3. Add `C:\php` to your **PATH** (Environment Variables).

### 2. Verify Installation
```
php -v
```

### 3. Run Your PHP Project
```
cd C:\path\to\project
php -S localhost:8000
```

### 4. Access in Browser
```
http://localhost:8000/index.php
```

---

## 🐧 Ubuntu Setup

### 1. Install PHP (CLI)
```
sudo apt update
sudo apt install php8.1-cli
```
(or simply)
```
sudo apt install php
```

### 2. Verify Installation
```
php -v
```

### 3. Prepare Your Project
Put these files in the same folder:
- `index.php`
- `login.php`
- `users.php`

Check that the **antispam field name** in `login.php` is:
```
email_address
```

### 4. Run Built-in PHP Server
```
cd /path/to/project
php -S localhost:8000
```

### 5. Set Permissions (Ubuntu)

#### Quick Testing (not recommended for production)
```
chmod 777 users.php
```

#### Safer Permissions (for Apache environments)
```
sudo chown www-data:www-data users.php
sudo chmod 664 users.php
```

### 6. Access in Browser
```
http://localhost:8000/index.php
```

---

## ✅ You're All Set!
Your PHP project should now run successfully on both Windows and Ubuntu.
