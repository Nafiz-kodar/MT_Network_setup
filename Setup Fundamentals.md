# 📡 Rover & Base Station Network Setup

This repository documents the **5.8 GHz** and **900 MHz** network setups for the Rover and Base Station systems.
It includes diagrams for both setups, showing **Ethernet (blue)** and **Electrical wiring (orange)** connections.

---

## 📑 Contents
1. [5.8 GHz Network Setup — Rover End](#58-ghz-network-setup--rover-end)
2. [5.8 GHz Network Setup — Base Station](#58-ghz-network-setup--base-station)
3. [900 MHz Network Setup — Rover & Base Station](#900-mhz-network-setup--rover--base-station)
4. [System Notes & Power Requirements](#system-notes--power-requirements)

---

## 5.8 GHz Network Setup — Rover End
![5.8 GHz Rover End](images/5.8_GHz_rover.png)

The 5.8 GHz Rover End can be setup in three different setups

### 1️⃣ Setup 1 — Antenna via POE Switch
- **Power Distribution Board** supplies **24V** to:
  - **POE Injector**, which powers the **POE Switch**.
  - **POE Switch** connects directly to the **Antenna** via Ethernet.

### 2️⃣ Setup 2 — PC and Antenna via POE Splitter
- **Power Distribution Board** outputs **24V** to a **POE Splitter**.
- **POE Splitter** splits into:
  - **PC (LAN connection)**
  - POE Out -> **Antenna**

### 3️⃣ Setup 3 — Multi-device Setup
- **Power Distribution Board** sends:
  - **24V** to **POE Splitter** for the Antenna.
  - **12V** to a **Switch** for multiple PCs/devices.

## ⚠️ **WARNING**

🚨 **Make sure to power the antenna using the PoE OUT**

🚨 **Do not connect POE directly to your PC. Using the wrong port can damage the device or cause it to malfunction.**

![PoE Injector and Splitter](images/poe_injector.png)

<p align="center">
  <strong>figure: picture of POE Splitter</strong> 
</p>

---

## 5.8 GHz Network Setup — Base Station
![5.8 GHz Base Station](images/58ghz_base.png)

**Flow:**  
1. **Socket** provides power to the **POE Injector** and **Switch**.  
2. **POE Injector** sends Ethernet+Power to the **Antenna**.  
3. **Switch** distributes network to multiple PCs/devices.  

---

## 900 MHz Network Setup — Rover & Base Station
![900 MHz Rover + Base](images/900mhz_rover_base.png)
![p900 connector and xt60](images/p900_connector_xt60.png)

**Rover End**
- **Power Distribution Board** connects to the **Antenna**.
- **Antenna** communicates with **Pixhawk** using serial protocol via JST cable.

**Base Station**
- **12V buck converter** powers the **Antenna**.
- **Antenna** communicates with **PC**.

---

## System Notes & Power Requirements
- **Ethernet cables (blue)** are used for data transmission between switches, PCs, and antennas.
- **Electrical wires (orange)** deliver power to network devices.
- **POE (Power over Ethernet)** allows single-cable power + data transfer for antennas.
- **Voltage levels:**
  - **24V** for POE-powered devices.
  - **12V** for switches or specific electronics.
- The **Pixhawk** is used in the 900 MHz setup for control/data relay.

