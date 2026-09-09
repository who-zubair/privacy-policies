# Privacy Policy for HisaabBook

**Last Updated:** September 9, 2026  
**Effective Date:** September 9, 2026  

This Privacy Policy explains how **HisaabBook** ("we", "our", or "the App"), developed as an Android application with package name `com.learner.hisaab`, collects, uses, stores, and protects your information when you use our mobile application.

We take your privacy seriously. HisaabBook is designed with an **offline-first and privacy-focused architecture**. This means your financial records, transaction entries, and ledger details remain under your direct control at all times.

---

## 1. Information We Collect and How We Use It

### A. Financial and Ledger Data (User-Generated)
- **What We Collect:** Information you explicitly enter into the App, including borrower/lender names, transaction amounts, item descriptions (e.g., cash, books, tools), transaction dates, due dates, partial payment logs, and interest parameters.
- **How It Is Used:** To calculate balances, generate transaction ledgers, provide dashboard statistics, and schedule reminders.
- **Where It Is Stored:** By default, all ledger data is stored **locally on your device** in an encrypted/private SQLite Room Database. If you choose to sign in with your Google Account, your ledger data is synchronized to your private cloud storage via Google Cloud Firestore.

### B. Contact Information
- **What We Collect:** Name, phone number, and optionally contact photos that you select from your phone's contact list when adding a borrower or lender.
- **How It Is Used:** To associate transactions with specific individuals and enable one-tap payment reminder messaging (via WhatsApp or SMS).
- **Storage:** Contact details associated with transactions are stored locally on your device. We **never** upload your entire address book or sync contact photos to external servers.

### C. SMS Information (Bank Transaction Parsing & Reminders)
- **What We Access (Opt-in Only):**
  - **Incoming Bank SMS (`RECEIVE_SMS`, `READ_SMS`):** If you explicitly enable the automated expense tracking feature, the App locally reads incoming SMS messages from recognized financial institutions and banks to automatically record debit/credit transactions in your personal account ledger.
  - **Sending SMS (`SEND_SMS`):** If you choose to send payment reminders or balance summaries via SMS to a borrower or contact, the App sends the message using your device's default SMS provider.
- **Privacy Guarantee on SMS Data:** 
  - **All SMS parsing is executed strictly on your local device.** 
  - We **never** read personal, private, or OTP messages.
  - SMS messages, sender details, and bank SMS bodies are **never sent to external servers or shared with any third party**.
  - You can enable or disable SMS tracking at any time in Settings.

### D. Audio & Voice Data (`RECORD_AUDIO`)
- **What We Access:** Microphone audio strictly when you activate the voice input feature in the AI assistant chat screen.
- **How It Is Used:** To convert spoken input into text for quick voice logging or querying your ledger.
- **Privacy Guarantee:** Audio recordings are processed on-the-fly and are **not permanently saved, stored, or sold**.

### E. Device & Usage Information
- **What We Collect:** Basic device metadata (device model, operating system version, crash reports, and anonymous usage telemetry).
- **How It Is Used:** To troubleshoot crashes, optimize performance, and ensure compatibility across Android devices.

---

## 2. Device Permissions and Why We Need Them

In accordance with Google Play Developer Policies, HisaabBook requests only permissions essential for its core functionality:

| Permission | Purpose | Optional / Required |
| :--- | :--- | :--- |
| `android.permission.INTERNET` | Required for optional Google Sign-in, cloud backup synchronization, in-app purchases, and AI query processing. | Required for online features |
| `android.permission.READ_CONTACTS` | Allows you to quickly select a person from your contacts instead of typing their details manually. | Optional (Granted at runtime) |
| `android.permission.RECEIVE_SMS` & `android.permission.READ_SMS` | Used exclusively to detect and parse bank debit/credit transactional SMS on-device for expense tracking. | Optional (Opt-in feature) |
| `android.permission.SEND_SMS` | Used only when you trigger SMS reminders to debtors or contacts regarding pending dues. | Optional (Granted at runtime) |
| `android.permission.RECORD_AUDIO` | Enables voice-to-text recording when interacting with the in-app AI assistant. | Optional (Granted at runtime) |
| `android.permission.POST_NOTIFICATIONS` | Displays timely reminders for pending dues, payment dates, and sync notifications (Android 13+). | Optional (Granted at runtime) |
| `android.permission.USE_BIOMETRIC` | Enables App Lock using fingerprint or face authentication to secure your ledger locally. | Optional (Configured in Settings) |
| `android.permission.VIBRATE` | Provides haptic feedback during interactions. | Included in build |

You can grant or revoke these permissions at any time through your Android device settings (**Settings > Apps > HisaabBook > Permissions**).

