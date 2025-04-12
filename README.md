
# Human Weakness Exploitation Simulation via BeEF & GoPhish  
## **A Controlled Phishing and Post-Exploitation Demonstration for Educational Purposes**  

---

## 📜 Overview  
This repository documents a lab simulation of a phishing campaign paired with browser exploitation using **GoPhish** (phishing framework) and **BeEF** (Browser Exploitation Framework). The project demonstrates how attackers exploit human behavior and technical vulnerabilities, while emphasizing defense strategies.  

### **Key Focus Areas:**  
- Phishing email/landing page design  
- Browser hooking and post-click exploitation  
- Ethical attack simulation metrics  
- Awareness and prevention guidelines  

---

## 🚀 Features  
- **Realistic Phishing Simulation:**  
  - GoPhish templates for emails and landing pages.  
  - Integration of BeEF hooks for post-click browser control.  
- **Ethical Metrics Tracking:**  
  - Email open rates, click-through rates, and BeEF session data.  
- **Defense-Oriented Outputs:**  
  - Mock SOC alerts, user training material, and technical safeguards.  

---

## ⚠️ Prerequisites  
- **Virtualization Software:** VMware/VirtualBox (for Kali Linux and Metasploitable VMs).  
- **Kali Linux VM:** Pre-installed tools:

  ```bash  
  sudo apt install beef-xss       # BeEF Installation 
  wget https://github.com/gophish/gophish/releases/download/v0.12.1/gophish-v0.12.1-linux-64bit.zip 
  ```

### Ethical Boundaries:

Only test on consented users or lab machines.

No real data exfiltration or destructive actions.

---

## 🛠️ Installation

- Clone the Repository:

```bash
git clone https://github.com/gophish/gophish/releases/download/v0.12.1/gophish-v0.12.1-linux-64bit.zip 
```

- Set Up GoPhish:

Unzip the GoPhish binary and configure `config.json` for your lab IP.
```
unzip gophish-v0.12.1-linux-64bit.zip 
```
- Configure BeEF:

Edit `/usr/share/beef-xss/config.yaml` to bind to your Kali IP.

- Import Templates:

Copy email/landing page templates from `GoPhish-Templates/` to GoPhish dashboard.

## � Usage
### Step 1: Launch GoPhish Campaign
- Start GoPhish:

```bash
./gophish  
```

- Upload target list (see `Metrics/sample_targets.csv`).

- Schedule the campaign with the BeEF-hooked landing page.

### Step 2: Monitor BeEF Sessions
- Start BeEF:

```bash
sudo beef-xss  
```
- Execute demo commands on hooked browsers (e.g., fake alerts, fingerprinting).

### Step 3: Analyze Metrics
- Review GoPhish campaign data in `Results/`.

- Export BeEF logs for hooked session details.

---

## 🛡️ Prevention Guidelines
### For Users:
- Verify sender addresses and URLs before clicking.

- Use script-blocking browser extensions (e.g., uBlock Origin).

### For Organizations:
- Deploy email authentication (DMARC/DKIM/SPF).

- Monitor traffic to suspicious endpoints (e.g., :3000/hook.js).

---

## 🤝 Contributing
This project is for educational purposes only. Contributions must adhere to:

- Strict ethical testing guidelines.

- No real-world phishing or unauthorized exploitation.

## 📄 License
### MIT License - Use responsibly and only in controlled environments.

## 🔗 Resources
- [GoPhish Documentation](https://docs.getgophish.com/user-guide)
- [BeEF Framework Wiki](https://github.com/beefproject/beef/wiki)
- [CISA Phishing Guidance](https://www.cisa.gov/phishing)

#### ⚠️ Disclaimer: This project simulates attacks to improve cybersecurity awareness. Never use these techniques maliciously.
  
## Author: Dorcas Johnson

Date: 11th April, 2025

Purpose: Educational demonstration of a Controlled Phishing and Post-Exploitation.

---
