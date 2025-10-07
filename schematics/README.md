# 🧭 K.A.R.L. Project — Schematics (EasyEDA PDF Exports)

This folder contains the **electrical schematics** for the **K.A.R.L. Project**, an autonomous rover powered by a **Raspberry Pi Pico**, **L298N motor driver**, and **MicroPython** control logic.
All diagrams were designed in **EasyEDA** and exported as **.pdf** files for quick viewing and documentation.

---

## 📘 Overview

Each schematic captures a core subsystem of the rover’s electronics — showing how the controller, sensors, and power circuits connect.
These PDFs are intended for quick reference during assembly, debugging, and documentation of the K.A.R.L. hardware design.

### Subsystems Included

* **Motor Control** — Wiring between the Pico and the L298N motor driver (supports two or four TT-style motors)
* **Ultrasonic Sensor (HC-SR04)** — Trigger and Echo wiring with a 5 V→3.3 V voltage divider
* **Power Distribution** — Battery connections, logic power, and ground reference layout
* **System Overview** — Combined schematic showing the full rover electrical topology

---

## ⚡ Voltage Divider Note (HC-SR04)

Because the **HC-SR04 Echo pin outputs 5 V** and the **Raspberry Pi Pico uses 3.3 V logic**, a **resistive voltage divider** is used to protect the input pin:

```
HC-SR04 Echo ----[10 kΩ]----+----→ Pico GPx
                             |
                           [15 kΩ]
                             |
                            GND
```

This reduces the Echo voltage to a safe ~3 V level for the Pico.

---

## 📁 File Naming Convention

| File Name                      | Description                         |
| ------------------------------ | ----------------------------------- |
| `motor_driver_L298N.pdf`       | Motor driver wiring diagram         |
| `ultrasonic_sensor_HCSR04.pdf` | HC-SR04 wiring and voltage divider  |
| `power_distribution.pdf`       | Battery and regulator wiring layout |
| `full_system_overview.pdf`     | Combined schematic for the rover    |

---

## 🧰 Design Notes

* Created entirely using **EasyEDA Online Editor**
* Exported as **PDFs** for initial documentation
* Preview images (`.png`) added for quick visualization
* Editable EasyEDA files will be included in a future update

---

## 🔧 Next Steps

* Annotate wire colors and pin labels for clarity
* Add PCB layout once breadboard validation is complete
* Include measured voltage/current data in future revisions

---

Would you like me to make a short caption or watermark suggestion for your `full_system_overview.png` (e.g. “K.A.R.L. v1.0 — EasyEDA Schematic” in the corner)? It makes the preview look polished on GitHub.
