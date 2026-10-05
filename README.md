# CSFM Library Plus

A cross-platform library management app built with Flutter and Firebase. It digitalizes the borrowing and reservation workflow of a school library, with role-based access for administrators and students.

> Academic project developed at **IT Business School (ITBS), Nabeul**, supervised by **M. Riadh Hajji**.

## Problem

Traditional library management is manual and slow. Students struggle to find available documents, reservations are processed late, borrowing and returns are poorly tracked, and there are no real-time notifications or usage statistics.

## Features

**Student**
- Secure sign-up and login with email verification
- Browse documents by category and search by title, author or category
- Reserve an available document and confirm its pickup
- Track current borrowings and the days remaining before return
- View borrowing and reservation history
- Receive notifications (reservations, returns)

**Administrator**
- Manage users (add, edit, delete)
- Manage documents (add, edit, delete)
- Approve or cancel reservations
- Manage borrowings and mark returns
- Track active delays and recent activity
- Consult usage statistics (most borrowed documents, monthly evolution, documents by category)

## Tech Stack

| Layer | Technology |
|---|---|
| Framework | Flutter, Dart |
| Authentication | Firebase Authentication (email verification, roles) |
| Database | Cloud Firestore (real-time NoSQL) |
| Local storage | SharedPreferences (session persistence) |
| UI | Material Design |

Platforms: **Web** and **Android**.

## Architecture

```
User (Student / Admin) → Flutter app → Firebase Authentication → Cloud Firestore
```

Main Firestore collections: `users`, `documents`, `reservations`, `emprunts`, `notifications`.

Access is role-based (administrator, internal student, external student). Firestore security rules allow only authenticated users to read data, students to access only their own data, and administrators to manage everything.

## Project Structure

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

## Screenshots

<!-- Add screenshots to a /screenshots folder, then reference them here, for example:
![Login](screenshots/login.png)
-->

_Coming soon._

## Getting Started

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

## Future Improvements

- Advanced push notifications (return reminders, available reservations)
- Detailed analytics dashboards for administrators
- Barcode / QR code scanning for borrowings and returns
- Offline mode
- Customizable theme and richer animations

## Author

**Med Amine Mrad**, Software Engineering student at ITBS, Tunisia.
