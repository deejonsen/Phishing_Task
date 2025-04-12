# Phishing_Task

# Human Weakness Exploitation Simulation via BeEF & GoPhish  
**A controlled phishing and post-exploitation demonstration for educational purposes**  

---

## 📜 Overview  
This repository documents a lab simulation of a phishing campaign paired with browser exploitation using **GoPhish** (phishing framework) and **BeEF** (Browser Exploitation Framework). The project demonstrates how attackers exploit human behavior and technical vulnerabilities, while emphasizing defense strategies.  

**Key Focus Areas:**  
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
  # BeEF Installation  
  sudo apt install beef-xss  
  # GoPhish (Download binary from GitHub)  
  wget https://github.com/gophish/gophish/releases/download/v0.12.1/gophish-v0.12.1-linux-64bit.zip
  ```
Ethical Boundaries:

Only test on consented users or lab machines.

No real data exfiltration or destructive actions.

🛠️ Installation
Clone the Repository:

bash
Copy
git clone https://github.com/yourusername/human-exploit-sim.git  
cd human-exploit-sim  
Set Up GoPhish:

Unzip the GoPhish binary and configure config.json for your lab IP.

Configure BeEF:

Edit /usr/share/beef-xss/config.yaml to bind to your Kali IP.

Import Templates:

Copy email/landing page templates from GoPhish-Templates/ to GoPhish dashboard.

� Usage
Step 1: Launch GoPhish Campaign
Start GoPhish:

bash
Copy
./gophish  
Upload target list (see Metrics/sample_targets.csv).

Schedule the campaign with the BeEF-hooked landing page.

Step 2: Monitor BeEF Sessions
Start BeEF:

bash
Copy
beef-xss  
Execute demo commands on hooked browsers (e.g., fake alerts, fingerprinting).

Step 3: Analyze Metrics
Review GoPhish campaign data in Results/.

Export BeEF logs for hooked session details.

🛡️ Prevention Guidelines
For Users:
Verify sender addresses and URLs before clicking.

Use script-blocking browser extensions (e.g., uBlock Origin).

For Organizations:
Deploy email authentication (DMARC/DKIM/SPF).

Monitor traffic to suspicious endpoints (e.g., :3000/hook.js).


🤝 Contributing
This project is for educational purposes only. Contributions must adhere to:

Strict ethical testing guidelines.

No real-world phishing or unauthorized exploitation.

📄 License
MIT License - Use responsibly and only in controlled environments.

🔗 Resources
GoPhish Documentation

BeEF Framework Wiki

CISA Phishing Guidance

⚠️ Disclaimer: This project simulates attacks to improve cybersecurity awareness. Never use these techniques maliciously.
  
