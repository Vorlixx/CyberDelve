# CyberDelve 🔥 Ultimate Bug Hunter Tool

**The most powerful client-side bug hunting platform, developed in Azerbaijan 🇦🇿**

A fully client-side JavaScript analysis tool that discovers API endpoints, secrets (API keys, JWT tokens, credit cards), and vulnerabilities (XSS, SQLi, LFI, prototype pollution) from HTML/JS files — **no backend, no installation, no server required.**

---

## 🚀 Features

| Category | Feature |
|----------|---------|
| 🔍 **Deep JS Analysis** | Scans all referenced JS files from dropped HTML |
| 🔑 **Secret Detection** | Firebase, AWS, Stripe, GitHub, Slack, JWT, private keys, credit cards |
| ⚡ **Vulnerability Scanner** | DOM XSS, code injection, open redirect, prototype pollution, LFI |
| 🔴 **Smart Risk Tagging** | 🔥 Critical / ⚠ High / ● Medium / · Low |
| 🔍 **Live Endpoint Check** | Test all discovered endpoints in real-time |
| ⚡ **Parameter Fuzzing** | Discovers hidden functionality via brute-force parameters |
| 🔐 **Auth Bypass Test** | SQL injection payloads against login/admin endpoints |
| 🤖 **AI Assistant** | Analyzes findings, identifies real threats vs placeholders, gives recommendations |
| 📝 **Bug Bounty Report** | Auto-generates structured security reports (download as .txt) |
| 📄 **Multi-Format Export** | TXT, JSON, CSV, **Nuclei YAML**, **Burp Suite JSON** |
| 📜 **Community Templates** | Pre-built XSS, SQLi, LFI, SSTI, SSRF, XXE payloads (click to copy) |
| 🌍 **Bilingual UI** | Azerbaijani 🇦🇿 / English 🇬🇧 |
| 🎨 **Professional UI** | Dark matrix aesthetic, neon glow effects, glass cards |

---

## 🛠 How to Use

### Step 1: Get the HTML file

Open the target website in your browser → press `Ctrl+U` (view page source) → press `Ctrl+S` (save as `.html`)

### Step 2: Drop it into CyberDelve

Drag & drop the saved `.html` file onto the drop zone — the tool automatically finds and analyzes all JavaScript files referenced in the page.

> 💡 You can also drop `.js`, `.ts`, `.jsx`, `.json` files directly.

### Step 3: Analyze the results

| Tab | What it does |
|-----|--------------|
| 📊 **Results** | All discovered endpoints and secrets — filter by type or risk level |
| 🔴 **Vulnerabilities** | Detected XSS, injections, open redirects — with file & line number |
| 🤖 **AI Analysis** | Click "Analyze" for intelligent evaluation of all findings |
| 📜 **Templates** | Pre-built test payloads — click "Use" to copy to clipboard |
| 📝 **Report** | Generate a complete bug bounty report and download as .txt |

---

## 🔍 What It Finds

### Secrets & Credentials

| Type | Example Pattern | Risk |
|------|----------------|------|
| Firebase API Key | `AIza...` | 🔥 Critical |
| AWS Access Key | `AKIA...` | 🔥 Critical |
| GitHub Token | `ghp_...` / `ghs_...` | 🔥 Critical |
| Stripe Live Key | `sk_live_...` | 🔥 Critical |
| Stripe Test Key | `sk_test_...` | ⚠ Medium |
| Slack Token | `xox[baprs]-...` | 🔥 Critical |
| JWT Token | `eyJ...` | 🔥 Critical |
| Private Key | `-----BEGIN PRIVATE KEY-----` | 🔥 Critical |
| Credit Card | Visa / MasterCard / AMEX / Discover | 🔥 Critical |
| Database URI | `mongodb://`, `postgres://` | ⚠ High |

### Vulnerabilities

| Type | Severity |
|------|----------|
| `.innerHTML` Assignment | 🔴 Critical |
| `eval()` Execution | 🔴 Critical |
| `document.write()` | 🔴 Critical |
| `new Function()` Call | 🔴 Critical |
| Open Redirect | 🟡 Medium |
| Prototype Pollution | 🟠 High |
| `postMessage` Issues | 🟡 Medium |
| Sensitive Data in `localStorage` | 🟡 Medium |
| Console Log Leak | 🟢 Low |

---

## ⚡ Risk Levels

| Level | Color | Meaning |
|-------|-------|---------|
| 🔥 **Critical** | Red | Real API key, JWT, credit card — immediate action required |
| ⚠ **High** | Orange | Admin panel, auth endpoint, database URI |
| ● **Medium** | Yellow | API endpoints, user data — should be investigated |
| · **Low** | Gray | Static files, images, fonts — usually safe |

---

## 📦 Export Formats

| Format | Purpose |
|--------|---------|
| 📄 **.txt** | Plain text for manual review |
| 📋 **.json** | Structured data for other tools |
| 📊 **.csv** | Import into Excel / Google Sheets |
| ⚡ **Nuclei YAML** | Directly import into Nuclei scanner |
| 🕷️ **Burp JSON** | Import into Burp Suite Professional |

---

## ⚙️ Requirements

- A modern browser (Chrome, Firefox, Edge, Safari)
- Internet connection (for Tailwind CSS CDN)
- **No server, no backend, no installation**

---

## 🛠 Running Locally

```bash
# Simply open the file
open index.html

# Or use VS Code Live Server
npx live-server

# Or Python HTTP server
python3 -m http.server 8080
# → http://localhost:8080
