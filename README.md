# 🔐 AuthApp - ASP.NET Core MVC Authentication & Authorization

A complete authentication and authorization system built with **ASP.NET Core MVC** and **Identity**.  
Supports **Role-based Access (Admin & User)**, **User Management**, **Email Confirmation**, **2FA**, and **Responsive Bootstrap UI**.

---

## 🚀 Features

### 🔑 Authentication
- User Registration & Login
- Secure Password Hashing
- Email Confirmation before Login
- Forgot Password & Reset via Email

### 🛡 Authorization
- **Two Roles**: `Admin` & `User`
- Admin can view **all registered users**
- User dashboard separate from Admin dashboard

### 👤 User Management (Admin Only)
- Create, Edit, Delete Users
- Assign/Change Roles
- View all registered users in a table

### 📧 Email & Security
- SMTP-based Email Sending (Gmail)
- Password Reset Email
- Two-Factor Authentication (2FA) via Email

### 🎨 UI / UX
- Responsive UI with **Bootstrap 5**
- Custom Login, Register, and Dashboard pages
- Role-specific navigation menu

---

## 📦 Technologies Used
- **ASP.NET Core MVC 9**
- **Entity Framework Core** (SQL Server)
- **ASP.NET Core Identity**
- **Bootstrap 5**
- **SMTP Email (Gmail)**
- **C# 12**

---

## ⚙️ Installation & Setup

### 1️⃣ Clone the Repository
```bash


2️⃣ Configure Database
Edit appsettings.json and update the SQL Server connection string:

"ConnectionStrings": {
  "ApplicationDbContextConnection": "Server=YOUR_SERVER;Database=AUTHAPP;Trusted_Connection=True;MultipleActiveResultSets=true;TrustServerCertificate=True;"
}



3️⃣ Configure Email Settings
In appsettings.json, set your Gmail SMTP details:

"EmailSettings": {
  "Host": "smtp.gmail.com",
  "Port": 587,
  "Username": "your-email@gmail.com",
  "Password": "your-app-password"
}



⚠️ Note: Use an App Password for Gmail, not your normal account password.



4️⃣ Apply Migrations & Run

dotnet ef database update
dotnet run


👥 Default Roles & Admin Setup
When the application starts for the first time:

Roles: Admin and User will be created automatically.

Default Admin Account:

Username: Admin

Password: Admin@123

Email: admin@example.com (update in seeding logic if needed)


📂 Project Structure
AuthAppUsingMVCCore/
│-- Controllers/
│-- Models/
│-- Views/
│-- Data/
│-- Services/
│-- wwwroot/
│-- appsettings.json
│-- Program.cs
│-- README.md



📌 Notes
For production, never store passwords or SMTP credentials in appsettings.json. Use environment variables or a secure secrets manager.

2FA will only work if email sending is properly configured.

Ensure SQL Server is running before applying migrations


💡 Developed by Abdullah Rana
git clone https://github.com/AbdullahRana18/AuthAppUsingMVCCore.git
cd AuthAppUsingMVCCore
