# Suraksha Kavach - Quick Reference Card

## 🚀 Quick Start (5 Minutes)

### For Android Studio
```bash
1. Open Android Studio
2. File > Open > Select "SurakshaKavach" folder
3. Wait for Gradle sync (5-10 min)
4. Click Run ▶️
5. Select device/emulator
6. Done! ✅
```

### First App Launch
```
1. Grant ALL permissions ✓
2. Add emergency contacts (3-5 recommended)
3. Configure settings (optional)
4. Hold SOS button for 2 seconds to test
```

---

## 📱 App Features at a Glance

| Feature | Activation | Result |
|---------|-----------|--------|
| **Emergency** | Hold SOS 2s | SMS + Call + Alarm + Vibration |
| **Add Contact** | Tap + button | Name, Phone, Relation |
| **Edit Contact** | Tap contact card | Modify details |
| **Delete Contact** | Tap trash icon | Remove contact |
| **Settings** | Settings button | Customize behavior |

---

## 🔧 Project File Structure (Simplified)

```
SurakshaKavach/
├── 📄 README.md                 # Main docs
├── 📄 SETUP_GUIDE.md            # Setup instructions
├── 📄 USER_MANUAL.md            # User guide
├── 📄 PROJECT_SUMMARY.md        # Complete summary
│
├── 🔧 build.gradle.kts          # Build config
├── ⚙️ settings.gradle.kts       # Gradle settings
│
└── 📱 app/
    ├── build.gradle.kts         # App build config
    ├── AndroidManifest.xml      # Permissions & config
    │
    ├── 💻 src/main/java/.../
    │   ├── MainActivity.kt              # Main screen
    │   ├── EmergencyContactsActivity.kt # Contacts
    │   ├── SettingsActivity.kt          # Settings
    │   ├── adapters/ContactsAdapter.kt  # List adapter
    │   ├── database/DatabaseHelper.kt   # SQLite
    │   ├── models/EmergencyContact.kt   # Data model
    │   ├── services/EmergencyService.kt # Emergency handler
    │   └── utils/PermissionHelper.kt    # Permissions
    │
    └── 🎨 res/
        ├── layout/              # XML layouts (5 files)
        ├── drawable/            # Icons (10+ files)
        ├── values/              # Colors, strings, themes
        └── mipmap-*/            # App launcher icons
```

---

## 💻 Key Code Locations

### Main Screens
```kotlin
MainActivity.kt              // Home screen with SOS button
EmergencyContactsActivity.kt // Manage contacts
SettingsActivity.kt          // App settings
```

### Core Logic
```kotlin
EmergencyService.kt          // Emergency protocol execution
DatabaseHelper.kt            // SQLite CRUD operations
PermissionHelper.kt          // Permission management
```

### UI Files
```xml
activity_main.xml            // Main layout
activity_emergency_contacts.xml // Contacts layout
activity_settings.xml        // Settings layout
```

---

## 🎨 Customization Quick Tips

### Change App Name
```xml
File: res/values/strings.xml
<string name="app_name">Your App Name</string>
```

### Change Colors
```xml
File: res/values/colors.xml
<color name="primary">#YourColor</color>
<color name="emergency_red">#DC143C</color>
```

### Change Emergency Number
```kotlin
File: SettingsActivity.kt (Line ~22)
const val DEFAULT_EMERGENCY_NUMBER = "112"
```

### Customize Alert Message
```kotlin
File: SettingsActivity.kt (Line ~23)
const val DEFAULT_ALERT_MESSAGE = "Your message"
```

---

## 🔐 Required Permissions

```xml
✓ ACCESS_FINE_LOCATION      (GPS)
✓ ACCESS_COARSE_LOCATION    (Network location)
✓ SEND_SMS                  (Send alerts)
✓ CALL_PHONE               (Emergency calls)
✓ VIBRATE                  (Vibration)
✓ FOREGROUND_SERVICE       (Background operation)
✓ INTERNET                 (Maps link)
✓ POST_NOTIFICATIONS       (Android 13+)
```

---

## 🛠️ Common Commands

### Build & Run
```bash
# Build debug APK
./gradlew assembleDebug

# Build release APK
./gradlew assembleRelease

# Install on device
./gradlew installDebug

# Run tests
./gradlew test

# Clean project
./gradlew clean
```

### Android Studio Shortcuts
```
Run App:           Shift + F10 (Win) / Ctrl + R (Mac)
Build Project:     Ctrl + F9
Clean Project:     Build > Clean Project
Sync Gradle:       File > Sync Project with Gradle Files
View Logcat:       Alt + 6
```

---

## 🐛 Quick Troubleshooting

| Problem | Quick Fix |
|---------|-----------|
| Gradle sync fails | File > Invalidate Caches > Restart |
| Build errors | Build > Clean > Rebuild |
| App crashes | Check Logcat (Alt+6) for errors |
| Permissions not working | Uninstall app, reinstall, grant again |
| Location not found | Enable GPS, test in open area |
| SMS not sending | Check SIM card, verify phone number |

---

## 📊 Database Schema

### Table: emergency_contacts
```sql
id              INTEGER PRIMARY KEY AUTOINCREMENT
name            TEXT NOT NULL
phone_number    TEXT NOT NULL
relationship    TEXT
created_at      INTEGER NOT NULL
```

### Operations
```kotlin
dbHelper.addContact(contact)        // Create
dbHelper.getAllContacts()           // Read all
dbHelper.getContactById(id)         // Read one
dbHelper.updateContact(contact)     // Update
dbHelper.deleteContact(id)          // Delete
```

---

## 🔑 Key Classes & Their Roles

