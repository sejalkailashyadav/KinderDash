# 🎓 Center Management ERP – KinderDash | Laravel App for MultiCenter Preschool

A full-featured, **role-based education ERP** built in Laravel for organizations managing multiple preschool centers. This system allows seamless control over centers, classes, child records, and fee reporting — all within a centralized dashboard.

🛠 Designed for:  
- Preschool chains (like **Kids Learning**)  
- Government-supported childcare  
- NGO-managed learning hubs  

This ERP enables Admins and Managers to collaboratively manage their responsibilities with secure, controlled access.

---

##  Core Use-Case

Kids Learning runs **multiple childcare centers**, each with their own classes, children, and staff. Admins need:
- A **central system** to control all centers
- Local **managers** who can only access their own center’s data
- Monthly **fee tracking** based on changing government subsidies (like CCFRI and ACCB)

This system solves all that using a clean, modular Laravel backend + Blade UI.

---

## 🚪 User Roles & Permission Architecture

| Feature/Module          | Admin (Global)        | Manager (Center-wise)  |
|--------------------------|------------------------|--------------------------|
| Dashboard Access         | ✅ Full Overview        | ✅ Own Center Only       |
| Center Management        | ✅ Add/Edit/Delete      | ❌ Not visible           |
| Class Management         | ✅ Full                 | ✅ Own Center Only       |
| Child Master             | ✅ Full CRUD            | ✅ Own Center Only       |
| Fees Master              | ✅ Full CRUD            | ❌ Hidden                |
| Monthly Reports          | ✅ Filter All Centers   | ✅ Own Center Only       |
| File Upload (Child)      | ✅ Yes                  | ✅ Yes                   |
| Manager User Creation    | ✅ Yes                  | ❌ No Access             |

🔐 **Role enforcement is done via Laravel Middleware + Policies** to ensure data integrity and access control.

---

## 🧠 System Modules & Features

### 🔐 Authentications
- Role-based login (Admin, Manager)
- Session-based access control
- Login protection with CSRF + password hashing

### 🏢 Center Management (Admin)
- Manage multiple education centers
- Add center details: Name, Email, License No, Facility ID, Phone

### 📚 Class Management
- Create/edit/delete classes
- Assign classes to specific centers
- Class Plans like "Happy Hoppers", "Infant 1 Day", etc

### 👶 Child Master
- Add child details: Name, DOB, Parent Name, Mobile, Email
- Assign child to center + class
- Upload profile photo
- View/Edit/Delete child records

### 💸 Fees Master (Admin Only)
- Define:
  - Monthly Base Fee
  - **CCFRI** (Childcare subsidy)
  - **ACCB** (Affordable Child Care Benefit)
  - Auto-calculated Total Fee
- Editable per child/class/month

### 📅 Monthly Reporting
- Filter by:
  - Month
  - Center
- View:
  - Child name, class, base fee, subsidies
  - Auto-generated total
  - Notes (editable per record)

---

## 🧰 Tech Stack & Architecture

| Layer            | Tech Used                         |
|------------------|-----------------------------------|
| Framework        | Laravel 10                        |
| Templating       | Blade Templates                   |
| UI Styling       | Bootstrap 5 / Tailwind (optional) |
| Authentication   | Laravel UI / Breeze               |
| Database         | MySQL                             |
| File Storage     | Laravel Storage (public path)     |
| Access Control   | Middleware, Gates, Policies       |
| Forms & Uploads  | Laravel Validation + CSRF secure  |

---

## 📂 Project Folder Structure Highlights

```bash
app/
  └── Http/
        ├── Controllers/
        │     ├── CenterController.php
        │     ├── ClassController.php
        │     ├── ChildController.php
        │     └── FeesController.php
        ├── Middleware/
        │     └── RoleMiddleware.php
resources/
  └── views/
        ├── dashboard.blade.php
        ├── child/
        ├── center/
        └── fees/
routes/
  └── web.php
````

## ⚙️ Setup Instructions

```bash
# 1. Clone the repository
git clone https://github.com/sejalkailashyadav/KinderDash.git
cd center-management-erp

# 2. Install PHP & JS dependencies
composer install
npm install && npm run dev

# 3. Environment setup
cp .env.example .env
php artisan key:generate

# 4. Database setup
# (Update .env with DB credentials)
php artisan migrate --seed

# 5. Launch the app
php artisan serve
```

✔ You can now visit `http://localhost:8000/login` and login with the test credentials.

---

## 🧠 Real-World Expansion Ideas

> These make your project ready for production or SaaS transformation.

* 📱 **Parent Mobile Portal** (Flutter/React Native)
* 🧾 **PDF Export** of monthly reports
* 💳 **Payment Tracking + History**
* ✉️ **Email/SMS** reminders to parents
* 🔍 **Audit Logs** of actions (edit/delete)
* 📊 **Analytics Dashboard** for Admins

---

## 🎬 **Demo Video:** [Click](https://drive.google.com/file/d/1NVSRbI-bqVSlqzU3Mbj0zXw0-2U1CcWB/view?usp=sharing)


---

## 👨‍💻 Author

Built with ❤️ by **\[Sejal Yadav]**,
Guided & structured with the help of ChatGPT.

This ERP structure is inspired by real-world preschool operational needs and Laravel best practices.

---

## 📜 License

This project is open-source. You're free to:

* Fork it
* Extend it
* Use it for client work or internal school systems

---

## 🔗 Let's Connect

If you want help deploying or selling this to schools:

* 📧 Email: [sejalyadav122@gmail.com](mailto:sejalyadav122@gmail.com)
* 🌐 Portfolio: [sejalkailashyadav](https://sejalkailashyadav.netlify.app/)
* 💼 LinkedIn: [sejalkailashyadav](https://www.linkedin.com/in/sejalkailashyadav/)

```

---

### ✅ What's Next?

- Want this as a downloadable `.md` file? I’ll generate it.
- Want to prepare a GitHub repo with first commit? I’ll help.
- Want a SaaS version plan (paid model)? I’ll map that too.

Just tell me your next step — let’s get it done. 🔥
```
