# Water Quality Monitoring With ESP32

## Abstract  
Water quality monitoring is essential for safeguarding public health, environmental protection, and efficient water resource management. This project employs the ESP32 (NodeMCU) microcontroller to design a cost-effective, real-time water quality monitoring system that can measure parameters such as pH, temperature, turbidity, and dissolved oxygen levels. The system integrates various sensors with the ESP32 to collect data and utilizes IoT capabilities to transmit this information to a cloud platform for remote monitoring and analysis. By leveraging this technology, users can receive timely alerts on water quality status, helping to prevent potential hazards and ensure water safety compliance.

---

## Project Structure  
```
Water-Quality-Monitoring-ESP32/
│-- Arduino_Code/
│   ├── water_quality.ino
│-- libraries/
│   ├── OneWire/
│   ├── DallasTemperature/
│   ├── Adafruit_ADS1X15/
│   ├── DFRobot_ESP_EC/
│   ├── Adafruit_GFX/
│   ├── Adafruit_SSD1306/
│-- images/
│-- README.md
```

---

## Installation & Setup  
### 1. Download the Required Files  
- Clone this repository or download the provided Arduino `.ino` file from the `Arduino_Code/` folder.
- Download the required libraries listed below and add them to your Arduino `libraries` folder.

### 2. Required Libraries  
Download and install the following libraries before uploading the code:

1. **OneWire Library**: [Download](https://github.com/PaulStoffregen/OneWire)
2. **Dallas Temperature Library**: [Download](https://github.com/milesburton/Arduino-Temperature-Control-Library)
3. **ADS1015 Library**: [Download](https://github.com/adafruit/Adafruit_ADS1X15) (Install version 1.4)
4. **DFRobot ESP EC Library**: [Download](https://github.com/GreenPonik/DFRobot_ESP_EC_BY_GREENPONIK)
5. **Adafruit GFX Library**: [Download](https://github.com/adafruit/Adafruit-GFX-Library)
6. **Adafruit SSD1306 Library**: [Download](https://github.com/adafruit/Adafruit_SSD1306)

### 3. Hardware Components  
- ESP32 NodeMCU WiFi Module
- TDS/EC Sensor
- DS18B20 Waterproof Temperature Sensor
- 0.96″ I2C OLED Display
- Connecting Wires
- Power Source

### 4. Connecting the Hardware  
| Sensor/Component | ESP32 Pin |
|-----------------|----------|
| DS18B20 Sensor | GPIO 4   |
| TDS/EC Sensor  | GPIO 36  |
| OLED Display   | GPIO 21 (SDA), GPIO 22 (SCL) |

### 5. Upload the Code  
- Open the Arduino IDE.
- Install the ESP32 board support in Arduino IDE.
- Select the correct board and COM port.
- Upload the `water_quality.ino` sketch.

---

## Project Description  
This project aims to develop an **IoT-Based Drinking Water Quality Monitoring System** using an ESP32 WiFi Module, TDS/EC Sensor, and Temperature Sensor. The system monitors:

- **Water Electrical Conductivity (EC):** Should not exceed 400 μS/cm (0.4 mS/cm) as per WHO standards.
- **Water Temperature:** Ideal for drinking water is **room temperature (20°C / 68°F)** for maximum flavor or **chilled cold (6°C / 43°F)** for maximum refreshment.

The EC & temperature values will be displayed on a **0.96" I2C OLED Display** and monitored online using the **ThingSpeak IoT platform** from anywhere in the world.

---

## Features  
 Real-time monitoring of water quality parameters  
 IoT-based remote monitoring via ThingSpeak  
 OLED display for local visualization  
 Alerts for exceeding water quality thresholds  
 Low-cost and energy-efficient solution  

---

## License  
This project is open-source and available under the **MIT License**.