| Class | Purpose | Key Methods |
|-------|---------|-------------|
| **MainActivity** | Main UI | `activateEmergency()` |
| **EmergencyService** | Emergency handler | `executeEmergencyProtocol()` |
| **DatabaseHelper** | SQLite operations | `addContact()`, `getAllContacts()` |
| **ContactsAdapter** | RecyclerView | `onBindViewHolder()` |
| **PermissionHelper** | Permissions | `hasAllPermissions()` |

---

## 📱 Testing Checklist

```
□ Install app successfully
□ Grant all permissions
□ Add 3+ emergency contacts
□ Edit a contact
□ Delete a contact
□ Change settings
□ Test emergency (with test contacts!)
□ Verify SMS received
□ Check location accuracy
□ Test alarm sound
□ Test on different Android versions
□ Test with/without internet
```

---

## 🚨 Emergency Protocol Flow

```
User Action: Hold SOS Button (2 seconds)
              ↓
System: Show Confirmation Dialog
              ↓
User: Confirm "YES"
              ↓
Parallel Execution:
    ├─→ Get GPS Location (3-10s)
    ├─→ Send SMS to all contacts (2-5s each)
    ├─→ Call emergency number (immediate)
    ├─→ Sound alarm 30s (if enabled)
    └─→ Vibrate phone (pattern)
              ↓
System: Show notification
              ↓
System: Stop service after completion
```

---

## 📚 Documentation Files

```
📄 README.md           → Technical overview, features, architecture
📄 SETUP_GUIDE.md      → Step-by-step installation guide
📄 USER_MANUAL.md      → End-user instructions & FAQ
📄 PROJECT_SUMMARY.md  → Complete project documentation
📄 QUICK_REFERENCE.md  → This file (cheat sheet)
📄 LAUNCHER_ICONS_NOTE.md → Icon customization guide
📄 LICENSE            → MIT License
```

---

## 🎯 Project Goals (Checklist)

### Core Features
- [x] Emergency panic button with confirmation
- [x] Real-time GPS location tracking
- [x] SMS alerts to multiple contacts
- [x] Emergency auto-dialer (configurable)
- [x] Audible alarm (30 seconds)
- [x] Phone vibration alerts
- [x] SQLite database for contacts
- [x] Add/Edit/Delete contacts
- [x] Settings customization
- [x] Permission management system

### Technical Requirements
- [x] Kotlin programming language
- [x] Material Design 3 UI
- [x] Minimum API 24 (Android 7.0)
- [x] Target API 34 (Android 14)
- [x] Foreground service for reliability
- [x] Local data storage (privacy)
- [x] Works offline (SMS/Call)
- [x] Comprehensive documentation

### UN SDG Alignment
- [x] Addresses SDG 5: Gender Equality
- [x] Target 5.2: Eliminate violence against women
- [x] Evidence-based (NCRB statistics)
- [x] Reduces emergency response time
- [x] Empowers women with safety tool

---

## 💡 Pro Tips

### For Developers
- Read code comments - they explain logic
- Test on real device for accurate GPS
- Use Logcat to debug issues
- Follow Kotlin coding conventions
- Keep documentation updated

### For Users
- Add trusted contacts only
- Test with willing contacts first
- Keep phone charged always
- Inform contacts they're on the list
- Practice the 2-second hold

### For Testing
- Use test numbers during development
- Disable auto-call to avoid unwanted calls
- Turn off alarm in public testing
- Verify SMS delivery thoroughly
- Test in different network conditions

---

## 🔗 Useful Links

### Android Development
- [Official Android Docs](https://developer.android.com/)
- [Kotlin Documentation](https://kotlinlang.org/docs/)
- [Material Design](https://m3.material.io/)

### Safety Resources
- India Emergency: 112
- Women Helpline: 1091
- [National Commission for Women](http://ncw.nic.in/)

---

## ⚡ One-Command Setup (After Android Studio Install)

```bash
1. Open Android Studio
2. Open Project > Navigate to SurakshaKavach folder
3. Wait for sync
4. Click Run ▶️
5. Select device
6. ✅ Done!
```

---

## 📞 Emergency Numbers by Country

```
India:      112
USA:        911
UK:         999 / 112
Canada:     911
Australia:  000 / 112
Europe:     112
UAE:        999
Singapore:  999 / 112
```

---

## ✅ Final Checklist Before Submission

```
□ Code compiles without errors
□ All features working
□ Documentation complete
□ Screenshots taken
□ APK generated and tested
□ README.md reviewed
□ License included
□ Git repository clean
□ Presentation prepared
□ Demo tested
```

---

## 🎓 Academic Presentation Points

**Key Points to Highlight:**
1. **Problem**: Women's safety crisis (NCRB data)
2. **Solution**: Fast, reliable emergency response app
3. **Tech Stack**: Kotlin, Android, SQLite, Material Design
4. **Features**: SMS, GPS, Call, Alarm - all automated
5. **Innovation**: 2-second activation, offline capable
6. **Impact**: Reduces response time, empowers women
7. **SDG**: Aligned with UN Goal 5 (Gender Equality)
8. **Scalability**: Can be extended to other regions

---

## 🚀 Version Information

```
App Version:    1.0
Build Type:     Debug/Release
Min SDK:        24 (Android 7.0)
Target SDK:     34 (Android 14)
Language:       Kotlin 1.9.20
Gradle:         8.2
Last Updated:   February 2026
```

---

**🛡️ Quick Reference Complete!**

*For detailed information, refer to the full documentation files.*

**Need Help?**
- Technical: Check SETUP_GUIDE.md
- Usage: Check USER_MANUAL.md
- Overview: Check README.md
- Complete Info: Check PROJECT_SUMMARY.md
