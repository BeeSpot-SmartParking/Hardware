# IDE Setup for ESP32 – *BeeSpot Smart Parking System*

<img src="images/1.png" width="50%">

---

## Why ESP32 for BeeSpot?
BeeSpot relies on **IoT-enabled ESP32 devices** to detect cars, manage parking occupancy, and integrate with gates, cameras, and smart meters.  
The ESP32 is the backbone of our hardware setup, handling:

- **Ground Sensors** (magnetic/ultrasonic) → detect car presence.  
- **Overhead Cameras with AI modules** → license plate recognition & spot monitoring.  
- **Gate/Barrier Controllers** → verify entry/exit for reservations.  
- **Smart Meters** → link parking usage with digital payments.  

To program and deploy ESP32 firmware, we use the **Arduino IDE**.  
This guide shows you how to set it up for BeeSpot development.

---

## Installing the ESP32 Board in Arduino IDE (Windows, macOS, Linux)

Arduino IDE supports ESP32 boards through an **add-on**.  
This enables BeeSpot developers to easily flash and test parking-related firmware.

⚠️ If you face issues, check the [ESP32 Troubleshooting Guide](https://randomnerdtutorials.com/esp32-troubleshooting-guide/).

---

### Step 1: Install Arduino IDE

Download and install Arduino IDE:  
👉 [https://www.arduino.cc/en/software](https://www.arduino.cc/en/software)

- Choose IDE **1.x** or **2.x** depending on your OS.  
- (We recommend **IDE 2.x** for BeeSpot for better support and debugging).  

![IDE Download Page](images/Arduino IDE Download Page.png "IDE Download Page")

---

### Step 2: Install ESP32 Board on Arduino IDE

1. Open **File > Preferences**.  
2. In **Additional Board Manager URLs**, paste this:

https://raw.githubusercontent.com/espressif/arduino-esp32/gh-pages/package_esp32_index.json

yaml
Copy code

3. Hit **OK**.  
4. Then open **Tools > Board > Boards Manager…**.  
5. Search for **ESP32 by Espressif Systems** and install it.  

![Board Installation](images/BoardINstallation.png "Boards Manager menu")

---

### Step 3: Test the Installation (BeeSpot Example)

Before connecting BeeSpot modules, let’s check that the ESP32 works properly.

1. Plug the ESP32 board into your PC.  
2. In Arduino IDE, select the board under **Tools > Board** (e.g., "ESP32 DevKit v1").  
3. Select the correct **Port**.  
4. Open the example: **File > Examples > WiFi (ESP32) > WiFiScan**.  
5. Press **Upload**.  

If everything works, you’ll see nearby WiFi networks in the **Serial Monitor (115200 baud)**.  

✅ This confirms that your ESP32 is ready for BeeSpot deployments.  

---

## Next Steps – Connecting BeeSpot IoT Modules

With the ESP32 set up, you can now integrate BeeSpot’s IoT devices:

- **Parking Spot Sensors** → Send live occupancy data to the BeeSpot server.  
- **Gate Control** → Open/close based on mobile reservations.  
- **ESP32-CAM Module** → Detect license plates & verify spot usage.  
- **Smart Meters (via WiFi)** → Enable seamless digital billing.  

Each module has its own ESP32 sketch, all flashable via Arduino IDE.

---

## Resources

- 👉 BeeSpot Hardware Repo: [https://github.com/BeeSpot-SmartParking/Hardware](https://github.com/BeeSpot-SmartParking/Hardware)  
- 👉 ESP32 Documentation: [https://docs.espressif.com/](https://docs.espressif.com/)  

---

📌 **This guide ensures every BeeSpot developer can prepare their ESP32 for building smart parking IoT modules.**
