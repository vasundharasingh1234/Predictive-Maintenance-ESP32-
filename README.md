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
