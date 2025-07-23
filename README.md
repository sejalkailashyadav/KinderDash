# 🎓 KinderDash – Laravel Admin + Manager Dashboard

KinderDash is a role-based dashboard system built with **Laravel 11** and powered by the **Highdmin** Admin Template. It helps education centers manage children, classes, fees, and monthly reports with clean workflows for both **Admins** and **Center Managers**.

---

## 🚀 Features

- 🧑‍🏫 **Role-Based Access** – Admins and Managers see different views & permissions
- 👶 **Child Management** – Add, edit, assign fees, classes, and siblings
- 💰 **Fee Plans** – Dynamically linked to centers via AJAX
- 🏫 **Center Dashboard** – View monthly reports per center
- 📊 **Reporting Module** – Generate reports based on month, center, or class
- 🧠 **Dynamic Dropdowns** – AJAX-powered field dependencies (fees, classes, siblings)
- 📁 **File Uploads** – Attach documents to child profiles
- 🎨 **Modern UI** – Powered by Highdmin Laravel 11 Template

---

## 🛠️ Tech Stack

- **Backend:** Laravel 11 (PHP 8.3+), Eloquent ORM
- **Frontend:** Blade Templates, jQuery, Bootstrap 5
- **Template:** [Highdmin Laravel 11 Template](https://themeforest.net/item/highdmin-laravel-11-admin-dashboard-template/57033064)
- **Database:** MySQL
- **Other:** AJAX, REST-style routing, file uploads

---

## 📸 Screenshots

_(Add your dashboard screenshots here)_

---

## 📦 Setup Instructions

```bash
# 1. Clone the repo
git clone https://github.com/yourusername/kinderdash.git
cd kinderdash

# 2. Install dependencies
composer install
npm install && npm run build

# 3. Configure environment
cp .env.example .env
php artisan key:generate

# 4. Setup database
php artisan migrate --seed

# 5. Serve the app
php artisan serve
