## 📡 Radio Frequency (RF) Modulation & Demodulation Using SDR

This guide covers how to modulate, demodulate, transmit, and receive RF signals using Software Defined Radio (SDR).

---

### 🔹 1. Understanding Modulation & Demodulation

**Modulation:** Converting digital or analog data into an RF signal for transmission.  
**Demodulation:** Extracting the original signal from the transmitted RF wave.

#### 📌 Types of RF Modulation

| Modulation Type | Description | Example Uses |
|---------------|-------------|-------------|
| **AM (Amplitude Modulation)** | Signal strength varies with data | AM Radio, Walkie-Talkies |
| **FM (Frequency Modulation)** | Frequency varies with data | FM Radio, Analog TV |
| **ASK (Amplitude Shift Keying)** | Digital version of AM | RFID, Infrared |
| **FSK (Frequency Shift Keying)** | Digital version of FM | Bluetooth, Pager |
| **PSK (Phase Shift Keying)** | Data encoded as phase shifts | Wi-Fi, Satellite Comm |
| **QAM (Quadrature Amplitude Modulation)** | Combination of AM & PSK | Cable TV, LTE |

---

### 🔹 2. Required Hardware for RF Signal Processing

To transmit & receive RF signals, you need an SDR device:

| Device | Function | Frequency Range |
|--------|----------|---------------|
| **RTL-SDR** | Basic RX only SDR | 24 MHz – 1.7 GHz |
| **HackRF One** | TX/RX capable SDR | 1 MHz – 6 GHz |
| **BladeRF** | High-performance SDR | 300 MHz – 3.8 GHz |
| **USRP B200/B210** | Advanced SDR for research | 70 MHz – 6 GHz |

---

### 🔹 3. Setting Up SDR Software

#### Install SDR Software on Linux/Windows

##### 🔹 Install RTL-SDR Drivers:
```bash
sudo apt update
sudo apt install rtl-sdr gqrx gnuradio
```

##### 🔹 Install HackRF Tools:
```bash
sudo apt install hackrf
```

##### 🔹 Install GNURadio & GQRX:
```bash
sudo apt install gnuradio gqrx
```

---

### 🔹 4. Receiving & Demodulating RF Signals

#### Step 1: Identify RF Signals Using GQRX
1. Open **GQRX** and select your SDR device.
2. Set frequency (e.g., **98.5 MHz for FM radio**).
3. Observe signal peaks on the spectrum.
4. Use **Mode Selection (AM/FM/USB/LSB)** to demodulate.

#### Step 2: Capture & Decode RF Signals Using Universal Radio Hacker (URH)
1. Open **URH** and set frequency.
2. Record the signal.
3. Analyze waveform (**ASK, FSK, PSK, etc.**).
4. Decode the captured data.

#### Step 3: Decode Digital RF Signals Using GNURadio
1. Open **GNURadio Companion**.
2. Add **RTL-SDR Source Block**.
3. Add **Demodulation Block (AM/FM/PSK/QAM)**.
4. Output to **Audio Sink** to hear the signal.

---

### 🔹 5. Transmitting & Modulating RF Signals

⚠️ **Warning:** Transmitting unauthorized signals is illegal in many countries. Always use a controlled test environment.

#### Step 1: Generate an RF Signal Using HackRF
Generate a test signal using `hackrf_transfer`:
```bash
hackrf_transfer -t test.wav -f 433920000 -s 2000000
```
This transmits the **test.wav** file at **433.92 MHz**.

#### Step 2: Modulate a Custom RF Signal Using GNURadio
1. Open **GNURadio Companion**.
2. Add **Signal Source Block (Sine wave)**.
3. Add **Modulation Block (FM Modulator)**.
4. Connect to **HackRF Sink** to transmit.

---

### 🔹 6. Practical RF Modulation/Demodulation Examples

| Example | SDR Device | Software |
|---------|-----------|----------|
| **Listening to FM Radio** | RTL-SDR | GQRX |
| **Sniffing & Decoding Sub-GHz Signals** | RTL-SDR, HackRF | Universal Radio Hacker |
| **Transmitting Custom RF Signal** | HackRF, BladeRF | GNURadio |
| **Recording & Replaying RF Signals** | HackRF, Flipper Zero | hackrf_transfer |
| **Decoding Bluetooth & Wi-Fi Signals** | HackRF, BladeRF | Bettercap |

---

### 🔹 7. Next Steps

✅ Install **RTL-SDR and GQRX** to start receiving signals.  
✅ Use **Universal Radio Hacker (URH)** for decoding digital RF signals.  
✅ Experiment with **GNURadio** to learn modulation techniques.  
✅ If you need transmission capabilities, use **HackRF One**.

---

### Do you need a step-by-step GNURadio project for a specific modulation type? 🚀
