Here's the updated **README.md** with the **SCR part removed** and focusing **only on the Power MOSFET-based PWM Floodlight Intensity Controller**:

---

# 🌟 Floodlight Intensity Controller (PWM + MOSFET Based)

A microcontroller-based floodlight intensity controller using **PWM** and **Power MOSFETs** for precise and efficient brightness control. This system enables real-time dimming of DC floodlights using analog input from a potentiometer.

---

## 📌 Features

* ✅ Smooth brightness control via PWM
* ✅ Real-time analog input using potentiometer
* ✅ Microcontroller-controlled PWM output
* ✅ Efficient power delivery using MOSFETs
* ✅ Optional LCD display for brightness level

---

## ⚙️ Technologies Used

* **Microcontroller:** STM32F446RE / Arduino Uno
* **MOSFET:** IRF540N (or any logic-level N-channel power MOSFET)
* **PWM Control:** Timer-based PWM generation
* **Analog Input:** ADC-based potentiometer interface

---

## 🔌 Working Principle

1. A **potentiometer** is connected to the microcontroller's **ADC pin**.
2. The microcontroller reads the analog value and maps it to a **PWM duty cycle** (0–100%).
3. A **PWM signal** is generated on a digital output pin connected to the **gate of a Power MOSFET**.
4. The **MOSFET** switches the DC supply to the **floodlight**, controlling its brightness based on the duty cycle.

---

## 🧰 Hardware Requirements

* STM32F446RE / Arduino Uno (or similar MCU)
* IRF540N / IRFZ44N MOSFET
* DC Floodlight (12V/24V)
* Potentiometer (10k)
* 16x2 LCD (optional, for brightness level)
* External Power Supply (12V/24V)
* Flyback diode (e.g., 1N5822) for inductive protection (optional)
* Resistors, jumper wires, breadboard or PCB

---

## 📋 Setup Instructions

1. **Connect the potentiometer** to the ADC input of the microcontroller.
2. **Configure PWM output** pin using a hardware timer.
3. **Connect the MOSFET** as a low-side switch to control floodlight power.
4. Optionally connect **LCD** to display brightness level in %.
5. Upload the firmware and power the circuit with a proper DC supply.

---

## 🧪 Testing & Results

* The floodlight's brightness changes smoothly from dim to full brightness.
* System tested up to **5A current draw** without MOSFET overheating.
* No visible flickering at PWM frequencies above 5kHz.
* LCD shows brightness percentage (if used).

---

## 🛡️ Safety Note

> Ensure proper **heat dissipation** using a heat sink on the MOSFET.
> Always verify power ratings of components to avoid damage.
> Use flyback diodes if the floodlight has inductive properties.

---

## 📚 Future Improvements

* Add remote dimming control via **Bluetooth / Wi-Fi**
* Automatic brightness adjustment based on ambient light (using **LDR**)
* Mobile app interface for control
* Overcurrent protection and thermal cutoff

---

## 📸 Demo

![Floodlight Dimming Demo](LINK: https://drive.google.com/file/d/1Sj8K62FDzM4mcXJ_QYpKZxGtfk0Eaq9b/view?usp=sharing)

---

## 📄 License

This project is open-source under the **MIT License**.

---

## 🙋‍♂️ Author

**Suraj N.**
For collaboration or questions, feel free to reach out on [LinkedIn](#) or via email.

---
