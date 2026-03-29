\# 🚀 Portable DNS Ad-Blocking System (Pi-hole + Tailscale)



\## 📌 Overview



This project implements a DNS-based ad-blocking system using Pi-hole, with remote access enabled via Tailscale. It allows filtering ads and trackers across devices without requiring router-level access.



\---



\## 🧠 Architecture



```

Laptop (Manual DNS: 192.168.1.9)

&#x20;       ↓

&#x20;    Pi-hole

&#x20;       ↓

&#x20;  Cloudflare DNS

&#x20;       ↓

&#x20;    Internet



Remote Access:

Laptop → Tailscale → Raspberry Pi

```



\---



\## ⚙️ Tech Stack



\* Pi-hole (DNS filtering)

\* Tailscale (VPN overlay network)

\* Raspberry Pi (server)

\* Linux



\---



\## 🔥 Key Features



\* DNS-level ad and tracker blocking

\* Real-time query monitoring

\* Remote access using Tailscale

\* Manual DNS configuration (no router access required)



\---



\## ⚠️ Challenges \& Solutions



\### ❌ Issue: Slow / broken internet with Tailscale DNS override



\* Root cause: Full DNS routing through VPN increased latency



\### ✅ Solution:



\* Disabled Tailscale DNS override

\* Implemented manual DNS configuration



\---



\### ❌ Issue: Network instability due to hotspot setup



\* Root cause: Double NAT and routing loops



\### ✅ Solution:



\* Connected Raspberry Pi and laptop to same router



\---



\## 📊 Results



\* Total Queries: 500+

\* Ads Blocked: \~7–10%

\* Stable and fast browsing experience



\---



\## ⚠️ Limitations



\* Cannot block YouTube ads

\* DNS over HTTPS (DoH) can bypass filtering

\* Requires manual DNS setup



\---



\## 📸 Screenshots



!\[Pi-hole Dashboard](screenshot.png)



\---



\## 🧠 Learnings



\* DNS fundamentals and routing

\* VPN-based networking (Tailscale)

\* Debugging real-world network issues

\* System design under constraints



\---



\## 🚀 Future Improvements



\* Add Grafana dashboard

\* Dockerize setup

\* Automate blocklist updates



