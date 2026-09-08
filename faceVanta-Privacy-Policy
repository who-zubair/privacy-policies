# Privacy Policy for FaceVanta

**Effective Date:** August 26, 2026  
**Last Updated:** August 26, 2026  
**App:** FaceVanta (Face Shape Intelligence & Style Recommendation)  
**Developer:** Zubair  

---

## 🔒 Executive Privacy Summary

FaceVanta is designed from the ground up with a **strict on-device, zero-cloud architecture**.

* **100% On-Device Processing:** All camera frames, facial mesh landmarks (478 points), geometric ratios, symmetry scores, and shape classifications are computed locally on your device CPU/GPU.
* **No Image Storage or Uploads:** Raw camera frames are processed ephemerally in RAM and immediately discarded. No photos or biometric vectors are ever uploaded to external servers or cloud databases.
* **Zero Tracking & No Ads:** FaceVanta contains **0 advertising SDKs**, **0 behavioral analytics trackers**, and **0 telemetry libraries**.
* **Local Data Sovereignty:** All history records and preferences reside strictly inside your device's sandboxed local SQLite database. You can permanently wipe all records at any time with 1 tap.

---

## Table of Contents

1. [Information We Process & Collect](#1-information-we-process--collect)
2. [Camera Access & Real-Time Frame Lifecycle](#2-camera-access--real-time-frame-lifecycle)
3. [Facial Geometry & Biometric Data Classification](#3-facial-geometry--biometric-data-classification)
4. [Hardware-Isolated On-Device Architecture](#4-hardware-isolated-on-device-architecture)
5. [Local Data Storage & Sandboxing](#5-local-data-storage--sandboxing)
6. [What We Do NOT Collect (Explicit Boundaries)](#6-what-we-do-not-collect-explicit-boundaries)
7. [Third-Party Services & Integrations](#7-third-party-services--integrations)
8. [In-App Purchases & Subscriptions (Google Play)](#8-in-app-purchases--subscriptions-google-play)
9. [Data Retention, Control & Deletion](#9-data-retention-control--deletion)
10. [Security Standards & Safeguards](#10-security-standards--safeguards)
11. [Children’s Privacy (COPPA Compliance)](#11-childrens-privacy-coppa-compliance)
12. [International Regulations (GDPR, CCPA, BIPA)](#12-international-regulations-gdpr-ccpa-bipa)
13. [Your Rights & Data Portability](#13-your-rights--data-portability)
14. [Android System Permissions Requested](#14-android-system-permissions-requested)
15. [Google Play Developer Policy Compliance](#15-google-play-developer-policy-compliance)
16. [Modifications to This Privacy Policy](#16-modifications-to-this-privacy-policy)
17. [Developer Contact & Inquiries](#17-developer-contact--inquiries)

---

## 1. Information We Process & Collect

| Data Type | Processed / Stored | Storage Location | Shared With Third Parties |
| :--- | :--- | :--- | :--- |
| **Camera Frames (Video Preview)** | Ephemeral / RAM only | Discarded within milliseconds | **Never** |
| **478 3D Facial Landmarks** | Ephemeral / RAM only | Discarded after ratio calculation | **Never** |
| **Facial Ratios & Metrics** | Yes (Numerical only) | Local Room SQLite Database | **Never** |
| **Face Shape Classification** | Yes (e.g., "Oval", "Square") | Local Room SQLite Database | **Never** |
| **Symmetry & Vitality Scores** | Yes (Percentage 0–100%) | Local Room SQLite Database | **Never** |
| **Cropped Face Thumbnail** | Yes (Optional preview) | Local app private storage | **Never** |
| **User Styling Preferences** | Yes (Gender, Age, Goal) | Local SharedPreferences | **Never** |
| **Habit Streaks & Scan History** | Yes (Timestamps & scores) | Local Room SQLite Database | **Never** |
| **In-App Subscription Status** | Yes | Local cache + RevenueCat (Receipt verification) | Anonymous Receipt only |

---

## 2. Camera Access & Real-Time Frame Lifecycle

FaceVanta requests access to the front-facing camera solely during an active face scan session initiated by the user.

### Processing Pipeline:
1. **Frame Capture:** The front camera streams image frames into the volatile system memory (RAM).
2. **MediaPipe Landmark Extraction:** Google's on-device MediaPipe Face Mesh model estimates 478 3D landmark coordinates in real-time (<15ms per frame) on your device's CPU/GPU.
3. **Deterministic Metric Calculation:** Mathematical ratios (e.g., bizygomatic cheek width, bigonial jaw width, morphological face height, jawline angle) are computed locally.
4. **Instant Disposal:** The raw pixel data of the camera frame is **instantly purged and released from RAM**. The raw image is never saved to flash storage or transmitted over the internet.
5. **No Background Access:** The camera is never accessed in the background or without the user explicitly pressing the scan trigger.

---

## 3. Facial Geometry & Biometric Data Classification

* **No Biometric Identification or Recognition:** FaceVanta does **not** create, extract, or store facial recognition templates, faceprint vectors, or biometric identifiers capable of uniquely identifying a person.
* **Proportions Only:** The data generated consists strictly of abstract numerical proportions (e.g., `length_to_width = 1.42`) and categorical shape labels (e.g., `FaceShape.OVAL`). These numerical ratios cannot be reverse-engineered to reconstruct an individual's face or identity.
* **No Remote Transmission:** All geometric calculations remain strictly confined to the host device.

---

## 4. Hardware-Isolated On-Device Architecture

* **MediaPipe On-Device ML:** The 478-node facial mesh model is packaged directly inside the app APK and executes locally without network dependencies.
* **Offline Functionality:** Face scanning, shape classification, symmetry scoring, and style recommendations operate 100% offline in Airplane Mode.
* **No Backend Server for User Data:** FaceVanta does not operate any proprietary servers, cloud storage buckets, or remote analytics endpoints to ingest facial or user data.

---

## 5. Local Data Storage & Sandboxing

All user data is stored within the Android sandboxed application directory (`/data/data/com.learner.facevanta/`):

1. **Room SQLite Database:** Stores your scan history, symmetry progression, habit streaks, and classification dates.
2. **Android SharedPreferences:** Stores your styling preferences (Gentleman / Lady mode) and onboarding completion state.
3. **OS Sandboxing & Full-Disk Encryption:** Protected by Android's UID isolation mechanism and hardware-backed filesystem encryption. No other app on the device can access FaceVanta's private storage.

---

## 6. What We Do NOT Collect (Explicit Boundaries)

FaceVanta strictly avoids collecting the following data:

* ❌ **No Personal Identifiers:** No names, email addresses, phone numbers, or account logins.
* ❌ **No Location Data:** No GPS coordinates, Wi-Fi location, or IP-based geolocation.
* ❌ **No Device Identifiers:** No IMEI, Android ID, MAC address, or Advertising ID (GAID/AAID).
* ❌ **No Behavioral Tracking:** No event logging, session analytics, or screen recording.
* ❌ **No Social or Contact Data:** No phonebook contacts, call logs, SMS, or social media connections.
* ❌ **No Cloud Photos or Videos:** No image storage on remote servers.

---

## 7. Third-Party Services & Integrations

FaceVanta uses a minimal set of verified third-party libraries:

### Google Play In-App Billing
* **Purpose:** Processes in-app VIP subscriptions.
* **Data Flow:** All payment details, credit card numbers, and billing addresses are processed exclusively by Google Play. FaceVanta has zero access to payment details.

### RevenueCat SDK
* **Purpose:** Validates digital purchase receipts with Google Play to unlock VIP features.
* **Data Flow:** Receives only an anonymous app user ID and Google Play purchase token. **RevenueCat does not receive facial scan data, photos, or biometric measurements.**

### Google MediaPipe
* **Purpose:** On-device 478 3D landmark mesh estimation.
* **Data Flow:** Model weights run locally on device hardware. No network requests are made by MediaPipe during face scanning.

---

## 8. In-App Purchases & Subscriptions (Google Play)

* All financial transactions and recurring subscriptions (FaceVanta VIP/Pro) are managed directly by Google Play.
* Subscriptions can be managed or cancelled at any time through **Google Play Store &rarr; Account &rarr; Payments &amp; Subscriptions**.
* Users can restore active purchases anytime via the in-app Settings menu.

---

## 9. Data Retention, Control & Deletion

Users maintain 100% ownership and immediate control over all generated data:

* **Wipe Scan History:** Tapping **Settings &rarr; Wipe Scan History** immediately executes a complete database truncate, permanently erasing all scans, scores, and thumbnails.
* **App Uninstallation:** Uninstalling FaceVanta from your Android device causes the operating system to immediately and irreversibly delete the entire sandboxed database and all preferences.
* **No Account Deletion Delay:** Because FaceVanta does not require accounts or cloud storage, there is no waiting period or cloud recovery queue. Deleting locally removes all data forever.

---

## 10. Security Standards & Safeguards

* **Zero Network Attack Surface:** Because facial measurements and images never cross a network socket, they are completely immune to man-in-the-middle (MITM) attacks, cloud database leaks, or server compromises.
* **Transient RAM Lifecycle:** Camera frames are freed from memory in real-time.
* **Encrypted at Rest:** Supported by Android's hardware-backed full-disk encryption (FDE/FBE).

---

## 11. Children’s Privacy (COPPA Compliance)

FaceVanta is intended for general audiences aged 13 and older for personal grooming and style exploration. We do not knowingly collect personal information from children under 13. Given our zero-cloud, non-identifiable architecture, no personally identifiable information of any user is gathered or stored remotely.

---

## 12. International Regulations (GDPR, CCPA, BIPA)

* **GDPR (European Union):** Satisfies Privacy by Design (Article 25) and Data Minimisation (Article 5) through pure on-device edge computing. No personal data crosses international borders.
* **CCPA / CPRA (California):** FaceVanta does not sell, share, or monetize user data.
* **BIPA (Illinois):** No biometric recognition or unique identification templates are generated or stored. Facial geometry calculations are temporary and strictly local.

---

## 13. Your Rights & Data Portability

* **Right to Access:** View all your historical scans and scores directly in the app.
* **Right to Erasure:** Instantly erase all data via Settings &rarr; Wipe Scan History.
* **Right to Revoke Permissions:** Camera access can be enabled or disabled anytime in **Android Settings &rarr; Apps &rarr; FaceVanta &rarr; Permissions**.

---

## 14. Android System Permissions Requested

| Permission | Technical Name | Purpose |
| :--- | :--- | :--- |
| **Camera** | `android.permission.CAMERA` | Real-time landmark detection during an active face scan session. |
| **Internet** | `android.permission.INTERNET` | Google Play subscription status verification and receipt validation. |
| **Post Notifications** | `android.permission.POST_NOTIFICATIONS` | Optional daily scan reminders (if enabled by user). |
| **Exact Alarms** | `android.permission.SCHEDULE_EXACT_ALARM` | Precise scheduling of daily reminder notifications. |

---

## 15. Google Play Developer Policy Compliance

This Privacy Policy complies with Google Play Developer Program Policies regarding **User Data, Biometrics, Permissions, and Subscriptions**. The Play Console Data Safety questionnaire for FaceVanta reflects the zero-data-collection, local-processing model described herein.

---

## 16. Modifications to This Privacy Policy

We may update this Privacy Policy periodically. The "Last Updated" date at the top of this document will reflect the latest revision. Any updates will be published in this repository.

---

## 17. Developer Contact & Inquiries

For questions, feedback, or privacy inquiries regarding FaceVanta:

* **Developer:** Zubair
* **GitHub:** [github.com/afaan13](https://github.com/afaan13)
* **Project Repository:** [github.com/afaan13/FaceShapeIntelligence](https://github.com/afaan13/FaceShapeIntelligence)

---

*&copy; 2026 FaceVanta. All rights reserved. Built with privacy as the core foundation.*
