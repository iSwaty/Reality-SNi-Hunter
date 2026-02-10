# 🦅 Reality SNI Hunter

![Python](https://img.shields.io/badge/Python-3.10%2B-blue) ![License](https://img.shields.io/badge/License-MIT-green) ![Platform](https://img.shields.io/badge/Platform-Windows%20%7C%20Linux-lightgrey)

**[English](#english) | [Русский](#russian) | [简体中文](#chinese)**

---

<a name="english"></a>
## 🇺🇸 English

**Reality SNI Hunter** is an advanced scanner designed to find the perfect SNI (Server Name Indication) domains for **V2Ray/Xray Reality** protocol.

Unlike simple scanners that check random IPs, this tool uses a "Topology-aware" algorithm. It scans subnets physically close to your VPS to ensure the SNI traffic looks indistinguishable from legitimate traffic routed to the same datacenter.

### ✨ Key Features
*   **Neighbor Scanning:** Scans IP ranges (±5 subnets) adjacent to your VPS.
*   **Distance Scoring:** Calculates a score based on Latency + Numerical Distance. Finds IPs on the "same switch".
*   **ASN Matching:** Highlights IPs belonging to the same Autonomous System as your VPS (Green mark).
*   **H2 & TLS 1.3 Verified:** Strictly checks for HTTP/2 and TLS 1.3 support (required for Reality).
*   **Smart Filtering:** 
    *   Removes "junk" domains (k8s, traefik, default, test).
    *   Rejects domains behind Cloudflare/CDNs.
    *   Expands wildcards (`*.site.com` → `site.com`).
*   **Modern GUI:** Dark theme, sortable columns, JSON/TXT export.

### 🚀 How to Run
**Windows (Pre-built):**
Download the `.exe` from the [Releases](https://github.com/YOUR_USERNAME/Reality-SNI-Hunter/releases) page.

**From Source:**
```bash
pip install -r requirements.txt
python main.py
