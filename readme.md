# 📬 Spinop Mail
**The Private Inbox Command Center.**

Spinop Mail is a lightweight, Electron-based desktop application designed to bridge the gap between webmail and native performance. No accounts, no cloud tracking, and no bloat. Just your email, exactly where you need it.

[![License: MIT](https://img.shields.io/badge/License-MIT-blue.svg)](https://opensource.org/licenses/MIT)
[![Open Source Love](https://badges.frapsoft.com/os/v1/open-source.svg?v=103)](https://github.com/ellerbrock/open-source-badges/)
[![Security: Sandboxed](https://img.shields.io/badge/Security-Sandboxed-success)](https://www.electronjs.org/docs/latest/tutorial/sandbox)

---

## ✨ Why Spinop Mail?

In a world where browsers are bloated and privacy is an afterthought, Spinop Mail returns to the basics. It’s built for users who want a dedicated space for their digital life without the overhead of a standard browser.

### 🚀 Key Features
- **Zero Account Required:** No "Spinop Account" needed. Your data never leaves your machine.
- **Dynamic Inbox Management:** Add and remove Gmail, Outlook, iCloud, or Hotmail accounts with a single click.
- **Biometric Ready:** Full native support for **Windows Hello**, **TouchID**, and **1Password** for instant, passwordless logins.(UNDER DEV)
- **Home Base Protection:** Smart logout detection snaps you back to the login screen if you accidentally wander off to a generic landing page.

---

## 🛡️ Security Architecture

We believe transparency is the ultimate security feature. Spinop Mail is built on a "Trust, but Verify" model:

### 1. Isolated "Cookie Jars" (Partitions)
Unlike standard browsers where tabs often share session data, Spinop Mail utilizes unique **Persistent Partitions** for every account. 
* **The Benefit:** You can stay logged into three different Gmail accounts simultaneously without them ever seeing each other's cookies or session tokens.

### 2. Hardened URL Whitelisting
Every link clicked inside the app is vetted by our security layer.
* **Login Gates:** Authentication domains (like `login.microsoftonline.com`) are permitted internally.
* **External Links:** Anything outside the trusted ecosystem is automatically forced to your default system browser (like Brave or Chrome), keeping your local app environment safe from phishing.

### 3. Native Hardware Bridge
By disabling the standard Electron sandbox for hardware communication, we allow the app to speak directly to your computer's **TPM (Trusted Platform Module)**. This enables instant, hardware-level authentication via Passkeys.

---

## 🛠️ Getting Started

### Prerequisites
- [Node.js](https://nodejs.org/) (Latest LTS)
- NPM

### Installation
1. **Clone the repository**
   ```bash
   git clone [https://github.com/yourusername/spinop-mail.git](https://github.com/yourusername/spinop-mail.git)
   cd spinop-mail