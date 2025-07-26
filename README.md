# FloodlightDimmer
Repository for Mini Project: Power Mosfet Based Floodlight Intensity dimmer
🌟 Floodlight Intensity Controller
A hardware-based floodlight intensity controller that allows precise control of light output using a microcontroller. 

Approach: MOSFET-Based PWM Control

📌 Features
  ✅ Adjustable floodlight brightness
  
  ✅ Microcontroller-based control logic
  
  ✅ Dual implementation: SCR and MOSFET methods
  
  ✅ Real-time analog control via potentiometer

  ✅ Safe and efficient circuit design

⚙️ Technologies Used
  Approach	Components Used
  SCR-Based	BT136/BT139 SCR, Zero-Crossing Detector, Opto-Isolator (MOC3021), Microcontroller
  MOSFET-Based	IRF540N MOSFET, STM32F446RE (or Arduino), PWM via Timer, ADC + Potentiometer

🔌 Working Principle
1. SCR-Based Triggering
  Uses phase-angle control to adjust the point in the AC cycle at which the SCR is triggered.
  
  Microcontroller detects zero crossing and delays SCR triggering using a timer to control brightness.

2. MOSFET-Based PWM
  Suitable for DC floodlights.
  
  Uses PWM signal to regulate duty cycle of the power delivered to the floodlight.
  
  Potentiometer input is read via ADC and mapped to PWM output.

🧰 Hardware Requirements
  STM32F446RE / Arduino Uno / Other Microcontroller
  
  IRF540N MOSFET / BT136 SCR
  
  Zero-Crossing Detector Circuit
  
  Opto-Isolator (MOC3021)
  
  16x2 LCD (Optional for display)
  
  Potentiometer (10k)
  
  Floodlight (AC or DC depending on method)
  
  External Power Supply (12V/24V DC or 230V AC)
  
  Resistors, Capacitors, Breadboard/PCB, etc.

📋 Setup Instructions
  Connect Potentiometer to microcontroller ADC input.
  
  Configure PWM output pin (for MOSFET) or triggering pin (for SCR).
  
  Use Timer Interrupt to vary duty cycle or delay from zero crossing.
  
  Display current intensity on LCD (optional).
  
  Power the circuit with the appropriate power source.

🧪 Testing & Results
  Tested with both AC and DC floodlights.
  
  Smooth dimming from 0% to 100% brightness.
  
  No flickering in MOSFET-based PWM approach.
  
  SCR-based design tested with isolation to ensure safety.

🛡️ Safety Note
  Always take proper precautions when working with AC mains voltage. Use opto-isolators and isolated power supplies. Double-check circuit insulation and grounding before testing.

📚 Future Improvements
  Add wireless control (Bluetooth or Wi-Fi)
  
  Schedule-based or sensor-driven dimming (LDR, motion sensors)
  
  Mobile app interface for brightness control
  
  Closed-loop feedback using light sensor (LDR)

📄 License
This project is open-source under the MIT License.

🙋‍♂️ Author
Suraj N.
For queries or collaboration, feel free to connect via LinkedIn or email.
