# MyShop - Laravel E-Commerce Platform

A complete multi-feature e-commerce platform built with **Laravel (PHP)** and **MySQL**.

---

## ?? Repository Contents

- **Laravel Core Application**: pp/, ootstrap/, config/, database/, esources/, outes/
- **Frontend & Public Assets**: public/, esources/views/
- **Database Dump**: \creativedesignbd_myshop3.sql\ (Full MariaDB/MySQL database schema and default records)
- **Environment Configuration Template**: \.env.example\

---

## ?? Important Note regarding Hosting & GitHub Pages

> **GitHub Pages cannot run this application directly.**
> 
> **Why?**
> GitHub Pages is designed exclusively for **static websites** (HTML, CSS, JavaScript). It **does not support server-side runtimes like PHP** or **database servers like MySQL**.
> 
> Since **MyShop** is a dynamic backend application requiring:
> 1. PHP 8.1+ / 8.2+ runtime
> 2. MySQL / MariaDB database server
> 3. Composer dependency manager & Laravel Artisan
>
> To run this application live on the web, you should deploy it to:
> - **cPanel / Shared Hosting** (e.g., Namecheap, Hostinger, local BDIX cPanel)
> - **Cloud / VPS** (e.g., DigitalOcean, Hetzner, AWS EC2, Linode)
> - **PaaS Platforms with PHP & MySQL support** (e.g., Render, Railway via Docker)

---

## ?? Local Installation & Setup Guide

### 1. Requirements
- **PHP** >= 8.1 / 8.2
- **Composer** (Dependency manager for PHP)
- **MySQL / MariaDB** (e.g., via XAMPP, Laragon, or Docker)
- **Node.js & NPM**

### 2. Steps to Run Locally

1. **Clone the repository:**
   \\\ash
   git clone https://github.com/junaedislamjim1012/myshop.git
   cd myshop
   \\\

2. **Install PHP dependencies:**
   \\\ash
   composer install
   \\\

3. **Install Frontend dependencies:**
   \\\ash
   npm install
   npm run build
   \\\

4. **Environment Setup:**
   \\\ash
   cp .env.example .env
   php artisan key:generate
   \\\

5. **Database Setup:**
   - Create a MySQL database (e.g., \myshop\).
   - Import \creativedesignbd_myshop3.sql\ into your MySQL database using phpMyAdmin or CLI:
     \\\ash
     mysql -u root -p myshop < creativedesignbd_myshop3.sql
     \\\
   - Update your \.env\ file with your database credentials:
     \\\env
     DB_CONNECTION=mysql
     DB_HOST=127.0.0.1
     DB_PORT=3306
     DB_DATABASE=myshop
     DB_USERNAME=root
     DB_PASSWORD=
     \\\

6. **Storage Link:**
   \\\ash
   php artisan storage:link
   \\\

7. **Start the local development server:**
   \\\ash
   php artisan serve
   \\\
   Access the app at: \http://localhost:8000\

---

## ?? Deploying to cPanel (Recommended for Production)

1. Compress all files except \endor\ and \
ode_modules\.
2. In cPanel **File Manager**, upload and extract into \public_html\ (or a subdomain folder).
3. In cPanel **MySQL Databases**, create a new database, user, and assign all privileges.
4. Open **phpMyAdmin**, select your new database, and import \creativedesignbd_myshop3.sql\.
5. Edit your \.env\ file in cPanel File Manager and enter your database details and \APP_URL\.
6. Configure your domain document root to point to the \public\ folder.

---

## ?? Security Notice

- Never commit your production \.env\ file containing active payment keys, mail credentials, or database passwords to a public GitHub repository.
- Keep the repository private if it contains proprietary business logic or licensed assets.
