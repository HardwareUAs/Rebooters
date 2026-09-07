# 🔄 Rebooters Series

> Automated cyclic power reboot modules with scheduled reset and emergency shutdown capabilities.

---

## 📋 Active Revisions

| Board Model | Voltage | Max Current | Dimensions | Key Features & Architecture |
| :--- | :---: | :---: | :---: | :--- |
| [![LMR_Q](https://img.shields.io/badge/LMR__Q-6f42c1?style=for-the-badge&logo=circuitverse&logoColor=white)](./LMR_v2.6Q/) | <small>4–30 V</small> | <small>3.0 A</small> | <small>50.1 × 13.3 mm</small> | <small>AEC-Q100 automotive buck, 12.1V ECO Mode, dual 5V outputs (`L1`/`L2`), -65V reverse clamping (Non-inductive)</small> |
| [![NanoWDC](https://img.shields.io/badge/NanoWDC-6f42c1?style=for-the-badge&logo=circuitverse&logoColor=white)](./NanoWDC_v1.1/) | <small>5 V</small> | <small>3.5 A</small> | <small>17.0 × 7.9 mm</small> | <small>Host Watchdog (`wdtCONTROL` 30m timeout), `SOFTkill` shutdown, configurable 10h reboot (Non-inductive)</small> |
| [![5VIN_ADC](https://img.shields.io/badge/5VIN__ADC-6f42c1?style=for-the-badge&logo=circuitverse&logoColor=white)](./5VIN_ADC_v2.1/) | <small>3.3–5 V</small> | <small>3.0 A</small> | <small>17.6 × 8.1 mm</small> | <small>Power switch IC with active discharge (90 Ω), 3ms soft-start, OCP/SCP, event-driven `LED` control (Non-inductive)</small> |
| [![5VIN_ADC](https://img.shields.io/badge/5VIN__ADC-6f42c1?style=for-the-badge&logo=circuitverse&logoColor=white)](./5VIN_ADC_v2.0/) | <small>3.3–5 V</small> | <small>6.0 A</small> | <small>19.0 × 7.3 mm</small> | <small>Integrated 50A flyback Schottky diode for kickback clamping, 20ms soft-start, event-driven `LED` control (Inductive)</small> |
| [![5VIN_ADC](https://img.shields.io/badge/5VIN__ADC-6f42c1?style=for-the-badge&logo=circuitverse&logoColor=white)](./5VIN_ADC_v1.3/) | <small>5 V</small> | <small>3.5 A</small> | <small>16.9 × 8.1 mm</small> | <small>High-side power switch with 20ms soft-start, continuous GND plane, event-driven `LED` control (Non-inductive)</small> |
| [![5VIN_ADCQ](https://img.shields.io/badge/5VIN__ADCQ-6f42c1?style=for-the-badge&logo=circuitverse&logoColor=white)](./5VIN_ADC_v1.2Q/) | <small>3.3–5 V</small> | <small>3.0 A</small> | <small>11.2 × 6.9 mm</small> | <small>Ultra-compact power switch IC with 90 Ω active discharge, 3ms soft-start, full OCP/SCP, event-driven `LED` control (Non-inductive)</small> |
| [![5VIN_ADCQ](https://img.shields.io/badge/5VIN__ADCQ-6f42c1?style=for-the-badge&logo=circuitverse&logoColor=white)](./5VIN_ADC_v1.1Q/) | <small>3.3–5 V</small> | <small>6.0 A</small> | <small>9.0 × 7.7 mm</small> | <small>Sub-miniature footprint, 50A flyback diode for inductive kickback, 20ms soft-start, event-driven `LED` control (Inductive)</small> |

---

### 🛡️ Common Architectural Features

* **⏱️ Autonomous 10-Hour Cyclic Reboot**: Periodically power-cycles connected hardware every 10 hours to maintain long-term stability and eliminate software lockups.
* **🎛️ Event-Driven Monitoring (`LED` / `wdtCONTROL`)**: Hardware monitoring line with debounce filtering capable of reacting to external events, logic signals, or status indicators to isolate or power-cycle downstream devices.
* **🛡️ Inrush & Soft-Start Protection**: Integrated soft-start control (3 ms – 20 ms) eliminating supply voltage drops and transient surges.
* **🔀 Inductive vs Non-Inductive Specialization**: High-speed flyback Schottky diode clamping on inductive models (6.0 A) vs active discharge and ultra-compact switching on digital non-inductive models (3.0 A – 3.5 A).
