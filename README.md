# water-level-indicator
# Automated Water Level Indicator & Monitoring System

An embedded C++ firmware solution designed to monitor liquid levels in real-time, trigger threshold-based visual/audio indicators, and prevent tank overflow or dry-run conditions.

---

## Live Interactive Simulation

Test and interact with the firmware live in your browser without physical hardware:  
👉 **[Run on Wokwi Simulator](https://wokwi.com/projects/475519206531255297)**

---

## Features

- **Multi-Level Threshold Detection:** Monitors discrete liquid thresholds (Low, Medium, High / Overflow).
- **Automated Alerts:** Triggers visual LED indicators and audio alerts when critical thresholds are reached.
- **Debounced Signal Processing:** Filters out surface ripples and false triggers for stable readouts.
- **Modular Embedded C++:** Clean structure separating input pin monitoring, state logic, and output control.

---

## Hardware / Pin Mapping

| Component | Pin Type | Arduino Pin | Description |
| :--- | :--- | :--- | :--- |
| Low Level Sensor / Contact | Digital / Analog In | `A0` / `D2` | Triggers low-level alert |
| Mid Level Sensor / Contact | Digital / Analog In | `A1` / `D3` | Normal operational range |
| High / Full Level Sensor | Digital / Analog In | `A2` / `D4` | Overfill alert trigger |
| Status LEDs (Green/Yellow/Red) | Digital Out | `D8`, `D9`, `D10` | Visual level indicators |
| Alarm Buzzer | Digital / PWM Out | `D11` | Acoustic warning on overflow/empty |

---

## How It Works

1. **Sampling:** Reads real-time logic levels or voltages from the water level sensor inputs.
2. **State Evaluation:** Compares the measured level against calibrated thresholds.
3. **Indicator Output:** Updates the corresponding LED indicators and sounds alerts if thresholds are breached.

---

## Repository Structure

- `src/` (or root): Embedded C++ source code (`main.cpp` or `sketch.ino`).
- `README.md`: Project documentation and direct interactive simulation link.
-
