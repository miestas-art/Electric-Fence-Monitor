# Electric-Fence-Monitor
An open-source electric fence monitoring system. Built with an ESP32, this device measures fence voltage, temperature, rainfall, and UV light, then sends the data wirelessly (WiFi) to Home Assistant.

This project intends to provide a complete solution for monitoring an electric fence of up to 10J, 15kV. 

Key Features:
  Real-time Monitoring: Safely measures and tracks fence voltage, allows identification alerting of fence failures.
  Environmental Sensing: Gathers critical environmental data, including air/soil temperature, rainfall, and UV levels.
  Long-Range Connectivity: Transmits data up to 150m using directional Wi-Fi antennas, seamlessly integrating with a Home Assistant system for data visualization and logging.
  Open-Source & Extensible: The entire project, from the circuit design to the ESPHome code, is available under the permissive MIT License, encouraging others to build upon and improve the design.

How It Works:
  The ESP32 collects data from various sensors and transmits it to your Home Assistant dashboard.
  High-Voltage Sensor: A resistor divider network safely steps down the fence voltage for the ESP32's ADC pin. A 3.3V TVS diode provides essential protection against voltage spikes.
  Temperature: Three DS18B20 waterproof sensors are connected using the 1-Wire protocol, which allows multiple sensors to share a single pin.
  Analog Sensors: A resistive rain sensor and a UV sensor module connect to dedicated ADC pins on the ESP32.
  Data Transmission: The ESP32-WROOM-32U uses its integrated Wi-Fi with external antennas to send sensor data via ESPHome to Home Assistant dashboard.
