# Suraksha Kavach - Setup Guide

## 🚀 Quick Start Guide

This guide will help you get the Suraksha Kavach Android app up and running on your system.

---

## 📋 Prerequisites

Before you begin, ensure you have the following installed:

### 1. **Android Studio** (Required)
- **Download**: [https://developer.android.com/studio](https://developer.android.com/studio)
- **Minimum Version**: Hedgehog (2023.1.1) or later
- **Size**: ~1-2 GB download

### 2. **Java Development Kit (JDK)**
- Android Studio usually includes JDK
- If needed, download JDK 17 or higher
- **Link**: [https://www.oracle.com/java/technologies/downloads/](https://www.oracle.com/java/technologies/downloads/)

### 3. **System Requirements**
- **OS**: Windows 10/11, macOS 10.14+, or Linux
- **RAM**: Minimum 8GB (16GB recommended)
- **Disk Space**: At least 8GB free space
- **Processor**: Intel i5 or equivalent (or better)

---

## 📂 Project Structure Overview

```
SurakshaKavach/
├── app/                           # Main application module
│   ├── src/
│   │   ├── main/
│   │   │   ├── java/              # Kotlin source files
│   │   │   │   └── com/surakshaKavach/womensafety/
│   │   │   │       ├── MainActivity.kt              # Main app screen
│   │   │   │       ├── EmergencyContactsActivity.kt # Contact management
│   │   │   │       ├── SettingsActivity.kt          # App settings
│   │   │   │       ├── adapters/                    # RecyclerView adapters
│   │   │   │       ├── database/                    # SQLite database
│   │   │   │       ├── models/                      # Data models
│   │   │   │       ├── services/                    # Background services
│   │   │   │       └── utils/                       # Utility classes
│   │   │   ├── res/               # Resources
│   │   │   │   ├── drawable/      # Icons and images
│   │   │   │   ├── layout/        # XML layouts
│   │   │   │   ├── values/        # Strings, colors, themes
│   │   │   │   └── xml/           # Configuration files
│   │   │   └── AndroidManifest.xml # App configuration
│   │   └── build.gradle.kts       # App-level Gradle file
│   └── proguard-rules.pro         # ProGuard rules
├── gradle/                        # Gradle wrapper files
├── build.gradle.kts               # Project-level Gradle file
├── settings.gradle.kts            # Gradle settings
├── gradle.properties              # Gradle properties
├── README.md                      # Project documentation
├── SETUP_GUIDE.md                 # This file
└── .gitignore                     # Git ignore rules
```

---

## 🔧 Installation Steps

### Step 1: Download the Project
You already have the project at:
```
c:\Users\Subham.singh1\OneDrive - 365shl\final_project\SurakshaKavach
```

### Step 2: Open Android Studio
1. Launch **Android Studio**
2. If this is your first time:
   - You'll see a welcome screen
   - Click **"Open"**
3. If you have other projects open:
   - Go to **File > Open**

### Step 3: Open the Project
1. Navigate to:
   ```
   c:\Users\Subham.singh1\OneDrive - 365shl\final_project\SurakshaKavach
   ```
2. Select the `SurakshaKavach` folder
3. Click **"OK"**

### Step 4: Wait for Gradle Sync
- Android Studio will automatically start syncing Gradle
- This may take 5-10 minutes on first run
- You'll see a progress bar at the bottom
- **Wait for it to complete!** ⏳

### Step 5: Install Android SDK (if prompted)
If Android Studio prompts you to install SDK components:
1. Click **"Install"** or **"Accept"**
2. Follow the installation wizard
3. Wait for downloads to complete

### Step 6: Set Up an Android Device

#### Option A: Use Android Emulator (Virtual Device)
1. Click **Tools > Device Manager** (or the phone icon in toolbar)
2. Click **"Create Device"**
3. Select a device (e.g., **Pixel 6**)
4. Click **"Next"**
5. Select a system image:
   - Recommended: **Android 13 (API 33)** or **Android 14 (API 34)**
   - Click **"Download"** if not already installed
6. Click **"Next"**, then **"Finish"**

#### Option B: Use Physical Android Device
1. Enable **Developer Options** on your phone:
   - Go to **Settings > About Phone**
   - Tap **"Build Number"** 7 times
   - You'll see "You are now a developer!"
2. Enable **USB Debugging**:
   - Go to **Settings > Developer Options**
   - Toggle on **"USB Debugging"**
3. Connect your phone via USB cable
4. On your phone, tap **"Allow"** when prompted about USB debugging

### Step 7: Run the App
1. Click the green **"Run"** button (▶️) in the toolbar
   - Or press **Shift + F10** (Windows/Linux) or **Control + R** (Mac)
2. Select your device/emulator from the list
3. Click **"OK"**
4. Wait for the app to build and install (2-5 minutes first time)
5. The app will launch automatically! 🎉

---

## 🛠️ Troubleshooting Common Issues

### Issue 1: Gradle Sync Failed
**Error**: "Gradle sync failed: Could not resolve dependencies"

**Solution**:
1. Check your internet connection
2. Go to **File > Invalidate Caches > Invalidate and Restart**
3. Wait for Android Studio to restart
4. Try syncing again

### Issue 2: SDK Not Found
**Error**: "SDK location not found"

**Solution**:
1. Go to **File > Project Structure > SDK Location**
2. Set the Android SDK path (usually `C:\Users\<YourName>\AppData\Local\Android\Sdk` on Windows)
3. Click **"Apply"** and **"OK"**

### Issue 3: Build Failed
**Error**: Various build errors

**Solution**:
1. Click **Build > Clean Project**
2. Then click **Build > Rebuild Project**
3. Wait for the build to complete

### Issue 4: Emulator Won't Start
**Error**: Emulator fails to launch

**Solution**:
1. Ensure virtualization is enabled in BIOS (VT-x/AMD-V)
2. Try creating a new virtual device with different specs
3. Or use a physical device instead

### Issue 5: App Crashes on Launch
**Error**: App crashes immediately after installation

**Solution**:
1. Ensure your device/emulator is running **Android 7.0 (API 24)** or higher
2. Check Logcat for error messages (**View > Tool Windows > Logcat**)
3. Try uninstalling and reinstalling the app

---

## 📱 Testing the App

### First Time Setup:
1. **Grant Permissions**:
   - When the app launches, it will request permissions
   - Tap **"Grant Permissions"**
   - Allow all requested permissions:
     - ✅ Location
     - ✅ SMS
     - ✅ Phone
     - ✅ Notifications

2. **Add Emergency Contacts**:
   - Tap **"📞 Emergency Contacts"**
   - Tap the **+** button
   - Add at least one contact:
     - Name: e.g., "John Doe"
     - Phone: e.g., "+911234567890"
     - Relationship: e.g., "Brother"
   - Tap **"Add"**

3. **Configure Settings** (Optional):
   - Tap **"⚙️ Settings"**
   - Modify emergency number if needed (default: 112)
   - Customize alert message
   - Enable/disable alarm and auto-call
   - Tap **"Save Settings"**

### Testing Emergency Feature:
⚠️ **WARNING**: This will send real SMS and make real calls!

For testing without actually sending alerts:
1. Add your own phone number as a contact
2. Hold the **SOS** button for 2 seconds
3. Confirm the emergency activation
4. Check if you receive the SMS with location

**To test safely:**
- Remove actual emergency numbers from contacts during testing
- Disable auto-call in settings
- Use test phone numbers

---

## 🎨 Customization

### Change App Name:
Edit `app/src/main/res/values/strings.xml`:
```xml
<string name="app_name">Your App Name</string>
```

### Change Colors:
Edit `app/src/main/res/values/colors.xml`:
```xml
<color name="primary">#YourColorHex</color>
<color name="emergency_red">#YourRedColorHex</color>
```

### Change Emergency Number Default:
Edit `SettingsActivity.kt`:
```kotlin
const val DEFAULT_EMERGENCY_NUMBER = "Your Number"
```

---

## 📚 Learning Resources

### Android Development:
- [Official Android Developer Guide](https://developer.android.com/guide)
- [Kotlin Documentation](https://kotlinlang.org/docs/home.html)

### Material Design:
- [Material Design 3](https://m3.material.io/)

### SQLite Database:
- [SQLite Tutorial](https://www.sqlitetutorial.net/)

---

## 🆘 Getting Help

If you encounter issues:

1. **Check Logcat**: View > Tool Windows > Logcat (for error messages)
2. **Clean & Rebuild**: Build > Clean Project, then Build > Rebuild Project
3. **Update Android Studio**: Help > Check for Updates
4. **Google the Error**: Copy error message and search online
5. **Stack Overflow**: [stackoverflow.com](https://stackoverflow.com/questions/tagged/android)

---

## ✅ Next Steps After Setup

1. **Read the README.md** for feature documentation
2. **Explore the code** to understand how it works
3. **Customize the app** for your needs
4. **Test thoroughly** before real-world use
5. **Share with users** who need it

---

## 📝 Important Notes

- ⚠️ This app requires **real device permissions** to function
- 📱 Test the emergency feature carefully before real use
- 🔒 All data is stored **locally** on the device (no cloud backup)
- 🌐 Internet is **not required** for SMS and calls (only for location)
- 🔋 Emergency service runs in the **foreground** to prevent battery optimization killing it

---

## 🎯 Project Goals Checklist

- [x] User-friendly interface
- [x] Real-time location tracking
- [x] SMS alerts to multiple contacts
- [x] Emergency auto-dialer
- [x] Audible alarm
- [x] SQLite database for contacts
- [x] Settings customization
- [x] Permission management
- [x] Material Design 3 UI
- [x] Comprehensive documentation

---

**Good luck with your project! Stay safe! 🛡️**

If you need any clarification or encounter issues, refer to the **Troubleshooting** section or the README.md file.
