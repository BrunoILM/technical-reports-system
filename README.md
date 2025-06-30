# 🛠️ Technical Maintenance & Shift Reports System

A modular web-based application to manage technical maintenance tasks, shift reports, and equipment records. Built with **Laravel (API)** and **Angular (Frontend)**.

---

## 📦 Features

- ✅ Equipment registration and status tracking
- 📝 Shift-based reporting with notes and summaries
- 🛠️ Maintenance scheduling (preventive, corrective, predictive)
- 📎 File attachments (images, PDFs, logs) per report/maintenance
- 🔐 Basic user roles: `admin`, `supervisor`, `operator`
- 📅 Calendar-based maintenance overview (planned)
- 📤 Export reports (planned)

---

## 🧩 Tech Stack

| Layer     | Stack              |
|-----------|--------------------|
| Backend   | Laravel 12, MySQL  |
| Frontend  | Angular 20         |
| Database  | MySQL              |
| Auth      | Laravel Sanctum    |
| DevOps    | Docker (optional), GitHub |

---

## 🗂️ Project Structure

technical-reports-system/ ├── backend-laravel/     # Laravel API │   └── ...              # Models, Controllers, Routes ├── frontend-angular/    # Angular UI │   └── ...              # Components, Services, Views └── README.md

---

## 🚀 Setup Instructions

### 1. Clone the repo
```bash
git clone https://github.com/yourusername/technical-reports-system.git
cd technical-reports-system

2. Backend (Laravel)

cd backend-laravel
cp .env.example .env
# Edit DB config in .env

composer install
php artisan key:generate
php artisan migrate
php artisan serve

3. Frontend (Angular)

cd ../frontend-angular
npm install
ng serve

> ⚠️ Ensure both Laravel and Angular are running on separate ports.




---

📌 Database Schema (Simplified)

Users

id, name, email, password, role


Equipment

id, name, code, description, location, status


Shift Reports

id, user_id, shift, date, summary


Maintenances

id, equipment_id, user_id, type, description, scheduled_at, performed_at, status


Attachments

id, file_path, type, maintenance_id?, report_id?, uploaded_by



---

🔧 Future Improvements

Notification system (email or in-app)

Approval workflows for reports

Dashboard with KPIs

File storage on S3



---

🧠 Author

Bruno Pérez
Passionate full-stack developer with a focus on meaningful software for real-world operations.

> "Though gold is valuable, knowledge resting on it is what builds enduring things."




---

📄 License

This project is licensed under the MIT License.
