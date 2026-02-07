# Suraksha Kavach

**A Mobile Framework for Women's Safety via Real-Time Geospatial Alerts**

[![Android](https://img.shields.io/badge/Platform-Android-green.svg)](https://www.android.com/)
[![Kotlin](https://img.shields.io/badge/Language-Kotlin-blue.svg)](https://kotlinlang.org/)
[![License](https://img.shields.io/badge/License-Apache%202.0-blue.svg)](LICENSE)

## Overview

Suraksha Kavach is a professional-grade Android application designed to enhance women's safety through immediate emergency response capabilities. Developed in alignment with **United Nations Sustainable Development Goal 5 (Gender Equality)**, this application provides a reliable and accessible safety framework for individuals in emergency situations.

**Copyright © 2026 Megha Dey. All Rights Reserved.**

## Project Objectives

- Analyze existing challenges to women's safety and review current technological solutions
- Design a user-centric and intuitive mobile application interface
- Develop a robust Android application featuring real-time location tracking, SMS alerts, audible alarm, and emergency auto-dialer
- Implement a secure on-device SQLite database for managing emergency contacts
- Evaluate application performance, reliability, and accuracy through rigorous testing
- Create a scalable and adaptable framework that can be localized for different regions

## Features

### Core Functionality
- **Emergency Panic Button**: Long-press activation (2 seconds) for quick emergency response
- **Real-time Location Tracking**: GPS-based location sharing via Google Maps link
- **SMS Alerts**: Automatic SMS sent to all emergency contacts with current location
- **Auto-Dialer**: Automatically calls emergency services (default: 112)
- **Audible Alarm**: Loud alarm sound to attract attention
- **Vibration Alert**: Continuous vibration during emergency

### Contact Management
- Add, edit, and delete emergency contacts
- Store contact name, phone number, and relationship
- SQLite database for secure local storage
- No contact limit

### Customizable Settings
- Configure emergency phone number
- Customize SMS alert message
- Enable/disable alarm
- Enable/disable auto-call feature

## Architecture

### Technology Stack
- **Language**: Kotlin 1.9.20
- **Platform**: Android (API 24 - API 34)
- **Database**: SQLite with structured CRUD operations
- **Location Services**: Google Play Services Location API
- **UI Framework**: Material Design 3 Components
- **Architecture Pattern**: MVVM-ready modular structure
- **Build System**: Gradle Kotlin DSL

### Project Structure
```
SurakshaKavach/
├── app/
│   ├── src/
│   │   ├── main/
│   │   │   ├── java/com/surakshaKavach/womensafety/
│   │   │   │   ├── MainActivity.kt
│   │   │   │   ├── EmergencyContactsActivity.kt
│   │   │   │   ├── SettingsActivity.kt
│   │   │   │   ├── adapters/
│   │   │   │   │   └── ContactsAdapter.kt
│   │   │   │   ├── database/
│   │   │   │   │   └── DatabaseHelper.kt
│   │   │   │   ├── models/
│   │   │   │   │   └── EmergencyContact.kt
│   │   │   │   ├── services/
│   │   │   │   │   └── EmergencyService.kt
│   │   │   │   └── utils/
│   │   │   │       └── PermissionHelper.kt
│   │   │   ├── res/
│   │   │   │   ├── layout/
│   │   │   │   ├── drawable/
│   │   │   │   ├── values/
│   │   │   │   └── xml/
│   │   │   └── AndroidManifest.xml
│   │   └── build.gradle.kts
│   └── build.gradle.kts
├── settings.gradle.kts
└── README.md
```

## 🚀 Getting Started

### Prerequisites
- Android Studio Hedgehog (2023.1.1) or later
- Android SDK API 24 or higher
- Kotlin 1.9.20 or later
- Gradle 8.2 or higher

### Installation Steps

1. **Clone or Download the Repository**
   ```bash
   cd /path/to/SurakshaKavach
   ```

2. **Open in Android Studio**
   - Launch Android Studio
   - Click "Open an Existing Project"
   - Navigate to the `SurakshaKavach` folder
   - Click "OK"

3. **Sync Gradle**
   - Android Studio will automatically sync Gradle files
   - Wait for the sync to complete
   - If prompted, update Gradle or Android Gradle Plugin

4. **Configure Emulator or Device**
   - **Emulator**: Create an AVD with API 24+ in Device Manager
   - **Physical Device**: Enable USB Debugging in Developer Options

5. **Run the Application**
   - Click the "Run" button (Green Play icon)
   - Select your device/emulator
   - Wait for the app to install and launch

## 📱 How to Use

### First Time Setup
1. Launch the app
2. Grant all required permissions:
   - Location (Fine & Coarse)
   - SMS
   - Phone
   - Notifications (Android 13+)
3. Add at least one emergency contact
4. Configure settings (optional)

### Emergency Activation
1. **Hold the red SOS button for 2 seconds**
2. Confirm emergency activation
3. The app will:
   - Get your current GPS location
   - Send SMS alerts to all emergency contacts
   - Call the emergency number (if enabled)
   - Sound the alarm (if enabled)
   - Vibrate the phone

### Managing Emergency Contacts
1. Tap "Emergency Contacts" from main screen
2. Tap the "+" button to add a contact
3. Enter name, phone number, and relationship
4. Tap to edit or delete existing contacts

### Configuring Settings
1. Tap "Settings" from main screen
2. Modify:
   - Emergency phone number (default: 112)
   - SMS alert message
   - Alarm settings
   - Auto-call settings
3. Tap "Save Settings"

## 🔐 Permissions Explained

| Permission | Purpose |
|------------|---------|
| `ACCESS_FINE_LOCATION` | Get precise GPS coordinates for location sharing |
| `ACCESS_COARSE_LOCATION` | Fallback location if GPS unavailable |
| `SEND_SMS` | Send emergency alerts to contacts |
| `CALL_PHONE` | Auto-dial emergency services |
| `VIBRATE` | Phone vibration during emergency |
| `FOREGROUND_SERVICE` | Keep emergency service running |
| `POST_NOTIFICATIONS` | Show emergency notifications (Android 13+) |

## 🧪 Testing

### Unit Testing
- Database operations
- Permission checks
- Settings validation

### Integration Testing
- Emergency service workflow
- SMS sending
- Location retrieval

### User Acceptance Testing (UAT)
- Test with real users in controlled environment
- Verify ease of use under stress
- Validate all features work reliably

## 📊 Project Timeline

| Phase | Duration | Activities |
|-------|----------|------------|
| Phase 1: Analysis & Design | Weeks 1-2 | Requirements, UI/UX design, database schema |
| Phase 2: Core Development | Weeks 3-8 | UI implementation, database, APIs integration |
| Phase 3: Integration & Testing | Weeks 9-11 | Module integration, testing, UAT |
| Phase 4: Finalization | Week 12 | Refinement, documentation, APK preparation |

## 🌍 UN SDG Alignment

This project directly contributes to **UN Sustainable Development Goal 5: Gender Equality**, specifically:

- **Target 5.2**: Eliminate all forms of violence against women and girls in public and private spheres
- **Target 5.5**: Ensure women's full and effective participation and equal opportunities for leadership

## 📈 Impact & Statistics

According to the National Crime Records Bureau (NCRB), crimes against women in India include:
- Cruelty by Husband or Relatives: 31.8%
- Assault on Women: 20.8%
- Kidnapping & Abduction: 19.2%
- Rape: 7.1%

Suraksha Kavach aims to reduce response time in emergencies and empower women with immediate access to help.

## 🛠️ Technical Highlights

### Key Components

1. **DatabaseHelper**: SQLite CRUD operations for emergency contacts
2. **EmergencyService**: Foreground service handling all emergency protocols
3. **PermissionHelper**: Centralized permission management
4. **ContactsAdapter**: RecyclerView adapter with DiffUtil for efficient updates

### Design Patterns
- Repository pattern for database access
- Observer pattern for UI updates
- Service pattern for background operations

### Security Features
- Local data storage (no cloud dependency)
- Encrypted shared preferences for settings
- Permission-based access control

## 🔮 Future Enhancements

- [ ] Voice-activated emergency trigger
- [ ] Integration with wearable devices
- [ ] Live location tracking dashboard for contacts
- [ ] Community safety map
- [ ] Multi-language support
- [ ] Fake call feature
- [ ] Video recording during emergency
- [ ] Integration with local police systems

## 🐛 Troubleshooting

### Common Issues

**App crashes on launch**
- Ensure minimum Android version is API 24 (Android 7.0)
- Clear app cache and data

**SMS not sending**
- Verify SMS permission is granted
- Check if phone has active SIM card
- Test with valid phone numbers

**Location not found**
- Enable GPS/Location services
- Grant location permissions
- Test in open area for better GPS signal

**Emergency call not working**
- Verify CALL_PHONE permission is granted
- Ensure emergency number is correct
- Check if device has network connectivity

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## Author

**Megha Dey**  
Lead Developer and Architect

## Contributors

Contributions are welcome. Please see CONTRIBUTING.md for guidelines.

## Support

For issues, questions, or contributions:
- Create an issue in the repository
- Contact project maintainers
- Refer to documentation

## Acknowledgments

- National Crime Records Bureau (NCRB) for providing crime statistics
- United Nations for Sustainable Development Goals framework
- Android developer community for open-source resources
- Contributors to women's safety initiatives worldwide

## Legal

Copyright © 2026 Megha Dey. All Rights Reserved.

Licensed under the Apache License 2.0. See LICENSE file for details.

---

**Suraksha Kavach - Technology Empowering Safety**

For questions or contributions, please refer to CONTRIBUTING.md
