# Privacy Policy for Scan247 — QR & Barcode Toolkit

**Last Updated:** October 10, 2026  
**Effective Date:** October 10, 2026

Scan247 ("we," "our," or "the App") is developed and published by **[INSERT DEVELOPER / COMPANY NAME]**. We respect your privacy and are committed to protecting it. This Privacy Policy explains our practices regarding the collection, use, storage, and disclosure of information when you use the Scan247 mobile application on Android and other supported platforms.

---

## 1. Quick Summary (At a Glance)

| Feature / Data Type | Processed On-Device? | Sent to Developer Servers? | Shared with Third Parties? |
|---|---|---|---|
| **Camera Viewfinder & Live Feeds** | **Yes** (in-memory only) | **No** (Never) | **No** (Never) |
| **Photos Selected from Gallery** | **Yes** (in-memory only) | **No** (Never) | **No** (Never) |
| **Decoded Scan Content & History** | **Yes** (Saved in local device storage) | **No** (Never) | **No** (Only when you tap "Share") |
| **Favorites & App Settings** | **Yes** (Saved in local device storage) | **No** (Never) | **No** (Never) |
| **User Account & Registration** | **None** (No accounts required) | **No** | **No** |
| **Advertising Identifiers & Ad Telemetry** | No (Processed by SDK) | **No** | **Yes** (Google AdMob SDK only) |
| **Financial / Billing Information** | **None** (Not collected) | **No** | **No** |

---

## 2. Information We Do NOT Collect

Scan247 is engineered with a **privacy-first, on-device architecture**:
- **No User Accounts:** We do not require you to create an account, register, or provide your name, email address, or phone number to use the App.
- **No Remote Scan Storage:** We operate no backend servers that collect, store, or log the QR codes or barcodes you scan or create.
- **No Image or Video Uploads:** Live camera frames and photos selected from your gallery never leave your device.
- **No Location Tracking:** We do not access or collect GPS coordinates or fine location data.
- **No Contact Book Scraping:** When you generate or scan a Contact QR code (vCard/MECARD), the contact information is processed locally on your device.

---

## 3. Data Processed Locally on Your Device

### A. Camera Feeds & Barcode Scanning
- **Functionality:** The App requires access to your device camera (`android.permission.CAMERA`) to detect and decode QR codes and barcodes in real time.
- **Processing:** Scanning is performed locally on your device using the Google ML Kit Barcode Scanning library. Camera frames are processed strictly in volatile memory (RAM) and are discarded immediately after analysis.
- **Storage:** No video streams, photos, or audio recordings are saved to storage or transmitted to any remote server.

### B. Gallery / Photo Library Image Scanning
- **Functionality:** When you choose the "Scan Image" feature, the App opens your device's system photo picker (`image_picker`).
- **Processing:** Only the specific image file you manually select is accessed. The image is analyzed locally on-device by Google ML Kit to detect QR codes or barcodes.
- **Storage:** The App does not retain a copy of your photograph. After extracting the barcode or QR text, the image file is released from memory.

### C. Scan History, Favorites, and Generated Codes
- **Functionality:** For your convenience, the App maintains a local log of your recent scans, favorited items, and generated codes.
- **Storage:** All history items (including decoded values, code types, timestamps, and labels) are saved strictly in your device's private application sandbox using Android `SharedPreferences`.
- **User Control & Deletion:** You have complete control over this data. You can delete individual items or wipe the entire history at any time using the "Clear History" button in the App. Uninstalling the App permanently removes all locally stored history.
- **Export:** If you choose to export your history as a CSV file or share an individual code via Android's system share sheet, the data is shared solely through the target application you select.

### D. App Preferences & Security Settings
- User preferences such as haptic vibration feedback, audio beep toggles, dark/light theme preferences, and the Dangerous Link Protection filter are stored strictly in local device storage.
- The **Dangerous Link Protection** feature inspects URLs for suspicious patterns, IP-based hosts, or known link shorteners using local, offline heuristic rules. Scanned URLs are **not** transmitted to external link-checking servers.

---

## 4. Third-Party Services and Network Data Collection

Scan247 does not operate proprietary analytics or tracking services. However, the App integrates select industry-standard third-party SDKs:

### A. Google Mobile Ads (AdMob)
The free version of Scan247 displays banner and interstitial advertisements provided by **Google AdMob** (`google_mobile_ads`). To serve advertisements and measure ad performance, Google Mobile Ads may automatically collect and process certain data:
- **Advertising Identifiers:** Google Advertising ID (GAID / `AD_ID`) and Privacy Sandbox ad service attribution tokens.
- **Device & Telemetry Information:** Device model, operating system version, carrier, network connection type (Wi-Fi/cellular), screen dimensions, and general system language.
- **IP Address:** Used by Google to determine coarse, general geographic location (e.g., country or metropolitan area) to deliver regionally relevant ads and detect fraud.
- **Ad Interaction Data:** Views, clicks, impressions, and diagnostic data related to ad rendering.

