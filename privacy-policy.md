# SN NetTerm Privacy Policy

**Effective date:** 2026-11-20
**Last updated:** 2026-11-20

This Privacy Policy describes how **Neslihan Kevser Sakaoğlu**, trading as Soft Nova ("SN", "we", "us"), handles information in the **SN NetTerm** Android app (package `com.sn.netterm`, the "App"). SN NetTerm is a developer and network diagnostics toolbox (REST client, TCP/UDP client and server, Wake-on-LAN, ping, MQTT and NATS clients, local mock server, automation rules and home-screen widgets).

**Short version:** We do not run servers for the App, there are no user accounts, and we do not collect, receive or store the content you work with (hosts, requests, responses, credentials, logs). That content stays on your device and is sent only to the targets you choose. The App shows ads served by Google AdMob, and Google collects limited device and usage data for that purpose (Section 4). If you allow it, the App also sends crash and error reports, without your content, to Google's Firebase Crashlytics (Section 4A).

## 1. Who is responsible

- Developer: Neslihan Kevser Sakaoğlu (Soft Nova)
- Contact: softnova.global@gmail.com
- Google acts as an independent controller/processor for ad-related data under its own policies (Section 4).

## 2. Information stored on your device (not sent to us)

The App stores the following **locally on your device** so that it can work. We have no access to it.

| Data | Examples | Where / how |
|---|---|---|
| Workspaces and saved items | Workspace names, REST requests and collections, TCP/UDP/WoL/MQTT/NATS profiles, hosts, IP addresses, ports, URLs, topics, payload templates, non-secret variables | App-private database |
| Secrets | API keys, passwords, Authorization and similar header values, secret variables | Encrypted with a non-exportable key in the Android Keystore; stored in app-private storage |
| Automation rules and run history | Rule definitions, schedules, run results, status codes, short result excerpts | App-private databases; run history keeps the latest 50 runs per rule, is deleted with the rule, and is not included in backups |
| Settings | Language, theme, widget configuration | App-private preferences |
| Temporary session data | Live terminal/log views, received messages, mock-server activity | Memory and app-private storage; secret values the App recognizes are masked |

You decide what you type into the App. If you enter personal data (for example in a request body or a target URL), it remains in the App's private storage on your device.

## 3. Information sent to the targets you choose

The App's purpose is to connect to servers, devices and brokers **that you specify** (REST/HTTP(S) endpoints, TCP/UDP hosts, MQTT/NATS brokers, Wake-on-LAN and ping targets). When you run a request, connect, send a packet, or run an automation rule, the App sends the data you configured (including any credentials you entered) directly from your device to that target.

- We do not receive, proxy, log or inspect this traffic.
- The target's operator is responsible for how it handles that data; their privacy policy applies, not ours.
- **Encryption depends on your choice.** The App allows unencrypted connections (plain HTTP, raw TCP/UDP, plain MQTT/NATS) because many local and embedded devices do not support TLS. The App shows a warning for unencrypted HTTP. Do not send sensitive data over unencrypted connections. If you explicitly consent to a self-signed certificate for a request, that certificate is not verified by a public authority.
- The App can open a TCP/UDP listener or a mock HTTP server on your device **only while you start it**. Devices on your network that can reach the chosen port can connect to it. Stop the server when you no longer need it.
- Use the App only on systems and networks you own or are authorized to test.

## 4. Advertising (Google AdMob) and consent

The App is free and shows banner ads served by **Google AdMob** (Google Mobile Ads SDK). To show and measure ads, and for fraud prevention, security and analytics, Google may collect and process, through the SDK:

- Advertising ID (Android advertising identifier) and other device/app identifiers
- IP address and approximate location derived from it
- Device and OS information (model, OS version, language, screen), app information (package name, version)
- Ad interactions, diagnostics and performance data (e.g. crashes, load times)

We do not send Google any of the content described in Section 2 (no requests, responses, hosts, credentials, logs or variables are passed to ad requests). We do not receive the individual-level data Google collects.

**Consent.** In the European Economic Area, the United Kingdom and Switzerland, the App asks for your consent through Google's User Messaging Platform (UMP) before any ad is requested, and ads are not requested until consent permits it. Where a privacy-options entry is required, it is available in **Settings**, and you can change your choice at any time.

**Controls.**
- Android: Settings > Privacy > Ads lets you delete your advertising ID or opt out of ad personalization (the path varies by device and Android version).
- How Google uses data from partner apps: https://policies.google.com/technologies/partner-sites
- Google Privacy Policy: https://policies.google.com/privacy

The App does not use interstitial, rewarded or app-open ads, and does not use Google's Privacy Sandbox advertising APIs.

## 4A. Crash and error reports (Firebase Crashlytics)

If you allow it, the App sends crash reports and "application not responding" (ANR) reports to **Firebase Crashlytics**, a service of Google, so that we can find and fix bugs. This is **optional and off until you allow it**: the App asks you once on first launch, and you can change your choice at any time in **Settings**. If you turn it off, no further reports are sent.

