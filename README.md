# Saudi National Day 96 - ESP

This project celebrates the **96th Saudi National Day** 🇸🇦 by displaying a custom animation on a **128x64 SH1106 OLED display** using an **ESP8266**, a breadboard, and jumper wires.

[![ESP8266](https://shieldcn.dev/badge/ESP8266-ready-00979D.svg?logo=espressif)](https://shieldcn.dev/badge/ESP8266-ready-00979D.svg?logo=espressif)
[![ESP32](https://shieldcn.dev/badge/ESP32-compatible-E7352C.svg?logo=espressif)](https://shieldcn.dev/badge/ESP32-compatible-E7352C.svg?logo=espressif)
[![SH1106 OLED](https://shieldcn.dev/badge/Display-SH1106_128x64-1E90FF.svg?logo=adafruit)](https://shieldcn.dev/badge/Display-SH1106_128x64-1E90FF.svg?logo=adafruit)
[![Arduino](https://shieldcn.dev/badge/Framework-Arduino-00979D.svg?logo=arduino)](https://shieldcn.dev/badge/Framework-Arduino-00979D.svg?logo=arduino)
[![License: MIT](https://shieldcn.dev/badge/License-MIT-green.svg?variant=outline)](https://shieldcn.dev/badge/License-MIT-green.svg?variant=outline)

![OLED Animation Demo](https://github.com/user-attachments/assets/5d8f30a8-5071-4deb-a198-34b693ae372c)

---

# Hardware Used
- **ESP8266 or ESP32**
- **SH1106 OLED Display (128x64, I²C)**
- **Breadboard**
- **Jumper Wires**

---

# Wiring

### OLED (I²C)

| OLED Pin | ESP8266 Pin |
|----------|-------------|
| VCC      | 3.3V        |
| GND      | GND         |
| SDA      | D2 (GPIO4)  |
| SCL      | D1 (GPIO5)  |

⚠️ The ESP8266 is **3.3V only** → connect OLED VCC to **3.3V**, not 5V.

⚠️ This code targets the **SH1106** controller (not SSD1306). Make sure your OLED module uses SH1106 → check the back of the board for the driver chip marking.

---

# Image Conversion

The bitmaps in this project were generated using the **image2cpp** tool:

🔗 https://javl.github.io/image2cpp/

**Recommended settings used:**
- Canvas size: **128 x 64**
- Scaling: **Scale to fit**
- Background color: **Black**
- Draw mode: **Horizontal** (1 bit per pixel)

---

# Screen Cycle

| Screen              | Duration |
|---------------------|----------|
| Flag + username     | 5 s      |
| National Day 96     | 10 s     |
| MBS Logo            | 5 s      |

---

# Libraries
- **Adafruit GFX**
- **Adafruit SH110X**

Install them via the Arduino Library Manager.

---

# Customizing
- **Username**: edit `USERNAME` near the top of the sketch.
- **Screen durations**: edit `PROFILE_TIME`, `NATIONAL_TIME`, `LOGO_TIME`.

---

# License
MIT
