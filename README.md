# Vulnerable Mobile Apps for Penetration Testing

This repository contains three vulnerable Android applications for security testing and learning purposes: **InsecureBankv2**, **DIVA (Damn Insecure and Vulnerable App)**, and **Sieve**. These apps are designed to be intentionally vulnerable, helping penetration testers and ethical hackers practice mobile security assessment techniques.

> **Note**: These applications should **only** be used in a controlled environment for educational purposes. Never install or run these apps on your primary device or in any production environment.

---

## Table of Contents
1. [InsecureBankv2](#insecurebankv2)
2. [DIVA (Damn Insecure and Vulnerable App)](#diva)
3. [Sieve](#sieve)
4. [Tools Required](#tools-required)
5. [Lab Setup](#lab-setup)
6. [Disclaimer](#disclaimer)

---

## InsecureBankv2

**InsecureBankv2** is an Android application that simulates an insecure banking application. It is riddled with vulnerabilities, including weak encryption, improper authentication, and insecure communication.

### Features to Test:
- Insecure Data Storage
- Insecure Authentication and Session Management
- Weak Encryption Mechanisms
- Insecure Communication (e.g., HTTP instead of HTTPS)
- SQL Injection Vulnerability

### Testing Focus:
- Testing secure data storage using tools like **adb** to inspect file systems.
- Analyzing traffic using proxy tools like **Burp Suite** to identify insecure communication.
- Reverse engineering to uncover weak encryption keys and hardcoded credentials.

---

## DIVA (Damn Insecure and Vulnerable App)

**DIVA** is an Android app specifically designed for security professionals to learn about various Android app vulnerabilities. It includes multiple challenges that cover the most common security flaws in Android applications.

### Features to Test:
- Insecure Logging
- Hardcoding Issues
- Broken Cryptography
- Insecure File Storage
- Insecure WebView Implementation
- Insecure Broadcast Receivers

### Testing Focus:
- Use tools like **Drozer** and **Frida** to exploit vulnerable components.
- Reverse engineer the APK using **jadx** or **apktool**.
- Inspect the app's storage and logging mechanisms for sensitive information.

### Challenges:
- The app includes intentional security flaws to help you learn and test your skills. Try identifying and exploiting as many issues as possible.

---

## Sieve

**Sieve** is a vulnerable Android application focused on insecure data storage mechanisms. It is a great target for testing how different storage types can be exploited in Android apps.

### Features to Test:
- Insecure Database Storage
- Weak Key Management
- Poor Password Storage

### Testing Focus:
- Analyze database files and attempt to retrieve sensitive information stored on the device.
- Inspect where passwords are stored and try to decrypt or crack them.
- Look into poor encryption mechanisms used for data storage.

---

## Tools Required

For testing these applications, you will need the following tools:

- **ADB (Android Debug Bridge)** for interacting with the device and exploring storage.
- **Burp Suite** or **OWASP ZAP** for intercepting HTTP/HTTPS traffic.
- **apktool** or **jadx** for reverse engineering APKs.
- **Frida** and **Drozer** for runtime manipulation and deeper inspection.
- **Genymotion** or **Android Studio AVD** for running these APKs in a virtual Android environment.

---

## Lab Setup

### Steps:
1. **Install Virtual Environment**: Set up an Android Virtual Device (AVD) or use Genymotion for testing. Kali Linux or Parrot OS can be used for your attacker environment.
2. **Install APKs**: Install the APK files using `adb` commands:
   ```bash
   adb install InsecureBankv2.apk
   adb install diva-beta.apk
   adb install sieve.apk
---
### Disclaimer
These APKs are intentionally vulnerable and should only be used in isolated environments like virtual machines or test devices. Do not use these apps on your main phone or in any production environment, as they pose significant security risks. The purpose of these apps is to educate and help improve Android application security knowledge.

 > **Warning**: Misuse of these apps outside controlled environments could lead to severe consequences. Always adhere to ethical guidelines when using these tools for educational purposes.
