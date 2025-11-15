# My Automatic Watering System

An Arduino-based **automatic plant watering system** that monitors soil moisture, controls a water pump, displays sensor data, and checks water-tank levels using an ultrasonic sensor.

---

## 🌱 Overview

This project automates the watering of plants using multiple sensors and a relay-controlled pump. The **Arduino Uno** reads soil moisture data and decides when to enable the pump. Additional components such as an **ultrasonic sensor**, **LED indicators**, and a **16x2 LCD display** enhance feedback and reliability.

### 🔧 System Behavior

* 💧 **Soil moisture sensor** checks if the soil is dry.
* 🚰 When dry → **Pump turns ON for 5 seconds**.
* 🌿 After watering → Pump turns OFF until dryness is detected again.
* 📏 **Ultrasonic sensor** monitors the water tank level.
* 🔵 If the tank is empty → **Blue LED turns ON** (warning).
* 🔴 When pump is running → **Red LED turns ON**.
* 📟 LCD displays sensor values and system states.

---

## 📦 Requirements

Hardware used:

* Arduino UNO board
* 1–2 Soil Moisture Sensors
* 16x2 LCD Display (Character OLED/HD44780 compatible)
* Red LED
* Blue LED
* Ultrasonic Sensor (HC-SR04)
* Breadboard
* 330Ω resistors (for LEDs)
* Relay module (to drive water pump)
* Water pump (DC)
* BMP280 Pressure/Temperature Sensor
* 12V & 5V power adapters

---

## 🔌 Wiring & Connections

### 🔁 Relay & Pump

* Relay **Vcc → 5V**
* Relay **GND → Breadboard GND**
* Relay **IN → Arduino Pin 8**
* Pump **Red wire (+) → Relay COM pin**
* Pump **Black wire (-) → Adapter (−)**
* Adapter **(+) → Relay NO pin** (Normally Open)

### 📡 Ultrasonic Sensor (HC-SR04)

* Vcc → 5V
* GND → GND
* Trig → **Pin 9**
* Echo → **Pin 13**

### 🌱 Soil Moisture Sensor

* Vcc → 5V
* GND → GND
* A0 → **Arduino A0**

### 🌡 BMP280 Pressure Sensor

* Vcc → 5V
* GND → GND
* SCL → **A5**
* SDA → **A4**

### 💡 LEDs

**Red LED (Pump active indicator)**

* LED + → 330Ω resistor → **Pin 7**
* LED − → GND

**Blue LED (Water tank empty warning)**

* LED + → 330Ω resistor → **Pin 10**
* LED − → GND

---

## 📟 LCD 16x2 Display

Connection mapping:

```
D4 → Pin 5
D5 → Pin 4
D6 → Pin 3
D7 → Pin 2
E  → Pin 11
RS → Pin 12
A  → 5V
K  → GND
VDD → 5V
VSS → GND
V0 → Pin 6 (contrast)
RW → GND
```

---

## 🧩 Circuit

Include your circuit diagram or wiring schematic here.
(You can upload an image named `circuit.png` in your repository.)

---

## 📝 Summary

This is a complete automated watering system that:

* Monitors environmental data
* Automatically waters plants
* Alerts user about tank water level
* Displays real-time information

Perfect for home automation, IoT learning, and Arduino beginners.

---

## 🤝 Contributing

Feel free to fork, improve wiring diagrams, or enhance the firmware.

---

## 📄 License

MIT License.
