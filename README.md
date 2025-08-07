# Motion-Activated Lock & Alarm System

## 📘 Description

For my final project at CodeWorks, I created a **motion-activated lock and alarm** system. This project uses a touch sensor to arm the system, and an ultrasonic sensor to detect nearby motion.

Once armed, if an object comes within **20 inches**, the alarm is triggered:
- A buzzer sounds  
- A servo motor locks the door  
- The system stays locked until the object is no longer detected

System modes are visually indicated using two LEDs:
- 🔴 **Unarmed**: Red LED is solid  
- 🟡 **Armed**: Red and Green LEDs blink  
- ⚫ **Triggered**: Both LEDs turn off

## 🔧 Components

- 1x HW-130 Motor Control Shield  
- 1x Servo Motor (connected to SER1)  
- 1x Ultrasonic Sensor (HC-SR04)  
- 2x LEDs (Red + Green)  
- 1x Piezo Buzzer  
- 1x Touch Sensor *(or button as an alternative)*  
- 2x 1KΩ Resistors  

## 🛠️ How to Build It

1. **Mount the HW-130 motor shield** on your Arduino Uno.

2. **Connect the components:**

   - **Servo Motor** → Plug into `SER1` pin header on the shield
   - **Ultrasonic Sensor**  
     - `Trig` → A0  
     - `Echo` → A1  
   - **Red LED** (with 1KΩ resistor) → A2  
   - **Green LED** (with 1KΩ resistor) → A3  
   - **Piezo Buzzer** → A4  
   - **Touch Sensor** (or button) → A5  
     - If using a button, wire one leg to A5 and the other to GND (use internal pullup in code)

3. **Upload the Arduino code** to your Uno. Make sure the correct board and port are selected in the Arduino IDE.

4. **Power the system**, press the touch sensor or button to arm it, and test it by moving something close to the ultrasonic sensor.

---

Let me know if you want a wiring diagram added or if you'd like the code embedded too!
