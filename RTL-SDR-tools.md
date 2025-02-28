## 🔹 RF Ethical Hacking & Security Testing Guide

RF hacking involves analyzing, intercepting, and manipulating wireless signals such as Wi-Fi, Bluetooth, RFID, NFC, and Sub-GHz frequencies.

---

### 📌 1. Required Hardware for RF Hacking

To start with RF security testing, you'll need specific devices:

| Device | Purpose |
|--------|---------|
| **HackRF One** | Wideband SDR for TX/RX (1 MHz–6 GHz) |
| **RTL-SDR** | Cheap SDR for RX only (24 MHz–1.7 GHz) |
| **YARD Stick One** | Sub-GHz attacks (e.g., car key fobs) |
| **Flipper Zero** | Multipurpose RF tool (NFC, IR, Sub-GHz, Bluetooth) |
| **Proxmark3 RDV4** | RFID cloning/hacking |
| **CrazyRadio PA** | Bluetooth Low Energy (BLE) sniffing |
| **Wi-Fi Pineapple** | Wi-Fi pentesting |
| **ESP8266 / ESP32** | Deauthentication & packet injection |
| **BladeRF** | Advanced SDR for GSM/4G attacks |
| **HackRF Portapack** | Standalone SDR hacking device |

---

### 📌 2. Software & Tools

Install these tools based on your target frequency range:

| Tool | Function |
|------|----------|
| **GQRX / SDR#** | RF signal visualization |
| **Universal Radio Hacker (URH)** | RF reverse engineering |
| **GNURadio** | Custom RF signal processing |
| **Flipper Zero Sub-GHz** | Signal sniffing & replay |
| **YARD Stick One Tools** | Sub-GHz RF manipulation |
| **Proxmark3 Software** | RFID/NFC cloning |
| **Kismet** | Wi-Fi & Bluetooth sniffing |
| **Bettercap** | Bluetooth & Wi-Fi MITM attacks |
| **Wireshark** | Packet analysis (Wi-Fi, BLE, etc.) |

---

### 📌 3. RF Hacking Attack Scenarios

#### 🔹 A. Sniffing & Intercepting Signals
1. Use **HackRF One + GQRX** to visualize signals.
2. Identify frequency using **rtl_power** (for RTL-SDR).
3. Decode the signal using **Universal Radio Hacker (URH)**.

#### 🔹 B. Replay Attacks (Sub-GHz & Remote Controls)
1. Record a signal (e.g., car key fob) with **HackRF**.
2. Replay it using **hackrf_transfer**.
3. Can also use **Flipper Zero** for replay attacks.

#### 🔹 C. Wi-Fi Deauthentication & MITM
1. **ESP8266 / ESP32** to send deauth packets.
2. **Wi-Fi Pineapple** for MITM attacks & rogue APs.
3. Use **Bettercap** for Bluetooth sniffing.

#### 🔹 D. Bluetooth Low Energy (BLE) Attacks
1. **CrazyRadio PA** for BLE sniffing.
2. **Bettercap or BLEAH** for MITM attacks.

#### 🔹 E. NFC/RFID Cloning
1. **Proxmark3** for RFID/NFC tag cloning.
2. Dump and emulate card data using **proxmark3 client**.

#### 🔹 F. GSM & LTE Security Testing
1. Use **BladeRF** for setting up a rogue GSM base station.
2. Test mobile network vulnerabilities.

---

### 📌 4. Legal & Ethical Considerations

⚠️ **Warning:** RF hacking can violate laws like the **Wireless Telegraphy Act**. Always:

✅ Get **proper authorization** before testing.  
✅ Use **RF shielding boxes** for testing.  
✅ Follow **ethical hacking guidelines**.

---

### 📌 5. Your Next Steps

🔹 Pick a device (**e.g., Flipper Zero, HackRF, or RTL-SDR**).  
🔹 Learn **signal analysis** (**GQRX, SDR#**).  
🔹 Start **sniffing & decoding RF signals** (**URH, Bettercap**).  
🔹 Try **penetration testing** on your own devices.

---

### Would you like a detailed tutorial for a specific device? 🚀
