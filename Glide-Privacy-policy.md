# Privacy Policy for Glide

**Effective Date:** November 9, 2026  
**Last Updated:** November 9, 2026  
**Application Name:** Glide (also referred to as "Glide: Edge Shortcut & Gesture Navigation")  
**Package Name:** `com.learner.glide`  
**Developer / Contact Email:** [who.dev.codez@gmail.com](mailto:who.dev.codez@gmail.com)  

---

## 1. Introduction

Glide ("we," "our," or "the app") is committed to protecting your privacy. This Privacy Policy outlines how Glide handles information on your Android device.

**Glide is built upon a fundamental privacy principle: Your device, your data.**  
Glide is an offline, on-device utility tool. We do **not** collect, store, sell, monetize, transmit, or share any personal information, usage analytics, or device identifiers with any external servers, third-party advertising networks, or analytics providers.

---

## 2. Information We Handle and How It Is Used

Glide functions entirely on your local device. The information processed by the application includes:

### A. Local User Configurations
- **What is processed:** Your customized edge handle positions, handle geometries (width, height, margins), active radial slices, quick launch app selections (Orbit Tiers), slider band settings (brightness/volume), visual themes, and excluded applications.
- **Where it is stored:** Exclusively within your device's private, sandboxed internal storage using Android `SharedPreferences`.
- **Transmission:** This data **never** leaves your device. It is never uploaded or backed up to external servers.

### B. Installed Applications List (`QUERY_ALL_PACKAGES`)
- **Purpose:** Glide provides a radial app launcher ring ("Orbit Tiers") and an app exclusion blacklist. To allow you to pick which apps appear in your shortcuts or which apps should pause edge gestures, Glide queries the list of installed applications on your device using Android's `PackageManager`.
- **Privacy Protection:** Package names, application titles, and application icons are processed solely in temporary memory (RAM) and stored in your local configuration. We do **not** transmit, monitor, or track your installed applications or your app usage habits.

---

## 3. Prominent Disclosure: Accessibility Service API Usage

Glide utilizes Android's **Accessibility Service API** (`SideShortcutAccessibilityService`) to deliver core navigation and device control features. In strict adherence to Google Play Developer Policies, we disclose the following:

### A. Purpose of Accessibility Services
Glide uses the Accessibility Service API strictly to:
1. **Execute User-Requested System Navigation Actions:**
   - Go Back (`GLOBAL_ACTION_BACK`)
   - Return to Home Screen (`GLOBAL_ACTION_HOME`)
   - Open Recent / Overview Apps (`GLOBAL_ACTION_RECENTS`)
   - Pull Down Notification Shade (`GLOBAL_ACTION_NOTIFICATIONS`)
   - Open Quick Settings Panel (`GLOBAL_ACTION_QUICK_SETTINGS`)
   - Lock the Device Screen (`GLOBAL_ACTION_LOCK_SCREEN`)
   - Trigger the Power Dialog (`GLOBAL_ACTION_POWER_DIALOG`)
   - Capture Screen Screenshot (`GLOBAL_ACTION_TAKE_SCREENSHOT`)
   - Toggle Split-Screen Multitasking (`GLOBAL_ACTION_TOGGLE_SPLIT_SCREEN`)
   - Dismiss the Notification Shade (`GLOBAL_ACTION_DISMISS_NOTIFICATION_SHADE`)
2. **Touch Passthrough Support:**
   - Detect non-gesture taps on edge trigger boundaries and dispatch them directly to underlying applications (`dispatchGesture`), ensuring normal interactions with buttons and elements located near the screen edge remain unhindered.
3. **Foreground Application Detection for App Exclusions:**
   - Detect changes in the active foreground package window (`TYPE_WINDOW_STATE_CHANGED`) solely to determine if a user-blacklisted app or keyboard is active, allowing Glide to pause edge triggers automatically.

