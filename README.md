![Electric Feather Icon](./assets/Icon.png)
# Electric-Fence-Monitor
An open-source electric fence monitoring system for ~50eur. 
Built with an ESP32, this device measures fence voltage (10J, 15kV), temperature, rainfall, and UV light, then sends the data wirelessly (WiFi) to Home Assistant.

## Key Features:
* Real-time Monitoring: Safely measures and tracks fence voltage, allows identification alerting of fence failures.
* Environmental Sensing: Gathers critical environmental data, including air/soil temperature, rainfall, and UV levels.
* Long-Range Connectivity: Transmits data up to 150m using directional Wi-Fi antennas, seamlessly integrating with a Home Assistant system for data visualization and logging.
* Open-Source & Extensible: The entire project, from the circuit design to the ESPHome code, is available under the permissive MIT License, encouraging others to build upon and improve the design.

## How It Works:
* The ESP32 collects data from various sensors and transmits it to Home Assistant dashboard.
* High-Voltage Sensor: A resistor divider network safely steps down the fence voltage for the ESP32's ADC pin. A 3.3V TVS diode provides essential protection against voltage spikes.
* Temperature: Three DS18B20 waterproof sensors are connected using the 1-Wire protocol, which allows multiple sensors to share a single pin.
* Analog Sensors: A resistive rain sensor and a UV sensor module connect to dedicated ADC pins on the ESP32.
* Data Transmission: The ESP32-WROOM-32U uses its integrated Wi-Fi with external antennas to send sensor data via ESPHome to Home Assistant dashboard.

## Component List
A list of the components used in this project

* **Microcontroller:** ESP32-WROOM-32U Development Board with external 2.4G antenna
* **High-Voltage Sensor:** 100MΩ high-voltage resistor (RI82-50X10-100MJ), 20kΩ metal film resistor
* **Circuit Protection:** SMAJ3.3A TVS diode
* **Capacitors:** 1µF capacitor
* **Temperature Sensors:** DS18B20 Waterproof Temperature Sensor Module (x3) with Plugable 3-pin terminal
* **Rain Sensor:** Digital Rain Snow Sensor Module w/Humidity Detection
* **UV Sensor:** GUVA-S12SD UV Detection Sensor Module
* **Soil Moisture:** Capacitive Soil Moisture Sensor Module
* **Ambient Light:** SAMIROB Ambient Light Sensor Module VEML7700 (I²C)
* **Connectivity and assembly:** High Voltage Cooper Wire 20KV-18AWG, 5V 1A USB A wall charger, USB A to A Cable,  Nylon PCB Standoff Spacers M3 (Thread 6mm), Single Side PCB Prototyping Boards 5*7cm, plastic box, 400-Point Breadboard for prototyping, Breadboard Jumper Wire Kit
