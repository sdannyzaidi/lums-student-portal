# LUMS Student Portal 🎓

[![Flutter](https://img.shields.io/badge/Flutter-02569B?style=for-the-badge&logo=flutter&logoColor=white)](https://flutter.dev)
[![Firebase](https://img.shields.io/badge/Firebase-039BE5?style=for-the-badge&logo=Firebase&logoColor=white)](https://firebase.google.com)
[![Dart](https://img.shields.io/badge/Dart-0175C2?style=for-the-badge&logo=dart&logoColor=white)](https://dart.dev)

A comprehensive mobile application designed to enhance the student experience at Lahore University of Management Sciences (LUMS). This cross-platform Flutter app provides students with essential tools for campus life, academic management, and community engagement.

## 📱 Features

### 🔐 Authentication & Security
- **Secure Login/Signup** - Firebase Authentication integration
- **Account Verification** - Email verification system
- **Password Management** - Reset and change password functionality
- **Profile Management** - Comprehensive user profile system

### 📰 Campus Communication
- **News Feed** - Stay updated with campus announcements and events
- **Post Creation** - Share updates, events, and information with the community
- **Interactive Polls** - Participate in campus-wide surveys and voting
- **Saved Posts** - Bookmark important announcements and posts

### 🎯 Student Services
- **Complaint System** - Submit and track complaints with resolution status
- **Student Council Integration** - Direct communication with student representatives
- **Office Hours** - Access faculty and staff availability schedules
- **Document Access** - Quick access to important campus documents

### 👥 Community Features
- **User Profiles** - Detailed student profiles with customization options
- **Social Interaction** - Connect and communicate with fellow students
- **Campus Updates** - Real-time notifications and announcements

## 🛠️ Technology Stack

- **Frontend**: Flutter (Dart)
- **Backend**: Firebase
  - Authentication
  - Cloud Firestore (Database)
  - Cloud Storage
- **State Management**: Provider Pattern
- **UI/UX**: Material Design with custom theming

## 📋 Prerequisites

Before running this project, make sure you have:

- [Flutter SDK](https://flutter.dev/docs/get-started/install) (>=2.12.2)
- [Dart SDK](https://dart.dev/get-dart) (>=2.12.2)
- [Android Studio](https://developer.android.com/studio) or [VS Code](https://code.visualstudio.com/)
- [Firebase CLI](https://firebase.google.com/docs/cli) (for Firebase setup)
- Android/iOS device or emulator

## 🚀 Installation & Setup

### 1. Clone the Repository
```bash
git clone https://github.com/yourusername/lums-student-portal.git
cd lums-student-portal
```

### 2. Install Dependencies
```bash
flutter pub get
```

### 3. Firebase Configuration
1. Create a new Firebase project at [Firebase Console](https://console.firebase.google.com/)
2. Add Android/iOS apps to your Firebase project
3. Download and place configuration files:
   - `google-services.json` in `android/app/`
   - `GoogleService-Info.plist` in `ios/Runner/`

### 4. Enable Firebase Services
In your Firebase console, enable:
- Authentication (Email/Password)
- Cloud Firestore
- Cloud Storage

### 5. Run the Application
```bash
# For Android
flutter run

# For iOS
flutter run -d ios

# For Web
flutter run -d chrome
```

## 📁 Project Structure

```
lib/
├── Backend/
│   ├── authentication.dart      # Firebase auth logic
│   ├── signUpOrLogin.dart       # Authentication flow
│   └── validators.dart          # Input validation
├── Themes/
│   ├── Theme.dart              # App theming and colors
│   └── progessIndicator.dart   # Custom loading indicators
├── models/
│   ├── complaint.dart          # Complaint data model
│   ├── post.dart              # Post data model
│   ├── profile.dart           # User profile model
│   └── officeHours.dart       # Office hours model
├── pages/
│   ├── home.dart              # Main dashboard
│   ├── login.dart             # Login screen
│   ├── signUp.dart            # Registration screen
│   ├── newsfeed.dart          # Campus news feed
│   ├── profile.dart           # User profile
│   ├── addPost.dart           # Create new posts
│   ├── addComplaint.dart      # Submit complaints
│   ├── studentCouncil.dart    # Student council interface
│   └── settings.dart          # App settings
└── main.dart                  # App entry point
```

## 🎨 Screenshots

*Add screenshots of your app here to showcase the UI*

## 🔧 Configuration

### Firebase Rules
Make sure to configure your Firestore security rules appropriately:

```javascript
rules_version = '2';
service cloud.firestore {
  match /databases/{database}/documents {
    // Add your security rules here
    match /{document=**} {
      allow read, write: if request.auth != null;
    }
  }
}
```

### App Permissions
The app requires the following permissions:
- Internet access
- Camera (for profile pictures)
- Storage (for file uploads)

## 🧪 Testing

Run the test suite:
```bash
flutter test
```

## 📱 Building for Production

### Android
```bash
flutter build apk --release
# or for app bundle
flutter build appbundle --release
```

### iOS
```bash
flutter build ios --release
```

## 🤝 Contributing

We welcome contributions! Please follow these steps:

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

### Code Style
- Follow [Dart style guide](https://dart.dev/guides/language/effective-dart/style)
- Use meaningful variable and function names
- Add comments for complex logic
- Ensure proper error handling

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 👥 Team

**Group 04 - Software Engineering (CS 360) Spring 2021**

- **Zuha Zia** - Group Leader
- **Huzaifah Nadeem** - Project Champion
- **Syed Muhammad Daniyal Zaidi** - Developer
- **Suleman Khan** - Developer
- **Khawaja Saad Munir** - Developer

## 🏫 About LUMS

[Lahore University of Management Sciences (LUMS)](https://lums.edu.pk/) is a leading university in Pakistan, known for its academic excellence and innovative approach to education.

## 📞 Support

For support and questions:
- Create an issue in this repository
- Contact the development team
- Check the [Flutter documentation](https://flutter.dev/docs)

## 🙏 Acknowledgments

- LUMS Faculty and Staff for their guidance
- Flutter and Firebase teams for excellent documentation
- The open-source community for inspiration and resources

---

**Made with ❤️ by LUMS Students for LUMS Students**
