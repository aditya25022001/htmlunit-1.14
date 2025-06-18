# HtmlUnit 1.14 (Patched)

This repository is a **patched and upgraded version of HtmlUnit 1.14**, originally released on 2008-01-09 but not published to OSS repositories. This fork is intended to modernize the build and test process, fix known vulnerabilities, and ensure compatibility with Java 8 and modern websites.

---

## 📦 Source

The original `htmlunit-1.14` source code was obtained from: [Sourceforge HtmlUnit 1.14](https://sourceforge.net/projects/htmlunit/files/htmlunit/1.14/)

> **Note**: HtmlUnit 1.14 is not published to Maven Central or other public OSS repositories.

---

## What’s Updated in This Fork

### 🔐 CVE Fix
- **Patched**: [CVE-2023-26119](https://nvd.nist.gov/vuln/detail/CVE-2023-26119) — a vulnerability in how JavaScript could execute unintended code in older versions.

### 🧪 Test Case Compatibility
- Updated test cases to use **current and accessible URLs**.
- Rewritten tests to avoid JavaScript-heavy sites that block bots or use dynamic scripts incompatible with HtmlUnit.

### 🚀 Build System Improvements
- **Java version upgraded**: from Java 1.4 → **Java 8**
- Removed deprecated plugins like:
    - `maven-clover-plugin` (no longer maintained)
- Updated plugin versions:
    - `maven-checkstyle-plugin`: `2.2-SNAPSHOT` → **`3.1.2`**

### 📁 Resources
- Added missing **resource files** for running test cases, including:
    - HTML samples
    - Unicode/non-ASCII files for upload tests
    - Local test assets for page simulation

---

## 🧰 How to Build

Make sure you have Java 8 and Maven 3.6+ installed.

```bash
mvn clean install
