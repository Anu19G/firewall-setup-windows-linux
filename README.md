# Firewall Setup and Testing — Windows & Kali Linux

This repository contains a complete step-by-step guide for configuring, testing, and resetting firewalls on **Windows** and **Kali Linux**.  

---

## 📌 Tools Used
- **Windows Firewall with Advanced Security**
- **PowerShell**
- **UFW (Uncomplicated Firewall)** on Kali Linux
- **Test-NetConnection** (Windows)

---

## 📂 Repository Structure
The repository includes:
- **Windows folder** — baseline firewall profile status file, exported firewall rules CSV, and GUI screenshots.  
- **Linux folder** — UFW baseline status file and terminal screenshots.  
- **Documentation folder** — full internship report in PDF format.  
- **README.md** — this documentation file.
  
---

## 🛠️ Task Summary

### **Windows Firewall Configuration**
1. **Baseline Capture**
   - Recorded firewall profile status (Domain, Private, Public).
   - Exported all existing firewall rules.
   - Captured screenshots from GUI and Advanced Security console.

2. **Inbound Rule Creation**
   - Blocked Telnet (TCP port 23) inbound traffic.
   - Verified block using `Test-NetConnection`.

3. **Outbound Rule Creation**
   - Blocked access to `flipkart.com` using IP-based rule.
   - Verified block by attempting to access the site in a browser.

4. **Cleanup**
   - Removed all custom rules and restored baseline.

---

### **Linux Firewall (UFW) Configuration**
1. **Installation & Enabling**
   - Installed UFW.
   - Enabled and captured initial baseline status.

2. **Rule Creation**
   - Allowed HTTP traffic (TCP port 80).
   - Denied Telnet traffic (TCP port 23).
   - Added advanced rules:
     - Limited SSH login attempts.
     - Allowed SSH only from a specific IP.
     - Set default policy to deny incoming, allow outgoing.

3. **Testing**
   - Verified rules using `nc`, `nmap`, and HTTP server.
   - Confirmed allowed and blocked traffic behavior.

4. **Reset**
   - Reset UFW to default settings.
   - Re-enabled firewall with open defaults.

---

## 📷 Screenshots
Evidence for each step is stored in:
- **Windows/screenshots/** → GUI & PowerShell evidence.
- **Linux/screenshots/** → Terminal outputs & UFW status.

---

## 🔍 Key Learning Outcomes
- Understanding of **firewall concepts** (inbound, outbound, profiles, default policies).
- Practical skills in **port blocking, IP restrictions, and service-specific rules**.
- Ability to test firewall rules using **both local and cross-system methods**.
- Knowledge of restoring and resetting firewall configurations.
