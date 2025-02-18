# Zipher Hertz System for 2.4GHz Testing and Jamming
The Zipher Hertz system, using an ESP32 and RF24 module, is designed for 2.4GHz signal testing, debugging, and controlled jamming. It can disrupt wireless communication for testing or close unwanted connections—ideal for those annoyed by noisy Bluetooth speakers. Intended for experimental and educational use only.

- Install Hertz : https://ziphercyprex.github.io/ZipherHertz-Jammer/
---

#### **⚠️ Legal Disclaimer**

#### Using an **ESP32 + NRF24 jammer** to interfere with wireless communications may be **illegal** in many countries. Unauthorized jamming can violate radio regulations, disrupt essential services, and result in severe penalties. Ensure you have proper authorization before conducting any tests.

---

### **✅ Guidelines**

#### **1. Supported Hardware**

- **ESP32** as the main controller.
- **NRF24L01 (3.7V)** or **E01-2G4M27D (5V)** for stronger interference.

#### Support Module
- ESP32 (ESP32S ESP32D ESP32U) 30pin 38pin
- ESP8266 (D1-Mini-Pro and All-8266 )

#### **2. Flashing the Firmware**

- Use the web flasher at **[Hertz Jammer](https://ziphercyprex.github.io/ZipherHertz-Jammer/)** for quick and easy flashing.
- Ensure proper driver installation before flashing.

<img src="https://github.com/user-attachments/assets/0f9eea2f-e1a7-4700-9690-9507fa357013" width="650" height="auto">

---

#### **3. Power & Connections**

- Use a **stable power source** to prevent instability.
- If using **E01-2G4M27D (5V)**, ensure the ESP32 can handle the voltage 5v.

### ESP32-nRF24L01+ pinout + battery mod
Here are pinouts for HSPI and VSPI. You need nRF24L01 modules connected.                
[nRF24L01+ pinout](https://howtomechatronics.com/wp-content/uploads/2017/02/NRF24L01-Pinout-NRF24L01-PA-LNA--768x512.png?ezimgfmt=ng:webp/ngcb2)
- Only ESP32s Led Stetus will work.
[ESP32s pinout](https://lastminuteengineers.com/wp-content/uploads/iot/ESP32-Pinout.png)

### HSPI
| E01-2G4M27D | HSPI Pin (ESP32) | 10uf capacitor |
|---------------|------------------|--------------------|
| VCC           | 5V               | (+) Capacitor |
| GND           | GND              | (-) Capacitor |
| CE            | GPIO 16          |
| CSN           | GPIO 15          |
| SCK           | GPIO 14          |
| MOSI          | GPIO 13          |
| MISO          | GPIO 12          |
| IRQ           |                  |

### VSPI 
| E01-2G4M27D | VSPI Pin (ESP32) | 10uf capacitor |
|---------------|------------------|--------------------|
| VCC           | 5V               | (+) Capacitor |
| GND           | GND              | (-) Capacitor |
| CE            | GPIO 22          |
| CSN           | GPIO 21          |
| SCK           | GPIO 18          |
| MOSI          | GPIO 23          |
| MISO          | GPIO 19          |
| IRQ           |                  |

### Battery modification (additional)
| 3.7V Li-Ion battery | JST-PH2 connector    | TP4056 Charging Module | Slide Switch | StepUp 3.7v to 5v | ESP32 |
|---------------------|----------------------|------------------------|--------------|-------------------|-------|
| (+) Battery         | (+) JST-PH2          | Batt +                 |              |                   |       |
| (-) Battery         | (-) JST-PH2          | Batt -                 |              |                   |       |
|                     |                      | OUT +                  | Switch +     | VCC IN            |       |
|                     |                      | OUT -                  |              | GND               |  GND  |
|                     |                      |                        | Switch -     | VCC OUT           |  5V   |

---

#### **4. Testing & Debugging**

- Perform tests in **controlled environments** (e.g., a Faraday cage).
- Monitor signal interference using a **spectrum analyzer**.


<img src="https://github.com/user-attachments/assets/3a1c8fc2-ab7a-4554-8887-1f77052d8791" width="650" height="auto">


---
### Other Board Connection (Writing . .)
### HSPI
| E01-2G4M27D | HSPI Pin (ESP8266) | 10uf capacitor |
|---------------|------------------|--------------------|
| VCC           | 5V               | (+) Capacitor |
| GND           | GND              | (-) Capacitor |
| CE            | GPIO 16          |
| CSN           | GPIO 15          |
| SCK           | GPIO 14          |
| MOSI          | GPIO 13          |
| MISO          | GPIO 12          |
| IRQ           |                  |

### VSPI 
| E01-2G4M27D | VSPI Pin (ESP8266) | VSPI Pin (ESP32S2) | 10uf capacitor |
|---------------|------------------|--------------------|----------------|
| VCC           | 5V               | 5V                 | (+) Capacitor  |
| GND           | GND              |                    | (-) Capacitor  |
| CE            | GPIO 22          |                    |                |
| CSN           | GPIO 21          |                    |                |
| SCK           | GPIO 18          |                    |                |
| MOSI          | GPIO 23          |                    |                | 
| MISO          | GPIO 19          |                    |                |
| IRQ           |                  |                    |                |

---

### **⚠️ Warnings**

1. This software is intended for educational and research purposes only. The author bears no responsibility for any misuse of this software. Use it responsibly and in compliance with all applicable laws and regulations.

---

### **🔹 Final Note**

Always check **local laws** and ensure compliance with **regulatory bodies** (FCC, CE, etc.) before experimenting with wireless transmission. Use responsibly and **never disrupt** critical communications.
