# ZHertz-Jammer
Zipher Hertz For Jamming 2.4ghz And -

- Install Hertz : https://ziphercyprex.github.io/ZHertz-Jammer/
---
### **ESP32 + NRF24 Jammer: Guidelines & Warnings**

#### **⚠️ Legal Disclaimer**

Using an **ESP32 + NRF24 jammer** to interfere with wireless communications may be **illegal** in many countries. Unauthorized jamming can violate radio regulations, disrupt essential services, and result in severe penalties. Ensure you have proper authorization before conducting any tests.
---

### **✅ Guidelines**

#### **1. Supported Hardware**

- **ESP32** as the main controller.
- **NRF24L01 (3.7V)** or **E01-2G4M27D (5V)** for stronger interference.

#### **2. Flashing the Firmware**

- Use the web flasher at **[ZHertz Jammer](https://ziphercyprex.github.io/ZHertz-Jammer/)** for quick and easy flashing.
- Ensure proper driver installation before flashing.

<img src="https://github.com/user-attachments/assets/0f9eea2f-e1a7-4700-9690-9507fa357013" width="650" height="auto">

---

#### **3. Power & Connections**

- Use a **stable power source** to prevent instability.
- If using **E01-2G4M27D (5V)**, ensure the ESP32 can handle the voltage difference.

### ESP32-nRF24L01+ pinout + battery mod
Here are pinouts for HSPI and VSPI. You need nRF24L01 modules connected.                
[nRF24L01+ pinout](https://howtomechatronics.com/wp-content/uploads/2017/02/NRF24L01-Pinout-NRF24L01-PA-LNA--768x512.png?ezimgfmt=ng:webp/ngcb2)
- Only ESP32s Led Stetus will work.
[ESP32s pinout](https://lastminuteengineers.com/wp-content/uploads/iot/ESP32-Pinout.png)

### HSPI
| nRF24L01 | HSPI Pin (ESP32) | 10uf capacitor |
|---------------|------------------|--------------------|
| VCC           | 3.3V             | (+) Capacitor |
| GND           | GND              | (-) Capacitor |
| CE            | GPIO 16          |
| CSN           | GPIO 15          |
| SCK           | GPIO 14          |
| MOSI          | GPIO 13          |
| MISO          | GPIO 12          |
| IRQ           |                  |

### VSPI 
| nRF24L01 | VSPI Pin (ESP32) | 10uf capacitor |
|---------------|------------------|--------------------|
| VCC           | 3.3V             | (+) Capacitor |
| GND           | GND              | (-) Capacitor |
| CE            | GPIO 22          |
| CSN           | GPIO 21          |
| SCK           | GPIO 18          |
| MOSI          | GPIO 23          |
| MISO          | GPIO 19          |
| IRQ           |                  |

### Battery modification (additional)
| 3.7V Li-Ion battery | JST-PH2 connector    | TP4056 Charging Module | Slide Switch | ESP32 |
|---------------------|----------------------|------------------------|-------------------|-------|
| (+) Battery         | (+) JST-PH2          | Batt +                  |                   |       |
| (-) Battery         | (-) JST-PH2          | Batt -                  |                   |       |
|                     |                      | OUT +                  | Switch +         |       |
|                     |                      | OUT -                  |                   |  GND  |
|                     |                      |                        | Switch -        |  3V3  |

===

#### **4. Testing & Debugging**

- Perform tests in **controlled environments** (e.g., a Faraday cage).
- Monitor signal interference using a **spectrum analyzer**.


<img src="https://github.com/user-attachments/assets/3a1c8fc2-ab7a-4554-8887-1f77052d8791" width="650" height="auto">


---

### **⚠️ Warnings**

1. **Illegal Use Risks**
    
    - Unauthorized jamming of public or private networks is **a criminal offense**.
    - May disrupt **Wi-Fi, IoT devices, drones, or industrial systems**.
2. **Detection & Tracking**
    
    - Authorities can **trace** jamming signals back to your location.
    - Many regions have **radio monitoring** systems to detect interference.
3. **Hardware Considerations**
    
    - NRF24L01 has **limited range**, while **E01-2G4M27D (5V)** provides stronger interference.
    - High-power modules generate more heat—use **cooling solutions if needed**.
4. **Ethical Responsibility**
    
    - Use for **educational & research** purposes only.
    - Avoid using jammers in **public areas** or against unauthorized targets.

---

### **🔹 Final Note**

Always check **local laws** and ensure compliance with **regulatory bodies** (FCC, CE, etc.) before experimenting with wireless transmission. Use responsibly and **never disrupt** critical communications.
