# LUMS Student Portal 🎓

A Flutter-based mobile application built for students at Lahore University of Management Sciences (LUMS).

The app combines common student services with a campus news feed and community features, using Firebase for authentication, database, and storage.

## Features

### Authentication

* Email/password login and registration
* Email verification
* Password reset and change
* User profile management

### Campus Feed

* View campus announcements and posts
* Create posts
* Participate in polls
* Save posts for later

### Student Services

* Submit and track complaints
* Access student council information
* View faculty and staff office hours
* Access important campus documents

### Community

* Student profiles
* Interact with other students
* Receive campus updates and notifications

## Tech Stack

* **Flutter / Dart** — Mobile app
* **Firebase Authentication** — User authentication
* **Cloud Firestore** — Application data
* **Cloud Storage** — File and image storage
* **Provider** — State management
* **Material Design** — UI

## Getting Started

### Requirements

* [Flutter SDK](https://flutter.dev)
* [Dart SDK](https://dart.dev)
* Android Studio or VS Code
* Firebase project
* Android/iOS device or emulator

### Installation

Clone the repository:

```bash
git clone https://github.com/yourusername/lums-student-portal.git
cd lums-student-portal
```

Install the Flutter dependencies:

```bash
flutter pub get
```

### Firebase Setup

Create a Firebase project and connect the Android and iOS applications to it.

Add the Firebase configuration files:

```text
android/app/google-services.json
ios/Runner/GoogleService-Info.plist
```

Enable the following Firebase services:

* Authentication
* Cloud Firestore
* Cloud Storage

### Run the App

```bash
flutter run
```

For a specific platform:

```bash
flutter run -d ios
flutter run -d chrome
```

## Project Structure

```text
lib/
├── Backend/
│   ├── authentication.dart
│   ├── signUpOrLogin.dart
│   └── validators.dart
├── Themes/
│   ├── Theme.dart
│   └── progessIndicator.dart
├── models/
│   ├── complaint.dart
│   ├── post.dart
│   ├── profile.dart
│   └── officeHours.dart
├── pages/
│   ├── home.dart
│   ├── login.dart
│   ├── signUp.dart
│   ├── newsfeed.dart
│   ├── profile.dart
│   ├── addPost.dart
│   ├── addComplaint.dart
│   ├── studentCouncil.dart
│   └── settings.dart
└── main.dart
```

## Application Flow

A typical user flow looks like this:

```text
Register / Login
       ↓
     Home
       ↓
 ┌─────┼──────────────┐
 ↓     ↓              ↓
Feed  Services      Profile
 ↓     ↓
Posts  Complaints
Polls  Office Hours
       Documents
```

## Screenshots

Screenshots can be added here to show the main screens and UI of the application.

## Testing

Run the Flutter test suite with:

```bash
flutter test
```

## Building

### Android

```bash
flutter build apk --release
```

Or generate an Android App Bundle:

```bash
flutter build appbundle --release
```

### iOS

```bash
flutter build ios --release
```

## Team

**Group 04 — Software Engineering (CS 360), Spring 2021**

* **Zuha Zia** — Group Leader
* **Huzaifah Nadeem** — Project Champion
* **Syed Muhammad Daniyal Zaidi** — Developer
* **Suleman Khan** — Developer
* **Khawaja Saad Munir** — Developer

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

---

Built by students as part of the LUMS Software Engineering course.
