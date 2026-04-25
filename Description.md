

### 1. Connections Diagram

| Sensor Type | ESP32 Pin | Wiring Instructions |
| :--- | :--- | :--- |
| **Danger Button** | **Pin 4** | Connect a tactile button between **Pin 4** and **3.3V**. |
| **Water Sensor** | **Pin 5** | Connect two open-ended wires: one to **Pin 5** and one to **3.3V**. |
| **Fire Sensor** | **Pin 23** | Run a wire (loop) directly from **3.3V** into **Pin 23**. |
| **Common Ground** | **GND** | Ensure all components share the ESP32 Ground if using external power. |

---

### 2. Short Description
**Child Safety Monitor:** A physical hardware-based safety monitor that detects environmental emergencies via three dedicated digital triggers. It provides real-time visual alerts through a hosted web dashboard, ensuring constant surveillance of a child's immediate surroundings.

---

### 3. How It Works
* **Fire Logic:** Uses a "Dead-Man's Switch" concept. Pin 23 must always receive 3.3V power. If a fire burns the wire, the signal is lost (becomes LOW), and the website alerts **"BABY ON FIRE."**
* **Water Logic:** Uses conductivity. When water touches the two open probes, it bridges the 3.3V to Pin 5 (becomes HIGH), triggering the **"UNDER WATER"** alert.
* **Danger Logic:** A simple push-button manual override for immediate help. Pressing the button sends 3.3V to Pin 4, triggering **"BABY IN DANGER!"**
* **Fixed IP:** Access the dashboard at **192.168.0.9** by connecting to the **CHILD SAFETY** WiFi.

---

### 4. Project Output Details
* **WiFi Name:** `CHILD SAFETY`
* **Password:** `234555444`
* **Access URL:** `http://192.168.0.9`
