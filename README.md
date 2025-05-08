# OpenEMR Installation Guide for Windows

![OpenEMR Logo](https://www.open-emr.org/images/logo.png)

This guide provides step-by-step instructions for installing OpenEMR on a Windows system using XAMPP.

## Requirements

- Windows 10 or 11
- XAMPP with PHP 8.1 or higher
- OpenEMR Windows ZIP package
- Internet connection

## Installation Steps

### 1. Download and Install XAMPP

1. Go to [Apache Friends](https://www.apachefriends.org)
2. Download the version with **PHP 8.1 or higher**
3. Run the installer and install XAMPP in the default location (`C:\xampp`)
4. Open **XAMPP Control Panel**
5. Start the following services:
   - Apache
   - MySQL

### 2. Test XAMPP Installation

- Open your browser and go to: `http://localhost`
- You should see the **XAMPP dashboard**

### 3. Download and Extract OpenEMR

1. Go to the official OpenEMR site: [open-emr.org](https://www.open-emr.org)
2. Click on **Download**
3. Choose the **Windows ZIP Package**
4. Extract the ZIP file
5. Move the extracted folder to: `C:\xampp\htdocs\`
6. Optionally rename the folder to something simple like `openemr`

### 4. Create MySQL Database

1. Visit: `http://localhost/phpmyadmin`
2. Click **New** on the left
3. Create a database named: `openemr`

### 5. Update PHP Settings

1. Open **XAMPP Control Panel**
2. Click **Config** next to Apache, then open `php.ini`
3. Scroll to the end of the file and paste the recommended PHP settings from OpenEMR documentation
4. Save the file
5. Stop and restart Apache

### 6. Run OpenEMR Installer

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

### 7. Step 3 – Create Database and First User

1. On the **"Step 3 - Creating Database and First User"** screen:
   - Click the **Create DB and User** button *(This process may take a minute as it sets up the database structure and creates the first admin user.)*
2. Once completed, you'll automatically move to the next step.

### 8. Step 4 – Configure PHP Settings (if not already done)

If you skipped configuring PHP earlier, do it now:
1. In the **XAMPP Control Panel**, click **Config** next to Apache, then open `php.ini`.
2. Scroll to the end of the file.
3. Paste the **recommended PHP settings** from the OpenEMR official documentation.
4. Save the file and restart Apache.

### 9. Step 5 – Configure Apache Web Server (if needed)

Apache should already be running via XAMPP. If you face issues:
1. Make sure **Apache** and **MySQL** are running in XAMPP.
2. Ensure port **80** is not in use by other applications like Skype or IIS.
3. If needed, edit `httpd.conf` in the Apache config to change the port.

### 10. Step 6 – Choose Theme and Appearance

1. On the **Theme and Display Settings** screen:
   - You can choose a theme or just click **Keep Current** to proceed with the default.
   - Choose:
     - Date Format: e.g., `dd-mm-yyyy`
     - Time Format: `24-hour` or `12-hour`
     - Timezone: e.g., `Asia/Kolkata`
2. Click **Continue**.

### 11. Final Step – Installation Success

1. You'll see a **Setup Complete** message.
2. Important information will be displayed:
   - Admin username and password
   - Configuration file location
   - Site ID (usually `default`)
3. **Note these details carefully**.
4. Click **Login** to proceed to the OpenEMR dashboard.

### 12. Start Using OpenEMR

1. Visit: `http://localhost/openemr`
2. Enter the **Admin Username** and **Password** you created.
3. Click **Login**.
4. 🎉 You're now inside the OpenEMR system and ready to begin!

## Troubleshooting

If you encounter any issues during installation:

1. **Check XAMPP services**: Ensure Apache and MySQL are running
2. **Port conflicts**: Verify that no other applications are using ports 80 or 443
3. **PHP configuration**: Make sure PHP settings match OpenEMR requirements
4. **Database connection**: Verify MySQL credentials are correct
5. **File permissions**: Ensure proper write permissions for OpenEMR directories

## Additional Resources

- [OpenEMR Official Documentation](https://www.open-emr.org/wiki/index.php/OpenEMR_Wiki_Home_Page)
- [OpenEMR Forums](https://community.open-emr.org/)
- [OpenEMR GitHub Repository](https://github.com/openemr/openemr)

## License

OpenEMR is licensed under the GNU General Public License (GPL)