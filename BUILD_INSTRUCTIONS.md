# 🔧 Build Instructions

## ✅ Fixed: Internet Permission Issue

The app was failing to load products because it was missing internet permission.

**Fixed in:** `android/app/src/main/AndroidManifest.xml`

Added:
```xml
<uses-permission android:name="android.permission.INTERNET"/>
<uses-permission android:name="android.permission.ACCESS_NETWORK_STATE"/>
```

---

## 🏗️ Building the APK

### **Step 1: Enable Developer Mode (Windows)**

You need to enable Developer Mode to build Flutter apps on Windows.

**Quick way:**
1. Press `Win + R`
2. Type: `ms-settings:developers`
3. Press Enter
4. Toggle **Developer Mode** to ON

**Manual way:**
1. Open **Settings** (Win + I)
2. Go to **Privacy & Security** → **For developers**
3. Enable **Developer Mode**
4. Restart if prompted

---

### **Step 2: Build Release APK**

After enabling Developer Mode:

```bash
cd c:\Users\PC\OneDrive\Desktop\e-commerce\ecommerce
flutter build apk --release
```

This will take 2-5 minutes.

---

### **Step 3: Find Your APK**

**Location:**
```
build/app/outputs/flutter-apk/app-release.apk
```

**Size:** ~20-25 MB (optimized)

---

## 📤 Uploading to GitHub

### **What's Excluded (via .gitignore):**

✅ Debug APKs (not needed)
✅ Build artifacts (temporary files)
✅ IDE configurations (personal settings)
✅ Dependencies (.pub-cache)

### **What's Included:**

✅ Source code (lib/)
✅ Android configuration
✅ iOS configuration
✅ pubspec.yaml
✅ README.md
✅ Release APK (optional)

---

## 🚀 Quick Commands

**Clean build:**
```bash
flutter clean
```

**Get dependencies:**
```bash
flutter pub get
```

**Build release APK:**
```bash
flutter build apk --release
```

**Build split APKs (smaller, multiple files):**
```bash
flutter build apk --split-per-abi
```

---

## 📱 Testing on Phone

### **Install APK:**
1. Transfer `app-release.apk` to your phone
2. Enable **Install from Unknown Sources** in settings
3. Tap the APK file to install
4. Open the app
5. ✅ Products should now load!

### **If Products Still Don't Load:**
- Check internet connection
- Try switching between WiFi and mobile data
- Check if API is accessible: https://fakestoreapi.com/products
- Check Android logs: `adb logcat | grep flutter`

---

## 🔍 Troubleshooting

### **"Developer Mode not enabled"**
→ Follow Step 1 above

### **"Gradle build failed"**
→ Run: `flutter clean` then rebuild

### **"SDK version mismatch"**
→ Run: `flutter doctor` and fix issues

### **Products don't load on phone**
→ Check AndroidManifest.xml has internet permissions (already fixed!)

---

## 📊 APK Information

**Release APK:**
- Size: ~20-25 MB
- Optimized: Yes
- Minified: Yes
- Tree-shaken: Yes (icons reduced 99.8%)

**Debug APK:**
- Size: ~40-50 MB
- Includes debugging symbols
- Not for distribution

---

## ✅ Checklist Before GitHub Upload

- [ ] Enable Developer Mode
- [ ] Build release APK
- [ ] Test APK on phone
- [ ] Verify products load
- [ ] All features work
- [ ] `.gitignore` is in place
- [ ] README.md is updated
- [ ] Debug files cleaned

---

## 📝 Git Commands

**Initialize repository:**
```bash
git init
git add .
git commit -m "Initial commit - E-commerce Flutter app"
```

**Push to GitHub:**
```bash
git remote add origin https://github.com/YOUR_USERNAME/REPO_NAME.git
git branch -M main
git push -u origin main
```

---

**You're all set! 🎉**