A report may contain: the crash stack trace (code locations only; error messages are removed before sending), device model, operating system version, app version, whether the app was in the foreground, memory and storage state, and a Firebase installation identifier that Crashlytics generates to count affected devices. Reports do not include your requests, responses, hosts, URLs, credentials, variables or logs. We do not set a user ID and do not link reports to your identity (the App has no accounts).

Crashlytics does not use your Advertising ID. Google processes this data as our service provider under the Firebase terms (https://firebase.google.com/terms/crashlytics and https://firebase.google.com/support/privacy). Google keeps reports for a limited period set by Google and may process them outside your country (Section 12). We view reports in the Firebase console; we receive no other personal data through it.

Where applicable (for example in the EEA, UK and Switzerland), the legal basis is your consent, which you can withdraw in **Settings**.

## 5. Permissions

| Permission | Why |
|---|---|
| Internet, network state | Connect to your targets, load ads, check connectivity |
| Notifications (Android 13+, asked only when first needed) | Show results of automation rules and widget actions. Optional; the App works without it |
| Advertising ID (`AD_ID`) | Used by Google AdMob (Section 4) |
| Wake lock (added by the ads and scheduling libraries) | Lets scheduled work and ad measurement complete reliably |

The App does not request access to your location, contacts, camera, microphone, phone state, SMS, call logs, photos or all-files storage. Importing and exporting files uses Android's system file picker, and only the files you pick are accessed.

## 6. Backup, export and sharing

- **Android Auto Backup.** If Google backup is enabled on your device, Android may back up the App's non-sensitive workspace data (workspace structure, request templates, settings) to **your own Google account**, under Google's terms. We cannot access this backup. Secrets (API keys, passwords, tokens), logs and rule run history are excluded from backup and device transfer; after restoring on a new device you re-enter secrets. Do not store sensitive information in fields the App does not treat as secret (for example free-text names or non-secret variables).
- **Export/Import.** You can export a workspace to a file at a location you choose. Secret values are not included. Treat exported files as sensitive; we have no control over them after export.
- **Share.** If you share a log or text through the Android share sheet, it goes to the app you select.

## 7. Do we share or sell your data?

We do not sell personal data and do not share it with third parties, except (a) the Google Mobile Ads SDK, which collects and shares data with Google as described in Section 4, and (b) Firebase Crashlytics, which sends crash reports to Google as described in Section 4A, only if you allow it. We have no other analytics or third-party SDKs besides Google AdMob, Google's User Messaging Platform and Firebase Crashlytics.

## 8. Retention and deletion

- **Data we hold.** We do not store your App content on any server. If you allowed crash reports, Google keeps them in our Firebase project for a limited period set by Google. To ask us to delete crash data linked to your device, e-mail softnova.global@gmail.com; we will delete it where technically possible (the installation identifier is not linked to your identity, so we may ask for details that help locate it).
- **Crash reports.** You can turn them off at any time in Settings; reports already sent expire automatically.
- **Data on your device** stays until you delete it in the App, clear the App's storage (Android Settings > Apps > SN NetTerm > Storage > Clear data), or uninstall the App. Uninstalling removes all App data from the device, including Keystore-protected secrets.
- **Google backup.** If Android Auto Backup saved App data to your Google account, you can delete that backup yourself in your Google account or device backup settings (Google One / Google Drive > Backups > select your device > delete backup, or manage backups at https://drive.google.com/drive/backups). We cannot access or delete this backup. The App has no in-app control to delete the backup.
- **Ad-related data** processed by Google is managed by Google (https://myaccount.google.com/data-and-personalization).
- Questions: softnova.global@gmail.com.

## 9. Security

Secrets are encrypted at rest with AES-256-GCM using a non-exportable Android Keystore key (hardware-backed where the device supports it), and are excluded from backup. Authorization headers and secret values are masked in logs and exports by default. App data is stored in app-private storage not accessible to other apps on a non-rooted device. Crash reports have error messages removed before they are sent. No method is absolutely secure, and the security of data in transit depends on the protocol you choose (Section 3).

## 10. Children's privacy

The App is intended for users aged **13 and older** and is not directed to children under 13. We do not knowingly collect personal information from children under 13. We do not require an account and do not ask for names, e-mail addresses or other personal details. If you are a parent or guardian and believe a child under 13 has used the App, contact softnova.global@gmail.com.

## 11. Your rights

Depending on your location (for example under the GDPR/UK GDPR, Turkish KVKK, or CCPA/CPRA), you may have rights to access, correct, delete, restrict or object to processing of your personal data, to withdraw consent, and to complain to a supervisory authority. As we do not hold your personal data on our own servers, such requests are met through the App's local controls and the Google tools described above. You may contact softnova.global@gmail.com for any request.

## 12. International transfers

Data processed by Google for ads and for crash reports may be processed in countries other than yours, subject to Google's safeguards. We do not transfer your data ourselves.

## 13. Changes to this policy

We may update this policy, for example if the App adds features or SDKs. The new version will be published at [POLICY_URL] with an updated "Last updated" date, and for material changes we will notify you in the App or in the store listing.

## 14. Contact

Neslihan Kevser Sakaoğlu (Soft Nova)
Email: softnova.global@gmail.com
Policy URL: https://github.com/softnovaglobal/SN-NetTerm/blob/main/privacy-policy.md
