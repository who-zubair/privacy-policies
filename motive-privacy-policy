# Privacy Policy for Motive

**Last Updated:** September 8, 2026  
**Effective Date:** September 8, 2026

---

## 1. Introduction and Overview

Welcome to **Motive** ("the Application", "the App", "we", "us", or "our"). 

Motive is an offline-first personal habit, routine, and discipline tracking application built for Android. This Privacy Policy informs users of Motive regarding our principles, practices, and policies concerning the collection, use, disclosure, and protection of personal data and device information when you use our Application.

Motive was built on a foundational philosophy: **Your self-improvement journey, personal habits, routines, and daily progress belong exclusively to you.** We believe personal habit data is inherently sensitive and private. Therefore, Motive operates with an uncompromising **zero-data-collection architecture**.

---

## 2. Application Identification

* **Application Name:** Motive
* **Package Name (Application ID):** `com.learner.motive`
* **Target Operating System:** Android (Google Play Store)
* **Lead Developer / Publisher:** Zubair ([who-zubair](https://github.com/who-zubair))
* **Primary Source Code Repository / Documentation:** [https://github.com/who-zubair](https://github.com/who-zubair)

---

## 3. Core Philosophy: Offline-First & Zero Data Collection

Unlike cloud-dependent applications, Motive does not rely on external cloud databases, user authentication servers, or remote synchronizations to provide its core functionality.

* **No User Accounts:** You do not need to register, sign in, enter an email address, link a phone number, or connect social media profiles to use Motive.
* **No Remote Servers:** We do not own, operate, or lease any remote servers, cloud databases, or web backends that collect, store, or process user habit logs or personal details.
* **Zero Telemetry:** Motive does not bundle or initialize any tracking SDKs, analytics suites, crash-reporting daemons that exfiltrate data, or behavioral monitoring tools.
* **Zero Advertising Networks:** Motive is 100% ad-free. It contains zero ad network SDKs, tracking pixels, or cross-app tracking identifiers (such as Google Advertising ID / GAID).

---

## 4. Information We Do Not Collect

To be completely explicit and transparent, Motive **DOES NOT** collect, transmit, intercept, sell, share, or monetize any of the following categories of information:

1. **Personally Identifiable Information (PII):** Names, home addresses, phone numbers, email addresses, government IDs, physical characteristics, or account credentials.
2. **Health, Biometric, or Medical Information:** Fitness monitor readings, heart rates, blood pressure, sleep sensor streams, or biological metrics.
3. **Financial or Payment Information:** Credit card numbers, banking details, billing addresses, or in-app payment profiles.
4. **Geolocation Data:** Precise GPS coordinates, Wi-Fi SSID location triangulation, cell tower identifiers, or IP-based location histories.
5. **Sensor Data:** Microphones, camera feeds, gyro telemetry, or ambient environmental sensors.
6. **Device Identifiers:** Hardware serial numbers, IMEI/MEID, MAC addresses, or Advertising IDs for advertising/profiling purposes.
7. **Contact Lists or Files:** We do not read your address book, SMS messages, call logs, calendar events, photos, or documents outside of user-selected backup files.

---

## 5. Local Data Storage & Persistence

All application data created, modified, or logged within Motive is stored exclusively within your device's protected internal application sandbox directory.

### 5.1 Local SQLite Database
Motive utilizes an embedded local SQLite database (powered by the Drift persistence engine) situated within your device’s private internal storage (`/data/data/com.learner.motive/databases/app_database.sqlite`). This database stores:
* Habit titles, frequency bitmasks, schedule rules, target values, and custom units.
* Daily completion logs, numerical progress, entry timestamps, and notes.
* Momentum history calculations, streak metrics, and cached performance scores.
* Soft-deleted habits archived in your local Habit Graveyard.

### 5.2 Local Preferences
Application preferences (such as light/dark theme preference, haptic feedback toggles, and celebration animation switches) are stored locally in Android's private `SharedPreferences`.

### 5.3 Sandbox Isolation
Android's application sandboxing ensures that no other standard application installed on your device can read, query, or access Motive’s database or preferences without your explicit system-level permission or device-level root modifications.

---

## 6. Android Device Permissions and Usage

Motive adheres strictly to the Principle of Least Privilege. We only declare and request the minimum device permissions necessary to execute local user-initiated features.

| Permission | Technical Identifier | Purpose & Justification |
| :--- | :--- | :--- |
| **Post Notifications** | `android.permission.POST_NOTIFICATIONS` | Required on Android 13 (API Level 33) and higher to display on-device habit reminder notifications scheduled explicitly by you. |
| **Vibrate** | `android.permission.VIBRATE` | Enables subtle, satisfying haptic feedback when turning dials, completing habits, or toggling switches within the UI. Can be toggled off at any time in Settings. |
| **Receive Boot Completed** | `android.permission.RECEIVE_BOOT_COMPLETED` | Allows Motive’s local alarm receiver to reschedule your configured daily reminder alarms automatically after your device restarts or powers on. |
| **Exact Alarm Scheduling** | `android.permission.SCHEDULE_EXACT_ALARM` / `USE_EXACT_ALARM` | Ensures local reminder notifications fire precisely at your specified reminder time rather than being batched or delayed by system Doze modes. |

**Important Note on Network Access:** In production release builds, Motive does **not** declare or request the `android.permission.INTERNET` permission for data exfiltration or remote synchronization. The app is physically incapable of transmitting your habit records over the internet.

---

## 7. Home Screen App Widgets (`MotiveAppWidgetProvider`)

Motive provides interactive Android Home Screen App Widgets (supporting 2x2, 4x2, and 4x4 layout sizes) that allow you to track and check off habits directly from your home screen.

* **Local Inter-Process Communication (IPC):** Widgets interact with the app using Android's native `AppWidgetManager`, `RemoteViews`, and local broadcast receivers (`MotiveAppWidgetProvider` and `MotiveWidgetActionReceiver`).
* **Offline Synchronization:** All widget state transitions, checkmarks, progress calculations, and habit titles are read and updated directly against the local device storage.
* **No Remote Relays:** No third-party servers, cloud push services, or external relays are involved in rendering widget contents or capturing widget clicks.

---

## 8. Local Notification Service

Motive includes an intelligent on-device reminder engine that delivers motivational quotes and habit reminders.

* **On-Device Scheduling:** Reminders are calculated and registered locally via Android's `AlarmManager` and `NotificationManager`.
* **No Push Notification Gateways:** Motive does not connect to Google Firebase Cloud Messaging (FCM), Apple Push Notification service (APNs), OneSignal, or any remote push gateway. 
* **Full User Control:** You can enable, disable, or adjust reminders for individual habits, or silence all Motive notifications entirely through Android's system settings.

---

## 9. Data Ownership, Export, and Portability

We firmly believe in complete user data sovereignty. You own 100% of the data you input into Motive.

* **Zero Vendor Lock-In:** You are never locked into our application.
* **Comprehensive Export:** Through **Settings → Export Data**, you can download your entire database at any time in open, standardized formats:
  * **JSON Backup:** A schema-versioned, structured JSON file containing all habits, schedule rules, completion logs, notes, and momentum metadata. Suitable for full restoration or custom backups.
  * **CSV Export:** Tabular comma-separated values compatible with spreadsheet software (e.g., Microsoft Excel, Google Sheets, LibreOffice Calc) for personal data analysis and reporting.
* **Scoped Storage:** Exported files are saved to the location you choose using Android's system Storage Access Framework / File Picker. Motive only accesses the specific file or directory you select.
* **Full Import & Restoration:** You can import any previously exported Motive JSON backup to restore your habits and history cleanly without needing any cloud connection.

---

## 10. Data Retention, Habit Graveyard, and Deletion

* **Data Retention:** Because data is stored locally on your device, it remains on your device for as long as Motive remains installed, or until you explicitly delete it.
* **Soft Deletion & Habit Graveyard:** Deleting a habit moves it to the local Habit Graveyard. This allows you to restore accidentally deleted habits.
* **Permanent Purge:** You can open the Habit Graveyard at any time to permanently remove habits. When permanently deleted, all corresponding schedule rules, completions, and logs are removed from the local SQLite database.
* **Complete Uninstallation:** Uninstalling Motive through Android settings triggers Android's standard package cleanup, which deletes all local SQLite databases, cached scores, and shared preferences.

---

## 11. Third-Party Services and SDKs

Motive maintains a strict, zero-dependency policy regarding third-party commercial SDKs:

* **No Analytics SDKs:** No Google Analytics for Firebase, Mixpanel, Amplitude, Flurry, or Segment.
* **No Advertising SDKs:** No Google AdMob, Unity Ads, AppLovin, ironSource, or Meta Audience Network.
* **No Crash Exfiltration SDKs:** No Firebase Crashlytics, Sentry, Bugsnag, or Rollbar transmitting user telemetry.
* **Open Source Foundations:** Motive is constructed using trusted, transparent open-source libraries (such as the Flutter SDK, Riverpod state management, and SQLite/Drift database abstractions) compiled directly into the binary.

---

## 12. Children’s Privacy (COPPA Compliance)

Motive is a general-audience productivity and habit-building utility. Because Motive does not collect, store, transmit, or solicit any personal information from any user, it does not knowingly collect personal information from children under the age of 13 (or under 16 in the European Union), in full compliance with the **Children’s Online Privacy Protection Act (COPPA)** and Article 8 of the **GDPR**.

Parents and legal guardians can rest assured that children can safely use Motive for tracking reading, homework, sports, or chore routines without risk of personal data disclosure, profiling, or behavioral tracking.

---

## 13. European Union & UK Data Protection (GDPR / UK GDPR)

For users located within the European Economic Area (EEA) and the United Kingdom, Motive operates in full harmony with the principles of the General Data Protection Regulation (EU Regulation 2016/679) and the UK Data Protection Act 2018:

* **Data Minimization (Art. 5(1)(c)):** Motive collects zero personal data.
* **Storage Limitation (Art. 5(1)(e)):** All data resides solely on user hardware under user control.
* **Integrity and Confidentiality (Art. 5(1)(f)):** Data is secured by the operating system’s sandbox isolation.
* **Data Subject Rights (Articles 15–21):** Because Motive does not process, store, or transmit personal data to external servers, we have no mechanism to identify, query, or extract user records from a central location. You exercise your rights to access, rectification, erasure, restriction, and portability directly on your device via Motive's Export, Graveyard, and Settings features.

---

## 14. California Privacy Rights (CCPA / CPRA)

Under the California Consumer Privacy Act (CCPA) and California Privacy Rights Act (CPRA):
* **No Sale or Sharing of Personal Information:** Motive has never sold, rented, leased, or shared personal information with third parties, and will never do so.
* **No Profiling or Targeted Advertising:** Motive does not track users across third-party websites or services, nor does it conduct automated profiling.
* **No Sensitive Personal Information Disclosure:** No sensitive personal information is transmitted or held by the publisher.

---

## 15. Security Safeguards

Although Motive operates offline, we implement industry-standard software engineering safeguards to protect the integrity of your local data:
* **Operating System Sandboxing:** Android isolates the application's file system so unauthorized apps cannot read your database.
* **Input Validation & Sanitization:** All user inputs, log counts, and unit definitions are sanitized and validated against typed schema boundaries before being committed to the database.
* **Atomic Database Transactions:** Local updates and batch imports execute within atomic SQLite transactions to prevent database corruption during sudden shutdowns or battery depletion.

---

## 16. Changes to This Privacy Policy

We may periodically update this Privacy Policy to reflect modifications in application features, legal requirements, or Android platform standards.

Any modifications will be reflected by updating the **"Last Updated"** date at the top of this document. We encourage users to review this policy periodically. Because we do not collect email addresses, notices of significant revisions will be documented within app release notes on Google Play or inside the Application’s **About Motive** view.

---

## 17. Contact & Inquiries

If you have questions, feedback, or concerns regarding this Privacy Policy or Motive's privacy practices, please contact the developer:

* **Developer:** Zubair
* **GitHub Profile:** [https://github.com/who-zubair](https://github.com/who-zubair)
* **Project Issue Tracker:** [https://github.com/who-zubair](https://github.com/who-zubair)
* **Application Settings:** Navigate to **Settings → About Motive** within the app for direct version and developer details.

---

*This document serves as the official Privacy Policy for Motive on the Google Play Store and public distribution repositories.*
