# Namana Physiotherapy Clinic - Android APK & Web App

Clinical record management, patient case sheets, consultation receipts, monthly analytics, IT returns, and dynamic cloud data synchronization.

---

## 📱 Building the Android APK on GitHub (Automated Workflow)

This repository is pre-configured with Capacitor and a complete native Android project ready to build standalone APKs on GitHub Actions.

### Method 1: Automatic Build on Push
Every time you push or merge code to `main` or `master`, the GitHub Actions workflow **"Build Android APK"** runs automatically.

### Method 2: Manual Trigger with 1 Click
1. Go to your repository on GitHub: `appnamana-png/NAMANA-APP-APK`.
2. Click on the **Actions** tab at the top.
3. In the left sidebar, click **"Build Android APK"**.
4. Click the **"Run workflow"** button on the right.
5. Choose your desired build variant (`both`, `release`, or `debug`) and click **"Run workflow"**.

### 📥 Downloading the APK:
1. Once the workflow run turns green (completed), click on it.
2. Scroll down to the **Artifacts** section at the bottom of the summary page.
3. Click on **`NamanaPhysioClinic-APK`** to download the ZIP file containing:
   - `NamanaPhysioClinic-release.apk` (Signed with debug keys for immediate installation)
   - `NamanaPhysioClinic-debug.apk`
4. Transfer the `.apk` to your Android phone, tap to install (enable "Install unknown apps" if prompted), and open the clinic app.

---

## 💻 Local Development

### 1. Web Preview
```bash
# Install dependencies
npm install

# Start local development server (binds to http://localhost:3000)
npm run dev
```

### 2. Build Web & Sync to Android
```bash
# Builds Vite web assets and syncs them into the native Android folder
npm run build:android
```

### 3. Open in Android Studio
```bash
npm run cap:open
```

### 4. Build APK Locally via Command Line
```bash
cd android
./gradlew assembleDebug
# The APK is generated at: android/app/build/outputs/apk/debug/app-debug.apk
```