### B. What Accessibility Services Do NOT Do:
- **No Keystroke Logging:** Glide does **not** read, log, or inspect text input, keystrokes, form entries, or search queries.
- **No Screen Content Scraping:** Glide does **not** read, analyze, capture, or record the contents of your screen, messages, emails, photos, or personal data.
- **No Credential Access:** Glide does **not** collect passwords, account credentials, or financial information.
- **No Network Transmission:** All accessibility actions are processed entirely offline within your device's local Android OS framework. Zero data is transmitted over the internet.

---

## 4. Other Android Permissions & Purpose

Glide requests only the minimum set of permissions necessary to execute features you configure:

| Permission | Purpose | Data Collection |
|---|---|---|
| `SYSTEM_ALERT_WINDOW` ("Display over other apps") | Displays the customizable edge triggers and radial overlay above running applications. | None. Used solely for local view rendering. |
| `CAMERA` & `FLASHLIGHT` | Toggles the device's physical LED torch when the Flashlight slice action is triggered. | None. Glide does **not** take photos, capture video, or access the camera sensor. |
| `WRITE_SETTINGS` | Adjusts screen brightness in real-time when using the radial brightness arc slider. | None. Used purely to write system display brightness values. |
| `ACCESS_NOTIFICATION_POLICY` | Toggles Do Not Disturb (DND) or sound/vibration ringer profiles when the Sound Mode slice is used. | None. Only modifies the system ringer mode. |
| `VIBRATE` | Provides subtle haptic feedback when you cross slice boundaries or drag to reorder items. | None. Hardware motor control only. |
| `REQUEST_IGNORE_BATTERY_OPTIMIZATIONS` | Prevents the Android operating system from killing background gesture listeners on aggressive OEM battery savers. | None. System power management only. |
| `RECEIVE_BOOT_COMPLETED` | Restarts the background edge trigger service automatically after you reboot your device. | None. |

---

## 5. Third-Party Services, SDKs, and Analytics

- **No Third-Party Analytics:** We do not integrate Google Firebase Analytics, Mixpanel, AppsFlyer, Flurry, or any other analytics tools.
- **No Advertising Networks:** Glide contains zero ads. We do not use Google AdMob, Unity Ads, Facebook Audience Network, or any advertising SDKs.
- **No Cloud Servers:** Glide does not operate remote servers, tracking endpoints, or telemetry APIs.
- **Optional Shizuku API:** For users who choose to enable privileged system toggles via Shizuku (e.g., Mobile Data Toggle, Reboot), communication occurs purely via inter-process communication (IPC) on your local device.

---

## 6. Data Security and Retention

- **Data Retention:** Because Glide stores data exclusively on your device, your settings remain on your device as long as the app is installed.
- **Data Deletion:** You can delete all data stored by Glide at any time by:
  1. Opening your device **Settings** > **Apps** > **Glide** > **Storage** > **Clear Data**.
  2. Uninstalling the Glide application, which immediately and permanently removes all associated local configurations.

---

## 7. Children's Privacy (COPPA Compliance)

Glide does not address or target anyone under the age of 13. We do not collect or solicit personal information from children. If you are a parent or guardian and have questions regarding our privacy practices, please contact us at [who.dev.codez@gmail.com](mailto:who.dev.codez@gmail.com).

---

## 8. GDPR (European Union) & CCPA / CPRA (California) Compliance

Under European (GDPR/UK GDPR) and Californian (CCPA/CPRA) privacy laws:
- **Right to Access / Portability:** All your data is stored locally in human-readable JSON within your device storage and can be exported at any time via the "Export JSON" feature in Settings.
- **Right to Erasure:** You can delete all data at any time via the "Reset Defaults" action or by clearing app storage.
- **Sale of Personal Data:** Glide **never** sells, rents, trades, or monetizes any user data.

---

## 9. Changes to This Privacy Policy

We may update this Privacy Policy from time to time to reflect changes in our practices or Android policy updates. Any updates will be posted with an updated "Last Updated" date at the top of this document and will be made accessible within the application's Settings screen.

---

## 10. Contact Us

If you have any questions, suggestions, or concerns regarding this Privacy Policy or Glide's privacy practices, please contact us at:

**Email:** [who.dev.codez@gmail.com](mailto:who.dev.codez@gmail.com)  
**Developer:** Glide Team  
