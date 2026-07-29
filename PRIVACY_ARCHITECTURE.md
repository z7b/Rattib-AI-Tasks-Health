# 🔒 Rattib Privacy Architecture (Privacy-First Life OS)

**Rattib** was designed and built from scratch following a strict **Privacy-First** and **Offline-First** philosophy. We believe your personal data, diaries, medical appointments, and daily tasks are highly sensitive information that should never leave your device.

This document outlines the technical details of Rattib's privacy architecture, establishing it as the most secure and reliable alternative to cloud-based productivity apps.

---

## 1️⃣ Absolute Local Storage (Zero-Cloud)
Unlike other applications (e.g., Todoist, Notion, Google Tasks) that synchronize every keystroke with their servers, **Rattib has no central user cloud database**.
- **Isar NoSQL Database:** All your data is stored in a lightning-fast, local `Isar` database encrypted within the app's secure OS Sandbox (Android/iOS).
- **Total Isolation:** No other app on your phone can access this data, and we (the developers) cannot view, pull, or access it in any shape or form.
- **Health Connect Integration:** Any health data synced (like step counts) via Google Health Connect is processed strictly on-device. Your sensitive health data NEVER leaves your phone.

---

## 2️⃣ On-Device Local AI
Most "AI-powered" apps send your texts and diary entries to external servers (like OpenAI or Google) for analysis—which is a blatant privacy violation.
- **100% Local Processing:** Rattib's built-in Smart Assistant (which suggests the *most important next step*) is a **Local Heuristics & ML algorithm** embedded directly into the app's code. It runs entirely on your phone's processor (CPU/NPU) without sending a single byte to an external server.

---

## 3️⃣ No Forced Cloud Sync
- **No Accounts Required:** The app does not require you to create an account, enter an email address, or log in to use it. You open the app and start using it instantly and completely anonymously.
- **Manual Backups:** Because we don't have servers, data responsibility lies with you. You can export your data locally and keep it safe or upload it to your personal cloud (Google Drive / iCloud) whenever you choose. We do not enforce any cloud sync mechanism.

---

## 4️⃣ UI Protection Mechanisms
- **Locked Screens & Secret Diaries:** The app features a locked diary feature to prevent intruders from viewing your private notes.
- **Screen Protector (Android):** Taking screenshots or screen recordings is blocked when you are on sensitive pages (like your diary or salary/shifts screen) to prevent accidental data leaks.

---

## 5️⃣ The ONLY Exceptions for Internet Connectivity
The app functions at 100% capacity **completely offline**. The only instances where outbound network requests occur are:
1. **Subscription Verification (In-App Purchases):** The app connects to Google Play or the App Store strictly to verify if you have purchased the Pro version.
2. **Ads & GDPR Consent (Free Version Only):** Ad requests are sent to ad networks (AdMob / Unity Ads) if you use the free version. We fully comply with the General Data Protection Regulation (GDPR) via Google's User Messaging Platform (UMP). Users in the European Economic Area (EEA) have explicit control to accept, manage, or reject personalized ads, and can revoke consent at any time from the app settings. This is entirely disabled if you upgrade to Pro.
3. **App Updates:** Checking the store for new versions.

*Your task contents, diary entries, or health data are NEVER transmitted during these connections.*

---

## Summary
**Rattib is your personal black box.** 
No cloud servers, no data harvesting, no diary tracking, and no forced synchronization. We build the tool; you own 100% of the data.
