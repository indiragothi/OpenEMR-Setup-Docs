# 📋 OpenEMR Installation Guide (Windows)

This document provides step-by-step instructions to install **OpenEMR** on a Windows system using **XAMPP**.

---

## ✅ Requirements

- Windows 10 or 11
- XAMPP with PHP 8.1 or higher
- OpenEMR Windows ZIP package
- Internet connection

---

## 🪜 Installation Steps

### 1️⃣ Download and Install XAMPP

1. Go to [https://www.apachefriends.org](https://www.apachefriends.org)
2. Download the version with **PHP 8.1 or higher**
3. Run the installer and install XAMPP in the default location (`C:\xampp`)
4. Open **XAMPP Control Panel**
5. Start the following services:
   - Apache
   - MySQL

---

### 2️⃣ Test XAMPP Installation

- Open your browser and go to: `http://localhost`
- You should see the **XAMPP dashboard**

---

### 3️⃣ Download and Extract OpenEMR

1. Go to the official OpenEMR site: [https://www.open-emr.org](https://www.open-emr.org)
2. Click on **Download**
3. Choose the **Windows ZIP Package**
4. Extract the ZIP file
5. Move the extracted folder to:  
   `C:\xampp\htdocs\`
6. Optionally rename the folder to something simple like `openemr`

---

### 4️⃣ Create MySQL Database

1. Visit: `http://localhost/phpmyadmin`
2. Click **New** on the left
3. Create a database named: `openemr`

---

### 5️⃣ Update PHP Settings

1. Open **XAMPP Control Panel**
2. Click **Config** next to Apache, then open `php.ini`
3. Scroll to the end of the file and paste the recommended PHP settings from OpenEMR documentation
4. Save the file
5. Stop and restart Apache

---

### 6️⃣ Run OpenEMR Installer

1. Go to: `http://localhost/openemr` in your browser
2. Click **Proceed to Step 1**
3. Choose **Fresh Installation**, then click **Proceed to Step 2**
4. Fill in the following:
   - MySQL Server: `localhost`
   - Database Name: `openemr`
   - MySQL User: `root`
   - MySQL Password: (leave blank if default)
   - Initial Admin Username and Password (your choice)
5. Click **Create DB and User**
6. Follow the remaining steps to complete the installation

---

## 🎉 Done!

You can now log in at:  
`http://localhost/openemr`  
Use the admin credentials you created during setup.

---

## ⚙️ Optional Customization

- Change theme: `Administration → Globals → Appearance`
- Manage users: `Administration → Users`
- Add custom fields: `Administration → Layouts`
- Add logo: Replace image in `sites/default/images/`

---

## 📌 Notes

- For production use, secure your installation properly
- Change root password in MySQL
- Backup database regularly
