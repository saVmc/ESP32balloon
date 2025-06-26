# ESP32balloon

Original prototype script for my 2025 T2 Weather Balloon project.  
Features camera usage, data monitoring, and logging.

## Features

- **Live Sensor Data Monitoring:**  
  View real-time data from temperature, humidity, air pressure, GPS, and air quality sensors via a web interface.
- **Camera:**  
  Take and download low or high-resolution photos, with GPS EXIF tags embedded.
- **CSV Logging:**  
  Download recent sensor readings as a CSV file.
- **GPS Tracking:**  
  Displays location, altitude, speed, course, satellite count, and signal strength.
- **Web Serial Monitor:**  
  Watch live serial output from the ESP32 right in your browser!
- **Self-Contained WiFi AP:**  
  ESP32 runs as a WiFi access point for easy field use.
- **Responsive Web UI:**  
  Use any browser on phone, tablet, or laptop.

## Hardware Used

- **ESP32-CAM** (AI-Thinker or compatible)
- **DHT11** for temperature & humidity
- **SPL06** for pressure/altitude
- **CCS811** for air quality (CO2 and TVOC)
- **GPS Module** (e.g. NEO-6M)
- (Optional) breadboard, jumper wires, 3.3V regulator, and external battery

## Getting Started

1. **Install Arduino IDE** and add the ESP32 board support.
2. **Install these libraries:**
   - [TinyGPSPlus](https://github.com/mikalhart/TinyGPSPlus)
   - [Adafruit_CCS811](https://github.com/adafruit/Adafruit_CCS811)
   - [DHT sensor library](https://github.com/adafruit/DHT-sensor-library)
   - [WebSockets by Markus Sattler](https://github.com/Links2004/arduinoWebSockets)
3. **Wiring:**  
   See comments in the `.ino` file for pinouts.
4. **Configuration:**  
   - Set your WiFi SSID and password in the `.ino` file (default: ESP32 is an AP named *WeatherBalloon*)
5. **Upload:**  
   Compile and upload the code to your ESP32-CAM.

## Web Interface

- **Connect to WiFi:**  
  Connect to the ESP32's WiFi AP (default AP = *WeatherBalloon*).
- **Visit the Webpage:**  
  Go to `http://192.168.4.1` in your browser.
- **Sections:**
  - **Home:** Live data and quick navigation.
  - **Camera:** Stream video, take photos (low/high quality).
  - **Serial Monitor:** Watch ESP32 serial output live.
  - **Download CSV:** Get recent sensor data as a CSV file.


## Credits

Written and designed by Farley Hammond (10CPTY).  
Special thanks to jorteh