Google processes this data in accordance with its own privacy policies:
- **Google Privacy Policy:** [https://policies.google.com/privacy](https://policies.google.com/privacy)
- **How Google uses information from apps:** [https://policies.google.com/technologies/partner-sites](https://policies.google.com/technologies/partner-sites)

**Opting Out of Personalized Ads:**
You can manage or reset your advertising identifier and opt out of personalized ads at any time through your Android device settings:
- Go to **Settings** → **Google** → **Ads** → tap **"Delete advertising ID"** or **"Reset advertising ID"**.

### B. Google Fonts
The App uses the `google_fonts` library to display modern typography. On first launch, the library may fetch font files from Google servers over HTTPS and cache them locally on your device. Google may receive standard HTTP request metadata (such as IP address and User-Agent) during this initial download.

### C. External Web Links (`url_launcher`)
When you scan a URL, email address, phone number, or map coordinate and choose an action (such as "Open Link" or "Call"), the App invokes Android's system intent to launch your default browser or dialer. Once you leave the App to visit an external website, your interactions are governed by that third-party website's privacy policy.

---

## 5. In-App Purchases and Subscriptions

Scan247 contains a toggle for "Pro Mode" in local preferences. 
- **Currently, no payment processor, Google Play Billing SDK, or third-party subscription service (such as RevenueCat) is integrated into the App.**
- The App does not collect, request, process, or store credit card numbers, bank accounts, or financial transaction data.
- If in-app purchases or subscriptions are introduced in a future update, all transactions will be processed exclusively through Google Play In-App Billing, and this policy will be updated accordingly.

---

## 6. Permissions Used by Scan247

Scan247 requests only the permissions necessary to deliver its core utility functions:

| Android Permission | Purpose in Scan247 |
|---|---|
| `android.permission.CAMERA` | Allows live camera preview for real-time QR code and barcode scanning. |
| `android.permission.FLASHLIGHT` | Allows you to toggle the device flashlight when scanning in low-light environments. |
| `android.permission.VIBRATE` | Provides subtle haptic feedback when a QR code or barcode is successfully decoded. |
| `android.permission.INTERNET` | Allows Google AdMob to load advertisements, downloads Google Fonts, and opens web URLs when you tap external links. |
| `android.permission.ACCESS_NETWORK_STATE` | Allows the AdMob SDK to verify whether an active internet connection is available before requesting ads. |
| `com.google.android.gms.permission.AD_ID` | Allows Google Mobile Ads to access the Android Advertising ID to serve ads and prevent fraud. |

You can revoke any runtime permission (such as Camera) at any time through your device's **Settings → Apps → Scan247 → Permissions**.

---

## 7. Data Retention and Deletion

- **Local Data:** Scan history and favorites remain on your device until you manually delete them. You can delete individual scans or clear all history using the built-in controls in the App. Uninstalling the App permanently deletes all local application data.
- **Third-Party Data:** Data collected by Google AdMob is retained according to Google's data retention policies (typically up to 9–18 months for advertising logs).

---

## 8. Data Security

We take data security seriously:
- All barcode scanning and image processing take place entirely on-device.
- Local data is kept inside Android's sandboxed internal storage, preventing unauthorized access by other applications on non-rooted devices.
- Network requests made by integrated SDKs (such as AdMob and Google Fonts) utilize encrypted HTTPS/TLS connections.

---

## 9. Children's Privacy

Scan247 is a general audience utility tool and is **not directed to children under 13 years of age** (or under 16 in the European Economic Area and United Kingdom). We do not knowingly collect personal identifiable information from children. If you are a parent or guardian and believe that your child has provided us with personal information, please contact us at the address below so we can investigate and address the matter.

---

## 10. Changes to This Privacy Policy

We may update this Privacy Policy periodically to reflect updates in our features, changes in integrated SDKs, or legal requirements. When changes are made:
- We will update the **"Last Updated"** date at the top of this document.
- We encourage you to review this policy periodically. Continued use of Scan247 after an update indicates your acceptance of the revised policy.

---

## 11. Contact Information

If you have questions, feedback, or concerns regarding this Privacy Policy or our data practices, please contact us at:

- **Developer / Publisher:** [INSERT DEVELOPER / COMPANY NAME]
- **Contact Email:** [INSERT SUPPORT EMAIL ADDRESS]
- **Website:** [INSERT WEBSITE URL OR GITHUB PROFILE]
- **Mailing Address:** [INSERT BUSINESS/MAILING ADDRESS, OPTIONAL]
