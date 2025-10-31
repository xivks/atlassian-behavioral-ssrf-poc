# Atlassian Behavioral SSRF PoC (Public Safe Demo)

**Author:** Varun S (xivks)  
**Platform:** Bugcrowd (Atlassian Program)  
**Date:** Oct–Nov 2025  
**Status:** Triaged / Educational Safe Version  

---

### 🧩 Overview
This repository demonstrates a **behavioral SSRF test** performed safely on a controlled Atlassian test instance (`bugbounty-test-xivks.atlassian.net`).

The research shows how **webhook or redirect-based outbound fetchers** respond differently to:
- External URLs (success, 302 redirect)
- Internal metadata ranges (timeout / 404)
- Loopback (UNKNOWN_URL)

These behaviors validate how Atlassian’s infrastructure segregates internal vs. external network resolution — useful for researchers studying **fetch behavior and isolation boundaries**.

---

### 🧰 Artifacts
- `evidence/raw_headers_*.txt`: Actual header responses for external / internal probes  
- `evidence/webhook_request_log_redacted.png`: Safe redacted webhook log  
- `docs/behavioral_summary.md`: Test plan, timestamps, and result mapping  

---

### ⚙️ Safe Execution
No unauthorized access, brute forcing, or sensitive enumeration was performed.  
All tests use **public endpoints and benign HTTP HEAD/GET requests** only.

---

### 🪶 License
This repository is for **educational and defensive research** under a **CC BY-NC 4.0 License**.

> _“Explore responsibly — validate, don’t violate.”_
