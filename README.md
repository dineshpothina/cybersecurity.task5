# cybersecurity.task5
# 🌐 **Network Packet Analysis using Wireshark**

### 🧠 **Overview**

This project demonstrates hands-on **packet capture and network traffic analysis** using **Wireshark** on Windows.
By analyzing real-time traffic generated while streaming **Netflix**, we observe how different internet protocols — such as **DNS**, **TCP**, and **TLS** — interact to establish and secure communication between the client and remote servers.

---

## 🎯 **Objectives**

* Capture and analyze live network traffic using Wireshark.
* Identify key network protocols and their roles in data transmission.
* Understand how encrypted and unencrypted traffic appears at the packet level.
* Develop practical skills for network troubleshooting and cybersecurity analysis.

---

## ⚙️ **Tools & Environment**

| Component             | Details                   |
| --------------------- | ------------------------- |
| **Operating System**  | Windows 10                |
| **Application Used**  | Wireshark v4.6.0          |
| **Network Interface** | Wi-Fi                     |
| **Activity Captured** | Streaming Netflix content |
| **Output File**       | `Wireshark_Wi-Fi.pcapng`  |

---

## 🧩 **Procedure**

### 🪴 Step 1 — Installation

Installed **Wireshark v4.6.0** along with **Npcap** for live network capture.
Verified installation by viewing available network interfaces in the Wireshark dashboard.


---

### 📡 Step 2 — Live Packet Capture

1. Selected the **Wi-Fi interface**.
2. Began live capture and streamed Netflix for about one minute.
3. Observed thousands of packets flowing in real time (TCP, TLSv1.3, DNS, UDP).
4. Stopped the capture and saved the session as `.pcapng`.


---

### 🔍 Step 3 — Protocol Filtering & Analysis

#### 🔹 **DNS (Domain Name System)**

Filtered using `dns`

* Shows lookups like `assets.netflix.com` and `push.prod.netflix.com`.
* Demonstrates how domain names resolve to IP addresses before communication begins.

---

#### 🔹 **TCP (Transmission Control Protocol)**

Filtered using `tcp`

* Displays packet exchanges including **SYN**, **ACK**, and **FIN** flags.
* Ensures reliable data transmission between client and Netflix servers.


---

#### 🔹 **TLS (Transport Layer Security)**

Filtered using `tls`

* Indicates **encrypted streaming data**.
* Confirms secure HTTPS communication protecting user privacy.

---

### 💾 Step 4 — Exporting Capture

Saved the complete capture file as:
`Wireshark_Wi-Fi.pcapng`
This file can be reopened in Wireshark for further inspection or protocol-specific studies.

---

## 📊 **Protocol Summary**

| Protocol       | Role                                  | Observation                                  |
| -------------- | ------------------------------------- | -------------------------------------------- |
| **DNS**        | Translates domain names into IPs      | Resolved multiple Netflix domains            |
| **TCP**        | Establishes reliable sessions         | Continuous packet exchange between endpoints |
| **TLSv1.3**    | Encrypts communication                | Secured streaming session                    |
| **UDP / IGMP** | Handles multicast & streaming support | Used for performance and efficiency          |

---

## 🧠 **Insights & Learning Outcomes**

* Learned to capture and interpret live traffic in real time.
* Understood relationships between DNS, TCP, and TLS during secure streaming.
* Gained practical exposure to **Wireshark filters** and **protocol decoding**.
* Recognized how encryption (TLS) hides application-layer data but still shows metadata.

---

## 📁 **Repository Structure**

| File                     | Description                |
| ------------------------ | -------------------------- |
| `Wireshark_Wi-Fi.pcapng` | Raw packet capture file    |
| `Screenshot (6).png`     | Interface overview         |
| `Screenshot (7).png`     | Live capture view          |
| `Screenshot (8).png`     | DNS filter results         |
| `Screenshot (9).png`     | TCP packet inspection      |
| `README.md`              | Documentation and analysis |

---

## 🚀 **Conclusion**

Through this experiment, real network data from a Netflix streaming session was analyzed using Wireshark.
The exercise provided hands-on understanding of how multiple protocols coordinate to deliver seamless and secure web communication.
