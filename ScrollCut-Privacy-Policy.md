# Privacy Policy for ScrollCut

**Last Updated: September 2026**

---

## 1. Introduction

ScrollCut ("the App") is developed and maintained by ZUBAIR ("Developer", "we", "us", or "our"). This Privacy Policy explains how the App collects, uses, stores, protects, and shares (or does not share) information when you install and use ScrollCut on your Android device. By downloading, installing, or using the App, you agree to this Privacy Policy. If you do not agree with the terms described herein, please uninstall the App immediately.

---

## 2. Data Collection & Storage

ScrollCut operates on a **LOCAL-FIRST, OFFLINE-ONLY** data model. All data collected by the App is stored exclusively on your device's local storage using Android's Room database and SharedPreferences. We do **NOT** collect, transmit, upload, or store any personal data on remote servers, cloud infrastructure, or any third-party services.

Specifically, the App stores:

- **App usage statistics**: Time spent per app, launch counts, session durations
- **User-configured app restriction rules**: Time limits, schedules
- **Streak and points data**: Daily compliance tracking
- **Settings preferences**: Theme, notification preferences, fitness challenge toggles
- **Device admin enrollment status**: For screen-lock enforcement only
- **Focus and wellness session history**: Breathing exercises, eye-care reminders

**None of this data ever leaves your device.**

---

## 3. Permissions & Their Purpose

ScrollCut requests the following Android permissions, each strictly necessary for core functionality:

### PACKAGE_USAGE_STATS (Usage Access)
Required to monitor per-app screen time. This is the core permission that enables ScrollCut to track how long you use each app. Android's UsageStatsManager API provides aggregated, read-only statistics. ScrollCut **cannot** read your messages, photos, files, or any in-app content.

### SYSTEM_ALERT_WINDOW (Draw Over Other Apps)
Required to display intervention overlays when an app's time limit is reached. The overlay blocks the restricted app and provides options to close or extend usage. This permission does **NOT** allow ScrollCut to read what is on your screen.

### FOREGROUND_SERVICE
Required to run the monitoring service that tracks real-time usage and triggers interventions. The service runs with a persistent notification so Android does not terminate it.

### POST_NOTIFICATIONS
Used to send warning nudges before an app's time limit is reached and to display the persistent monitoring notification.

### RECEIVE_BOOT_COMPLETED
Allows ScrollCut to automatically restart its monitoring service after device reboot, ensuring continuous protection.

### DEVICE_ADMIN (Optional)
If enabled, allows ScrollCut to lock the device screen as a fitness-challenge enforcement mechanism. This is entirely opt-in and can be disabled at any time from Settings.

### ACCESSIBILITY_SERVICE (If applicable)
Used solely to detect app launches for real-time usage tracking. ScrollCut does **not** read screen content, keystrokes, or interact with other apps' UI elements through this service.

---

## 4. Data Processing & Usage

All data processing occurs entirely on-device. The App:

- Calculates daily, weekly, and monthly usage statistics locally
- Computes streak scores and compliance points using local algorithms
- Generates insights and focus scores from locally stored usage data
- Determines when to trigger intervention overlays based on local time-limit rules

**No data is processed on external servers. No machine learning models are trained on your data. No analytics are sent to any third party.**

---

## 5. Data Sharing

ScrollCut does **NOT** share, sell, lease, rent, trade, or transfer any user data to any third party under any circumstances. This includes:

- No advertising networks or ad SDKs are integrated
- No analytics services (Google Analytics, Firebase Analytics, Mixpanel, etc.) are integrated
- No crash reporting services that transmit data are used
- No social media SDKs are integrated
- No data brokers or marketing partners receive any data

**The App operates in complete data isolation on your device.**

---

## 6. Data Export & Deletion

You have full control over your data:

### Export
You can export all your usage data as a JSON file from **Settings > Privacy & Data > Export Usage Data**. This creates a local file on your device that you can review, archive, or delete.

### Deletion
You can permanently delete all stored data from **Settings > Privacy & Data > Reset All Data**. This action is irreversible and removes all usage history, streak data, configured rules, and preferences.

### Uninstallation
Uninstalling ScrollCut from your device automatically removes all associated local data, as the App uses Android's standard app-specific storage.

---

## 7. Children's Privacy

ScrollCut is not directed at children under the age of 13. We do not knowingly collect personal information from children. The App is designed as a general-purpose digital wellness tool for users of all ages. Since no data is transmitted from the device, no age-specific data collection concerns apply. Parents or guardians may install and configure ScrollCut on a child's device to help manage screen time.

---

## 8. Security Measures

Your data is protected by:

- **Android's built-in app sandboxing**: No other app can access ScrollCut's data
- **Encrypted SharedPreferences**: For sensitive configuration data
- **Private internal storage**: Room database stored in the app's private internal storage directory
- **No network endpoints**: No APIs or cloud connections that could be exploited
- **Device Admin enrollment**: When enabled, provides additional tamper resistance

Since no data leaves your device, there are no server-side security concerns, no risk of data breaches from cloud infrastructure, and no man-in-the-middle attack vectors.

---

## 9. Third-Party Services

ScrollCut does not integrate any third-party services that collect or process user data. The App uses only Android's built-in system APIs (UsageStatsManager, AlarmManager, NotificationManager, DevicePolicyManager) and open-source libraries (Jetpack Compose, Room, Hilt, Lottie for animations). None of these transmit user data externally.

---

## 10. Changes to This Policy

We may update this Privacy Policy from time to time. Any changes will be reflected in the "Last updated" date at the top of this document and will be distributed through app updates on Google Play. Continued use of the App after policy changes constitutes acceptance of the updated terms. We encourage you to review this policy periodically.

---

## 11. Your Rights

Under applicable data protection regulations (including GDPR, CCPA, and similar frameworks), you have the right to:

- **Access**: All data the App stores about you (via the Export function)
- **Delete**: All data the App stores about you (via the Reset function)
- **Restrict processing**: By disabling monitoring or uninstalling the App
- **Data portability**: Via JSON export

Since all data is local and no data is transmitted, many traditional data-subject-request workflows are simplified: you can exercise all rights directly from within the App without contacting us.

---

## 12. Contact

If you have any questions, concerns, or requests regarding this Privacy Policy or the App's data practices, please contact us at:

**Developer:** ZUBAIR  
**Email:** who.dev.codez@gmail.com

We are committed to addressing any privacy concerns promptly and transparently.

---

*© 2026 ZUBAIR. All rights reserved.*
