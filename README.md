
# 🛡️ TPOT Honeypot Deployment on Cloud

This repository documents the full process of setting up and deploying a **TPOT Honeypot** on a cloud-based VPS. The goal is to simulate a vulnerable environment that attracts and logs malicious traffic — useful for threat intelligence, research, and learning purposes.

## 👨‍💻 Deployed & Managed by
**Emmanuel A.**  
🔗 [LinkedIn](https://www.linkedin.com/in/thedamilare) | 🌐 [GitHub](https://github.com/Cybernuel)

---

## 📌 Project Overview

The honeypot is built using the [TPOT framework](https://github.com/telekom-security/tpotce), which combines multiple honeypot sensors (e.g., Cowrie, Dionaea, and more) into a single powerful deployment. This project was deployed in the cloud for 24/7 accessibility and wider attack surface exposure.

---

## 🎥 Demo Video

Check out the full deployment walkthrough and demo below:  
🔗 **[Watch the video here]([https://your-video-link.com](https://www.linkedin.com/posts/thedamilare_cybersecurity-threathunting-tpot-activity-7349406545576628224-1pmd?utm_source=share&utm_medium=member_desktop&rcm=ACoAAFHCqjQBCBsazDmLmi-A3AQpYFgkGfGXLrs))**

---

## ☁️ Why Cloud Deployment?

Hosting the honeypot on a cloud VPS (like DigitalOcean or AWS) provides:

- ✅ Global attacker visibility  
- ✅ Separation from personal/home networks  
- ✅ Easy remote access & monitoring  
- ✅ More realistic attack simulation  

---

## ⚙️ Installation Summary

Here’s an overview of the key steps taken:

1. **Provisioned a VPS** (Ubuntu 20.04) on a secure cloud provider.
2. **Updated the system** and installed required dependencies.
3. **Cloned the TPOT repository**:
   ```bash
   git clone https://github.com/telekom-security/tpotce
   cd tpotce/iso/installer
```
````

4. **Switched to a non-root user** before installation:

   ```bash
   sudo adduser tsec
   su - tsec
   ```
5. **Ran the install script**:

   ```bash
   ./install.sh
   ```
6. **Chose deployment type** (`sensor`, `tarpit`, `mobile`, etc.).
7. Waited for TPOT to install and configure all services (\~30 mins).
8. **Accessed the dashboard** via browser:

   ```
   https://<your-vps-ip>:64297
   ```
9. **Logged in using default credentials** and updated password securely.

---

## 📊 Features & Tools Used

* 🔐 **TPOT Framework**
* 🧲 Cowrie (SSH Honeypot)
* 📡 Dionaea (Malware Collector)
* 🕸️ Suricata (Network IDS)
* 🌐 Kibana + Elasticsearch (Log Analysis)
* 📦 Docker

---

## 🧠 Lessons & Insights

Deploying TPOT helped me understand:

* Real-world attack patterns
* Network traffic analysis
* Log correlation and monitoring
* Securing cloud environments

---

## 🚀 Future Plans

* Integrate alerting via Telegram or email
* Export logs to SIEM
* Build a dashboard for visualizing honeypot activity

---

## 📬 Contact

For questions, collaboration, or setup help:

📩 Emmanuel A.
🔗 [LinkedIn](https://www.linkedin.com/in/thedamilare)
💻 [GitHub](https://github.com/Cybernuel)

---

> ⚠️ **Disclaimer:** This project is for **educational and research purposes only**. Do not use this setup to engage in malicious activity.

