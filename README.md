# Smart Load Monitoring System

An IoT-based load monitoring system built with an ESP32 microcontroller and an HX711 load cell amplifier. This system continuously measures material weight using strain gauge technology, displays real-time values on an LCD, and provides automated threshold alerts via a local web dashboard.

---

## Project Overview

Warehouses often face challenges with real-time inventory tracking, structural overloading, and production stoppages due to material depletion. This system solves those issues by offering automated continuous weight monitoring and instant alerts when weights cross safe operational thresholds.

---

## Key Features

* **Hardware Monitoring:** Continuous weight measurement (0–500g range) with high-precision sensing and real-time visualization on a 16x2 I2C LCD.
* **Threshold Alert System:** Automatically triggers visual warnings and browser pop-ups for **Weight Depletion (<200g)** and **Weight Overload (>500g)**.
* **Local Web Dashboard:** Serves an asynchronous web server on the ESP32, allowing remote access and real-time updates via local Wi-Fi without internet dependency.
* **Self-Calibration & Taring:** Includes automated tare routines to zero out the scale during initialization.

---

## Technical Stack & Components

### Hardware Components
* ESP32 Microcontroller
* HX711 Load Cell Amplifier
* 5kg Strain Gauge Load Cell
* 16x2 I2C LCD Display
* Breadboard and Jumper Wires

### Software & Libraries
* Arduino IDE
* `HX711` Library
* `LiquidCrystal_I2C` Library
* `WiFi` and `WebServer` Libraries

---

## System Architecture & Code Flow

1. **Initialization:** Hardware components initialize, the LCD shows a boot sequence, and the scale performs a tare operation.
2. **Network Connection:** The ESP32 connects to a local Wi-Fi network and starts an HTTP server on port 80.
3. **Continuous Monitoring:** The loop reads sensor weights every 100ms, evaluates thresholds, and updates the local LCD and web clients.

---

## Simulation & Demo

* **Wokwi Simulation:** [View Live Simulation](https://wokwi.com/projects/435813032575352833)
* **Demo Video:** [Watch Video Demo on Google Drive](https://drive.google.com/file/d/1Y7X_FPdb0d7yk4srHoZADahY-cGcOP1/view?usp=sharing)

---

## Author

* **Aviral Jha** (Reg. No.: 23BEC0387)
* **Institution:** Vellore Institute of Technology (VIT), Vellore
