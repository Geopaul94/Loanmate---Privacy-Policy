# Privacy Policy for LoanMate

**Effective Date:** October 2, 2026  
**Last Updated:** October 2, 2026  
**Developer:** Geo Paulson  
**Contact Email:** [geopaul94@gmail.com](mailto:geopaul94@gmail.com)  
**App Name:** LoanMate: EMI & Loan Tracker (`com.geo.loanmate`)

---

## 1. Introduction & Core Philosophy
LoanMate ("the app", "we", "us", "our") is a personal loan, EMI tracking, and calculator application developed by Geo Paulson. We respect your privacy and are committed to protecting your personal and financial data. 

**LoanMate is built with an offline-first architecture.** All financial data, loan details, calculation histories, and reminders created within the app are stored directly on your mobile device by default. We do not operate proprietary servers to store, process, or harvest your financial data.

---

## 2. Non-Financial Service Disclaimer
**LoanMate is strictly a personal record-keeping, organizer, and financial calculation tool.** 
* LoanMate **does not** lend money, originate loans, provide credit, process payments, or transfer funds.
* LoanMate **does not** connect to, sync with, or integrate with any banks, Non-Banking Financial Companies (NBFCs), credit bureaus, or financial institutions.
* Pre-defined or custom categories (e.g., Personal Loan, Car Loan, Home Loan, Gold Loan, Education Loan, Credit Card EMI, KSFE Chitty, LIC, Business Loan) are user-assigned labels strictly meant for organizing personal records. The app has no formal relationship with any third-party lenders or institutions mentioned in user-created entries.

---

## 3. Data Collection and Usage

### A. Data You Enter (Local Device Storage)
* **What Data is Handled:** Loan titles, lender names, principal amounts, interest rates, tenure/durations, EMI calculation parameters, payment logs, due dates, notes, and custom categories.
* **Where It Is Stored:** Stored securely on your device using Android's private Room (SQLite) database and `DataStore` / `EncryptedSharedPreferences`.
* **Who Accesses It:** Only you. This data remains on your physical device unless you explicitly export it or turn on cloud backup.

### B. Optional Google Drive Backup & Sync
* **User Consent:** Cloud sync is entirely optional. It is disabled by default and requires explicit user sign-in via Google OAuth (`play-services-auth`).
* **Google API Scopes Used:** Restricted scopes `drive.file` and `drive.appdata`.
* **Storage Location:** Backups are saved directly into a designated folder named `loanmate backupfile` (and app data folder) on your personal Google Drive account.
* **Data Format:** Structured JSON files containing your loan records and payment logs.
* **Developer Access:** We (the developer) **have zero access** to your Google account, credentials, or Google Drive files. The sync operates directly between your Android device and Google's official API servers.
* **Retention Policy:** LoanMate retains up to the 5 most recent backup files on your Google Drive and automatically prunes older backups to optimize storage space.
* **Revocation:** You can turn off sync inside the app Settings or revoke LoanMate's access at any time via [Google Account Security Permissions](https://myaccount.google.com/permissions).

### C. Biometric Authentication (App Lock)
* **How It Works:** LoanMate offers an optional biometric lock feature (Fingerprint / Face Unlock) to secure app access.
* **Data Handling:** Handled entirely by the Android Operating System's `BiometricPrompt` framework. LoanMate **never receives, collects, or stores** raw biometric data or security credentials; the OS simply returns a pass/fail confirmation.

### D. Local Data Export & PDF Summaries
* You can manually export your financial records as a JSON backup or generate a PDF summary using Android's `FileProvider`. These files are saved locally on your device and are shared **only when you explicitly initiate a share action** (e.g., sending via email or messaging apps).

---

## 4. Permissions Requested & Purpose

LoanMate requests only essential Android permissions required for core utility:

| Permission | Purpose |
| :--- | :--- |
| `POST_NOTIFICATIONS` | To post local EMI payment due notifications and reminders. |
| `SCHEDULE_EXACT_ALARM` | To trigger precise timely EMI reminders before payment due dates. |
| `RECEIVE_BOOT_COMPLETED` | To re-schedule active EMI payment reminders after your phone restarts. |
| `INTERNET` | Used exclusively for Google Drive cloud sync (when enabled) and checking for official app updates via Google Play. |
| `USE_BIOMETRIC` / `USE_FINGERPRINT` | To authenticate the user for optional app unlock. |
| `VIBRATE` | To provide tactile haptic feedback for user interactions and alert notifications. |

---

## 5. Third-Party Libraries & Services

LoanMate relies on a minimal set of trusted official SDKs:

* **Google Play Services (Auth & Drive v3 API):** Facilitates secure Google Sign-In and Google Drive sync.
* **Google Play In-App Updates SDK:** Checks for official software updates available on the Google Play Store.
* **Android Jetpack Libraries (Room, WorkManager, Hilt, DataStore):** Provide robust local database management and background job scheduling.

### What We DO NOT Include:
* ❌ **No Ad Networks:** Zero advertising SDKs (e.g., AdMob, Unity Ads). No user tracking for ads.
* ❌ **No Analytics SDKs:** Zero behavioral tracking (e.g., Firebase Analytics, Mixpanel, Google Analytics).
* ❌ **No External Crash Reporting:** No background log transmission to third-party crash servers (e.g., Crashlytics).
* ❌ **No Third-Party Data Sales:** We do not sell, rent, or trade your personal or financial data to any third party under any circumstances.

---

## 6. Data Security
* **On-Device:** Data is stored within Android’s isolated application sandbox and protected using industry-standard cryptography (`security-crypto`).
* **In-Transit:** All optional Google Drive sync communication is encrypted using secure HTTPS/TLS protocols directly between your device and Google servers.

---

## 7. Data Retention and Deletion

* **Deleting Local Data:** You can edit or delete individual loan entries anytime within the app. Clearing app storage via Android Settings or uninstalling LoanMate permanently removes all locally stored data.
* **Deleting Cloud Backups:** You can delete your backup folder directly from your Google Drive account, or disconnect LoanMate via your [Google Account Permissions](https://myaccount.google.com/permissions).

---

## 8. Children’s Privacy
LoanMate is a general-audience personal finance organizer intended for individuals of legal age. It is not directed toward children under 13 (or applicable local legal age). LoanMate does not knowingly request or collect data from children.

---

## 9. Changes to This Privacy Policy
We may update this Privacy Policy periodically to reflect app updates or legal requirements. Any modifications will be posted in this document with an updated **Effective Date** at the top.

---

## 10. Contact Us
If you have any questions, feedback, or concerns regarding this Privacy Policy or LoanMate's privacy practices, please contact:

**Geo Paulson**  
Developer of LoanMate  
Email: [geopaul94@gmail.com](mailto:geopaul94@gmail.com)  
Location: Kerala, India
