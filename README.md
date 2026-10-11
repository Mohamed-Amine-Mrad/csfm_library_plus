<h1 align="center">📚 CSFM Library Plus</h1>

<h3 align="center">
Cross-Platform Library Management Application
</h3>

<p align="center">
  Flutter • Dart • Firebase Authentication • Cloud Firestore
</p>

<p align="center">
  <img src="https://img.shields.io/badge/Flutter-02569B?style=for-the-badge&logo=flutter&logoColor=white">
  <img src="https://img.shields.io/badge/Dart-0175C2?style=for-the-badge&logo=dart&logoColor=white">
  <img src="https://img.shields.io/badge/Firebase-FFCA28?style=for-the-badge&logo=firebase&logoColor=black">
</p>

<p align="center">
  🎓 Academic project at IT Business School (ITBS), Nabeul · Supervised by M. Riadh Hajji
</p>

<p align="center">
  <img src="https://capsule-render.vercel.app/api?type=rect&color=00BFFF&height=2&section=header" width="80%">
</p>

## 📌 Overview

Traditional library management is manual and slow: students struggle to find available documents, reservations are processed late, borrowing and returns are poorly tracked, and there are no real-time notifications or usage statistics.

**CSFM Library Plus** digitalizes this workflow with an app that runs on **web and Android**, with role-based access for administrators and students.

<p align="center">
  <img src="https://capsule-render.vercel.app/api?type=rect&color=00BFFF&height=2&section=header" width="80%">
</p>

## ✨ Features

### 🎓 Student
- 🔐 Secure sign-up and login with email verification
- 🔎 Browse documents by category and search by title, author or category
- 📅 Reserve an available document and confirm its pickup
- ⏳ Track current borrowings and the days remaining before return
- 🕘 View borrowing and reservation history
- 🔔 Receive notifications (reservations, returns)

### 🛡️ Administrator
- 👥 Manage users (add, edit, delete)
- 📖 Manage documents (add, edit, delete)
- ✅ Approve or cancel reservations
- 🔁 Manage borrowings and mark returns
- ⏰ Track active delays and recent activity
- 📊 Consult usage statistics (most borrowed documents, monthly evolution, documents by category)

<p align="center">
  <img src="https://capsule-render.vercel.app/api?type=rect&color=00BFFF&height=2&section=header" width="80%">
</p>

## 🔐 Roles & Security

Access is role-based: **Administrator**, **Internal Student** and **External Student**.

- 🔑 Firebase Authentication with email verification
- 💾 Session persistence with SharedPreferences
- 🛡️ Firestore security rules: only authenticated users can read data, students access only their own data, and administrators manage everything

<p align="center">
  <img src="https://capsule-render.vercel.app/api?type=rect&color=00BFFF&height=2&section=header" width="80%">
</p>

## 🛠️ Tech Stack

**Architecture**

`User (Student / Admin)` → `Flutter app` → `Firebase Authentication` → `Cloud Firestore`

**Tech Stack**

`Flutter` · `Dart` · `Firebase Authentication` · `Cloud Firestore` · `SharedPreferences` · `Material Design`

**Firestore collections**

`users` · `documents` · `reservations` · `emprunts` · `notifications`

<p align="center">
  <img src="https://capsule-render.vercel.app/api?type=rect&color=00BFFF&height=2&section=header" width="80%">
</p>

## 📁 Project Structure

```
lib/
├── core/
│   ├── constants/
│   └── theme/
├── screens/
│   ├── admin/
│   ├── auth/
│   ├── home/
│   └── student/
├── services/
└── widgets/
```

<p align="center">
  <img src="https://capsule-render.vercel.app/api?type=rect&color=00BFFF&height=2&section=header" width="80%">
</p>




## 🚀 Getting Started

### Prerequisites
- [Flutter SDK](https://docs.flutter.dev/get-started/install)
- A Firebase project with **Authentication** (email/password) and **Cloud Firestore** enabled

### Run the project

```bash
git clone https://github.com/Mohamed-Amine-Mrad/csfm_library_plus.git
cd csfm_library_plus
flutter pub get
flutter run -d chrome    # web
flutter run              # connected Android device or emulator
```

### Use your own Firebase project

The repository contains the Firebase client configuration of the original project. To connect the app to your own backend, install the [FlutterFire CLI](https://firebase.google.com/docs/flutter/setup) and run:

```bash
flutterfire configure
```

This regenerates `lib/firebase_options.dart` and `android/app/google-services.json` for your project.

<p align="center">
  <img src="https://capsule-render.vercel.app/api?type=rect&color=00BFFF&height=2&section=header" width="80%">
</p>

## 🔭 Future Improvements

- 🔔 Advanced push notifications (return reminders, available reservations)
- 📈 Detailed analytics dashboards for administrators
- 📷 Barcode / QR code scanning for borrowings and returns
- 📴 Offline mode
- 🎨 Customizable theme and richer animations

<p align="center">
  <img src="https://capsule-render.vercel.app/api?type=rect&color=00BFFF&height=2&section=header" width="80%">
</p>

## 👨‍💻 Author

**Med Amine Mrad**, Software Engineering student at ITBS, Tunisia.

<p align="center">
  <a href="https://www.linkedin.com/in/mrad-mohamed-amine">
    <img src="https://img.shields.io/badge/LinkedIn-Connect-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white">
  </a>
  <a href="mailto:mohamedamine.mrad@itbs.tn">
    <img src="https://img.shields.io/badge/Email-Contact-EA4335?style=for-the-badge&logo=gmail&logoColor=white">
  </a>
</p>
