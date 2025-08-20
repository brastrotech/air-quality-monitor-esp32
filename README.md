# air-quality-monitor-esp32
An IoT project using ESP32 with BME680, PMS5003, PMS7003, GPS, OLED Display, and SD Card. It measures temperature, humidity, pressure, gas, and air quality (PM1 / PM2.5 / PM10), logs data to an SD card, shows live readings on an OLED display, and uploads results to InfluxDB for cloud monitoring and dashboards.
# 🌍 ESP32 Air Quality Monitoring System

This project uses **ESP32** + **BME680** + **PMS5003** + **GPS (NEO-6M)** + **SSD1306 OLED** + **SD card** to collect and visualize environmental data.  
Data is logged locally (SD card), displayed on OLED, and sent to **InfluxDB** for cloud storage & dashboards.

---

## 🚀 Features
- 📡 GPS location tracking with TinyGPS++
- 🌡️ Temperature, Humidity, Pressure, Gas readings (BME680)
- 🏭 Air Quality Monitoring (PMS5003 for PM1 / PM2.5 / PM10)
- 💾 Local data logging to SD card
- 📶 WiFi connection with **WiFiManager** & portal config
- ☁️ Cloud upload to **InfluxDB**
- 🖥️ OLED display visualization

---

## 🛠️ Hardware Requirements
- ESP32 (ESP-WROOM-32)
- BME680 sensor
- PMS5003 air quality sensor
- SSD1306 OLED display (128x64 I²C)
- SD Card module (CS = GPIO5)
- NEO-6M GPS module

---

## 🔌 Wiring
| Component     | ESP32 Pin |
|---------------|-----------|
| BME680 (I2C)  | SDA=21, SCL=22 |
| SSD1306 OLED  | SDA=21, SCL=22 |
| PMS5003       | RX=16, TX=17   |
| GPS NEO-6M    | RX=27, TX=26   |
| SD Card CS    | GPIO5          |

---

## 📡 Setup
1. Install required libraries in Arduino IDE / PlatformIO:
   - `Adafruit BME680`
   - `Adafruit SSD1306`
   - `Adafruit GFX`
   - `TinyGPSPlus`
   - `PMS`
   - `WiFiManager`
   - `InfluxDB Client for Arduino`

2. Configure **InfluxDB** credentials in `include/config.h`:
