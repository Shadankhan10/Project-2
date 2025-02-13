# Evil Twin Attack with ESP8266

## Introduction
This project is designed for **ESP8266-based Evil Twin & Deauther WiFi penetration testing**. It includes features like:
- **Display integration** (for real-time logs)
- **RSSI (Received Signal Strength Indication) support**
- **Improved captive portal functionality**
- **Fixes for ESP8266 Boards Manager to prevent errors during deauthentication**
- **Optimized performance to ensure a smooth attack execution**

The project name is inspired by *Zero Two* from *Darling in the Franxx*.

---

## ⚠️ Disclaimer
**This tool is strictly for educational and security testing purposes.**

- **Use only on networks you own or have explicit permission to test.**
- **The user is fully responsible for any consequences.**
- **Misuse of this tool may lead to legal consequences. Proceed with caution.**

I am **not responsible for any misuse** of this program.

---

## 🛠 How It Works
This tool utilizes a **deauthentication attack** to force devices off their WiFi network. Once disconnected, the tool creates a **cloned SSID (Evil Twin)**, tricking victims into connecting to it. This allows for **credential capture** and other testing techniques.

---

## 🔧 Prerequisites
### Required Hardware:
- **ESP8266 Development Board** (e.g., NodeMCU, Wemos D1 Mini, etc.)
- **Arduino IDE** (for compiling and uploading code)
- **0.96” I2C OLED Display** *(optional, for real-time monitoring)*
- **Jumper wires & breadboard** *(optional, for prototyping)*

---

## 📌 Installation Guide
1. **Add ESP8266 Board to Arduino IDE:**
   - Open **Arduino IDE**
   - Navigate to **File > Preferences > Additional Board Manager URLs**
   - Paste this URL:
     ```
     https://raw.githubusercontent.com/SpacehuhnTech/arduino/main/package_spacehuhn_index.json
     ```
   - Alternatively, refer to the **Spacehuhn Deauther ESP8266 installation wiki**.
2. **Install ESP8266 Deauther Board:**
   - Go to **Tools > Board > Boards Manager**
   - Search for **"deauther"** and install **Deauther ESP8266 Boards**.
3. **Select the Correct Board:**
   - Navigate to **Tools > Board > Deauther ESP8266 Boards**.
   - Select the appropriate board (e.g., NodeMCU if using NodeMCU).
4. **Download & Open the Project Code:**
   - Download the project files and open `evil_twin.ino` in **Arduino IDE**.
5. **Install Required Libraries:**
   - Go to **Tools > Manage Libraries**.
   - Search for `Adafruit SSD1306` and install **Adafruit SSD1306 by Adafruit**.
6. **Upload Code to ESP8266:**
   - Select the correct **COM port**.
   - Click **Upload** to compile and flash the firmware to your ESP8266.
7. **Done!** Your device is ready to use.

---

## 📡 Usage Guide
### Wiring (if using an OLED Display):
| OLED Pin | ESP8266 Pin |
|----------|------------|
| VCC      | 3.3V       |
| GND      | GND        |
| SCL      | D1         |
| SDA      | D2         |

### Steps to Use:
1. **Connect to the Evil Twin WiFi Network:**
   - Find and connect to the SSID **"Eveil"** (default password: `123456`).
   - You can customize this in the code.
2. **Access the Attack Panel:**
   - The captive portal should open automatically.
   - If not, open a browser and go to `192.168.4.1`.
3. **Select Target Network:**
   - Choose the target SSID from the list.
4. **Launch the Attack:**
   - Click **"Start Deauth"** to disconnect clients from the target WiFi.
   - Click **"Start Evil Twin"** to create a fake SSID.
5. **Monitor Activity:**
   - The OLED display (if connected) will show logs and captured credentials.
   - If a victim enters a password in the captive portal, the **cloned SSID disappears**, and deauth stops.
   - The results can be viewed in the attack panel under **Zero Twin v1.0**.

---

## ⚙️ Customization
The source code includes variables for:
- **Changing the default SSID & password**
- **Customizing the captive portal**
- **Adjusting attack behavior**

You can modify these settings to match your testing environment.

---

## 🚨 Warning
🚫 **DO NOT test this on unauthorized networks.**
❌ **Avoid using it on family, friends, or strangers.**
⚖️ **Use this tool responsibly to avoid legal trouble.**

---

### 🔗 Useful Links
- **Official ESP8266 Deauther Project:** [Spacehuhn GitHub](https://github.com/SpacehuhnTech/Deauth)
- **Additional Resources & Tutorials:** [ESP8266 Forum](https://www.esp8266.com/)

---

## 🔥 Final Thoughts
This tool provides an **effective way to test WiFi security** and **educate cybersecurity learners** about Evil Twin Attacks. It is designed to be **easy for beginners** while still offering **advanced customization** for professional users.

💡 **Always use this tool ethically and within legal boundaries!**


