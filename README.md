# 🔧 Predictive Maintenance of Industrial Motor using ESP32

## 📌 Project Overview
This project implements a **Predictive Maintenance System** for industrial motors using **ESP32**, vibration, and temperature sensors.  
The system continuously monitors motor health and provides early alerts to prevent unexpected motor failures.

By analyzing **vibration data** from MPU6050 and **temperature data** from DHT22, the system classifies motor condition into:
- ✅ Healthy
- ⚠ Maintenance Required
- ❌ Failure Soon

Alerts are provided using an **LCD display**, **LED**, and **buzzer**.

---

## 🎯 Objectives
- Monitor vibration using MPU6050 accelerometer
- Measure temperature using DHT22 sensor
- Analyze data in real time using ESP32
- Display motor health status on I2C LCD
- Provide alerts using LED and buzzer
- Simulate the system using Wokwi

---

## 🛠️ Tech Stack

### Hardware
- ESP32
- MPU6050 (Accelerometer & Gyroscope)
- DHT22 (Temperature Sensor)
- 16×2 I2C LCD
- LED
- Active Buzzer

### Software
- Arduino IDE
- Wokwi Simulator
- Libraries:
  - Wire.h
  - LiquidCrystal_I2C.h
  - Adafruit_MPU6050.h
  - Adafruit_Sensor.h
  - DHT.h

---

## 📊 System Architecture
MPU6050 (Vibration) ─┐
├── ESP32 ── LCD Display
DHT22 (Temperature) ─┘ ├── LED Alert
└── Buzzer Alert



---

## 🔌 Pin Configuration

| Component | ESP32 Pin |
|---------|-----------|
| LED (+) | GPIO 2 (via 220Ω resistor) |
| Buzzer (+) | GPIO 4 |
| DHT22 DATA | GPIO 15 |
| MPU6050 SDA | GPIO 21 |
| MPU6050 SCL | GPIO 22 |
| LCD SDA | GPIO 21 |
| LCD SCL | GPIO 22 |
| GND | Common Ground |

---

## ⚙️ Working Principle
1. ESP32 reads vibration data from MPU6050.
2. ESP32 reads temperature data from DHT22.
3. Sensor values are compared with predefined thresholds.
4. Motor condition is determined as Healthy, Maintenance Required, or Failure Soon.
5. Alerts are generated using LED, buzzer, and LCD.

---

## 🧠 Decision Logic

| Condition | Motor Status |
|--------|--------------|
| Normal vibration & temperature | Healthy |
| Medium vibration or high temperature | Maintenance Required |
| High vibration and high temperature | Failure Soon |

---

## ▶️ How to Run (Wokwi)
1. Open Wokwi ESP32 Simulator
2. Add ESP32, MPU6050, DHT22, I2C LCD, LED, and buzzer
3. Upload the Arduino code from `code/` folder
4. Start simulation
5. Change sensor values to observe alerts

---

## 📷 Output
- LCD displays motor status
- LED indicates warning condition
- Buzzer alerts during failure condition
- Serial Monitor shows sensor readings

---

## 📈 Applications
- Industrial motor monitoring
- Predictive maintenance systems
- Smart factories
- Power plants
- HVAC systems

---

## 🚀 Future Scope
- Integration with TinyML / Edge Impulse
- Cloud-based monitoring dashboard
- Mobile app notifications
- Additional sensors (current, RPM)

---

## 📌 Conclusion
This project demonstrates a low-cost and efficient predictive maintenance solution using ESP32. By monitoring vibration and temperature, early alerts can be generated to reduce downtime and maintenance cost.

---

## 👩‍💻 Author
**Vasundhara Singh**  
B.Tech – Electronics & Communication Engineering
