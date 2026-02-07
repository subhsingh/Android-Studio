# Launcher Icons Guide

## Current Status
The app currently uses a simple XML-based launcher icon with a shield design.

## To Create Professional Icons

### Option 1: Use Android Studio's Asset Studio (Recommended)
1. Right-click on `app/src/main/res` in Android Studio
2. Select **New > Image Asset**
3. Choose **Launcher Icons (Adaptive and Legacy)**
4. Options:
   - **Foreground Layer**: Upload your icon image (512x512 px)
   - **Background Layer**: Choose a color or image
5. Click **Next**, then **Finish**
6. Android Studio will generate all required icon sizes automatically

### Option 2: Use Online Icon Generator
1. Visit: [https://romannurik.github.io/AndroidAssetStudio/](https://romannurik.github.io/AndroidAssetStudio/)
2. Create your launcher icon
3. Download the generated zip file
4. Extract and replace files in the `app/src/main/res/` folder

### Option 3: Manual Creation
Create icon files for each density:
- `mipmap-mdpi/ic_launcher.png` (48x48 px)
- `mipmap-hdpi/ic_launcher.png` (72x72 px)
- `mipmap-xhdpi/ic_launcher.png` (96x96 px)
- `mipmap-xxhdpi/ic_launcher.png` (144x144 px)
- `mipmap-xxxhdpi/ic_launcher.png` (192x192 px)

## Icon Design Guidelines

### Theme
- **Shield or Protection Symbol**: Represents safety
- **Primary Color**: Red (#DC143C) for emergency/alert
- **Secondary Elements**: Heart, location pin, or SOS symbol

### Design Principles (Google Material Design)
- **Simple**: Clear and recognizable at small sizes
- **Bold**: Use strong shapes and colors
- **Memorable**: Unique and distinctive
- **Scalable**: Looks good at all sizes

### Recommended Tools
- **Adobe Illustrator**: Professional vector design
- **Figma**: Free online design tool
- **Canva**: Easy-to-use template-based design
- **Inkscape**: Free open-source vector editor

## Resources
- [Material Design Icons](https://fonts.google.com/icons)
- [Flaticon](https://www.flaticon.com/) - Free icon packs
- [Icon8](https://icons8.com/) - Icon marketplace

## Current Icon Structure
```
app/src/main/res/
├── mipmap-anydpi-v26/
│   ├── ic_launcher.xml (Adaptive icon config)
│   └── ic_launcher_round.xml (Round adaptive icon)
├── drawable/
│   └── ic_launcher_foreground.xml (Foreground layer - current simple design)
└── values/
    └── ic_launcher_background.xml (Background color)
```

The current setup uses an **adaptive icon** system (Android 8.0+) with:
- **Foreground**: XML drawable with shield and SOS design
- **Background**: Solid red color (#DC143C)

This ensures the icon works across all Android versions and different launcher shapes (round, square, squircle, etc.).
