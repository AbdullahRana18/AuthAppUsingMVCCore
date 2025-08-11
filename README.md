# AuthApp – ASP.NET Core Identity Authentication System

## 📌 Overview
AuthApp is a secure authentication and account management system built with **ASP.NET Core MVC** and **Identity**.  
It provides user registration, login, logout, email confirmation, password reset, two-factor authentication, and account management features with **SMTP email integration**.

---

## ✨ Features
- 🔐 **User Authentication** (Login, Logout, Register)  
- 📧 **Email Confirmation**  
- 🔑 **Forgot & Reset Password**  
- 🔒 **Two-Factor Authentication (2FA)** via Email  
- ⚙ **Account Management** (Update Profile, Change Password)  
- 📬 **SMTP Email Sending** (Configured for Gmail)  

---

## 📄 Pages & Routes

### Authentication
- `/Account/Register` → New user registration  
- `/Account/Login` → User login  
- `/Account/Logout` → User logout  
- `/Account/ForgotPassword` → Request password reset link  
- `/Account/ResetPassword` → Reset password  
- `/Account/ConfirmEmail` → Email confirmation  
- `/Account/TwoFactorAuthentication` → 2FA verification page  

### Account Management
- `/Account/Manage` → Update profile and account settings  

---

## 🛠 Getting Started

### 1️⃣ Clone the Repository
```bash

git clone https://github.com/YourUsername/AuthApp.git
cd AuthApp


2️⃣ Configure Database
Update appsettings.json:
"ConnectionStrings": {
  "ApplicationDbContextConnection": "Server=YOUR_SERVER;Database=AUTHAPP;Trusted_Connection=True;MultipleActiveResultSets=true;TrustServerCertificate=True;"
}


3️⃣ Configure Email Settings
Set Gmail SMTP details in appsettings.json:

"EmailSettings": {
  "Host": "smtp.gmail.com",
  "Port": 587,
  "Username": "your-email@gmail.com",
  "Password": "your-app-password"
}


4️⃣ Apply Migrations & Run
dotnet ef database update
dotnet run


  📦 Technologies Used
ASP.NET Core MVC

Identity (Authentication & Authorization)

Entity Framework Core (SQL Server)

Bootstrap 5 (Responsive UI)

SMTP Email (Gmail)


📌 Notes
Make sure SMTP credentials are valid.

For production, store sensitive data in environment variables instead of appsettings.json.

2FA will only work if email sending is configured correctly.
git clone https://github.com/YourUsername/AuthApp.git
cd AuthApp
