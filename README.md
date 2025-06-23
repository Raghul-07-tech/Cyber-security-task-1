# Cyber-security-task-1
# 🔍 Network Scan with Nmap GUI (Zenmap)

This project involves performing a local network scan using **Nmap** (via the Zenmap GUI on Windows) to identify live devices, open ports, and potential security risks on a home or lab network.

---

## 📌 Objectives

1. Install and configure Nmap (Zenmap GUI)
2. Identify local IP address range
3. Run a TCP SYN scan (`-sS`) on the full subnet
4. Record IP addresses with open ports
5. Optionally analyze traffic with Wireshark
6. Research services and identify security risks
7. Save scan results for reporting

---

## 🛠 Tools Used

- 🛡️ **Nmap v7.97**
- 💻 **Zenmap GUI**
- 🌐 Windows 10 (Wi-Fi network)
- 🧪 *(Optional)* **Wireshark** for packet capture

---

## 🖥️ Scan Summary

- **Target Range**: `192.168.1.0/24`
- **Scan Type**: TCP SYN Scan (`-sS`)
- **Live Devices Found**: `192.168.1.1`, `192.168.1.3`, `192.168.1.4`, `192.168.1.7`
- **Scan Target Example**: `192.168.1.X` (your system)

---

## 🚨 Ports & Services Detected on Target

| **Port** | **Service**     | **Description**                             | **Risk Level**       |
|----------|------------------|---------------------------------------------|-----------------------|
| 135      | msrpc           | Windows RPC used for DCOM communication     | ⚠️ Medium             |
| 139      | netbios-ssn     | NetBIOS session (file/printer sharing)      | ❌ High               |
| 445      | microsoft-ds    | SMB file sharing (used in WannaCry attacks) | ❌ High               |
| 5357     | wsdapi          | Web Services for Devices API                | ⚠️ Medium             |
| 5432     | postgresql      | PostgreSQL database                         | ⚠️ Medium–High        |

---

## 🔐 Risk Evaluation Summary

- Ports **139** and **445** are known to be high-risk.
- PostgreSQL (`5432`) should be protected with authentication and firewalled.
- Ensure unused ports are closed and that all services are patched and secured.

---

## 📁 Files Included

| File Name           | Description                        | Shareable? |
|---------------------|------------------------------------|------------|
| `scan_profile.usp`  | Zenmap scan profile (contains IPs) | ⚠️ Sensitive |
| `zenmap.conf`       | Zenmap GUI configuration           | ✅ Safe     |
| `zenmap_version`    | Version info of Zenmap/Nmap        | ✅ Safe     |

---

## 📝 How to Use Zenmap

1. Open Zenmap
2. Set target to your IP range (e.g., `192.168.1.3/24`)
3. Use scan command: `nmap -sS <target>`
4. Click **Scan**
5. View results in **Ports/Hosts** tab
6. Save scan via `File → Save Scan`

---

## ⚠️ Legal Notice

Scans must only be performed on **networks you own or are authorized to analyze**. Unauthorized scanning is illegal and unethical.

---

## ✅ Task Completion

✔️ All scanning steps were completed successfully.  
✔️ Services were evaluated for risk.  
✔️ Scan results were saved and documented.