---

## 3. Third-Party Services and Data Processors

HisaabBook integrates with trusted third-party services provided primarily by Google LLC to provide authentication, cloud sync, analytics, and billing:

1. **Google Firebase Authentication & Cloud Firestore:**
   - Provides optional Google Account sign-in and cloud backup synchronization.
   - When enabled, user data is isolated per authenticated account using server-side security rules so that only you can access your data.
   - [Google Privacy Policy](https://policies.google.com/privacy) | [Firebase Privacy & Security](https://firebase.google.com/support/privacy)

2. **Google Firebase Analytics:**
   - Collects anonymized diagnostics and app usage statistics to help us improve user experience.
   - Does not collect personal financial balances or transaction amounts.

3. **Google Play In-App Billing:**
   - Manages purchases and subscriptions for Pro features. Financial billing data (such as credit card information) is handled exclusively by Google Play; HisaabBook never receives or stores your payment card credentials.
   - [Google Play Terms of Service](https://play.google.com/intl/en-US_us/about/play-terms/)

4. **Google Generative AI (Gemini API):**
   - Powers the natural language assistant for smart financial queries and summaries.
   - Only prompts you enter or queries you submit are processed. We do not use your private financial records to train public AI models.

5. **Google ML Kit (Text Recognition):**
   - Used for on-device OCR (receipt text recognition). Processing occurs locally on your phone.

---

## 4. Data Storage, Backup, and Security

- **Offline-First Storage:** Your records are stored in a local SQLite database on your device. The app operates completely without an internet connection.
- **Cloud Backup (Optional):** If you log in with Google, your entries sync securely to Google Firebase Firestore via TLS/HTTPS encryption.
- **Manual JSON Backup & Checksum:** HisaabBook allows you to export your data as a `.json` backup file. Backups utilize a SHA-256 integrity checksum to safeguard against corruption or unauthorized tampering.
- **Biometric App Lock:** You can secure the app using your device's biometric security (fingerprint/face). Biometric authentication is handled by Android’s hardware-level biometric prompt; HisaabBook never stores or accesses your raw biometric prints.

---

## 5. Data Retention and Deletion (Account Deletion Policy)

We respect your right to completely delete your data at any time:

### A. Local Data Deletion
- You can reset or delete all local records at any time by going to **Android Settings > Apps > HisaabBook > Storage > Clear Data**, or by uninstalling the application.

### B. Cloud Account & Cloud Data Deletion
If you synced your data via Google Sign-in and wish to permanently delete your account and all associated cloud records:
1. **In-App Option:** Navigate to **Settings > Account > Delete Account / Clear Cloud Data**.
2. **Web / Email Request:** You can request the permanent deletion of your account and all associated Firestore records by emailing us at the contact address provided below with the subject line **"Request Data Deletion - HisaabBook"** using your registered Google Account email. All corresponding cloud records will be permanently purged within 30 days.

---

## 6. Children’s Privacy

HisaabBook is not directed toward children under the age of 13 (or under 16 in the European Union). We do not knowingly collect or solicit personal information from children. If you become aware that a child has provided us with personal information without parental consent, please contact us so we can take immediate action to remove the data.

---

## 7. Your Rights (GDPR & CCPA Compliance)

Depending on your jurisdiction, you have certain privacy rights regarding your personal information:
- **Right to Access & Portability:** You can export a complete copy of your ledger in JSON or CSV format at any time directly through the app.
- **Right to Rectification:** You can edit or correct any information directly within the app interface.
- **Right to Erasure ("Right to be Forgotten"):** You can delete individual entries, wipe local storage, or request full deletion of cloud records.
- **Right to Withdraw Consent:** You can revoke any previously granted Android permission via your device settings.

---

## 8. Changes to This Privacy Policy

We may update our Privacy Policy from time to time to reflect improvements to our app or changes in legal regulations. When changes are made, the "Last Updated" date at the top of this page will be revised. We recommend reviewing this policy periodically. Continued use of HisaabBook following any updates constitutes acceptance of the revised terms.

---

## 9. Contact Us

If you have questions, suggestions, or concerns regarding this Privacy Policy or your data, please contact us:

- **Developer / Project:** HisaabBook Development Team
- **GitHub Repository:** [https://github.com/afaan13/Hisaab-Book](https://github.com/afaan13/Hisaab-Book)
- **Email Contact:** `who.dev.codez@gmail.com` *(or open an inquiry via GitHub Issues)*

---
*This privacy policy meets the requirements of the Google Play Developer Distribution Agreement, Google Play User Data Policies, and global data protection standards.*
