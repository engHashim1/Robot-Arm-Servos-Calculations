# Robot-Arm-Servos-Calculations
Calculating Robot Arm Servos 

# Robot Arm Servo Torque Calculation

## 1. Problem Description
We need to calculate the required torque for each servo motor in a robotic arm to lift a **1 kg** load.  
The arm dimensions are:

- First segment: **15 cm**
- Second segment: **10 cm**
- Gripper length: **4 cm**

We will choose the appropriate servo motors for each joint and check if they can lift **2 kg** with the help of gears.

---

## 2. Torque Calculation Formula
The torque (T) is given by:

\[
T = F \times d
\]

Where:
- **T** = Torque (in kg·cm or N·cm)
- **F** = Force applied (in kg or N)
- **d** = Distance from the rotation axis to the center of mass (in cm)

---

## 3. Calculations for 1 kg Load

### **Joint 3 (Gripper Joint)**
- Distance to load: **4 cm**
- Torque:  
\[
T = 1 \, kg \times 4 \, cm = 4 \, kg·cm
\]

---

### **Joint 2 (Middle Joint)**
- Distance to load: **10 cm** (second segment) + **4 cm** (gripper) = **14 cm**
- Torque:  
\[
T = 1 \, kg \times 14 \, cm = 14 \, kg·cm
\]

---

### **Joint 1 (Base Joint)**
- Distance to load: **15 cm** (first segment) + **10 cm** (second segment) + **4 cm** (gripper) = **29 cm**
- Torque:  
\[
T = 1 \, kg \times 29 \, cm = 29 \, kg·cm
\]

---

## 4. Recommended Servo Motors

| Joint             | Required Torque (kg·cm) | Example Servo Model | Torque Rating (kg·cm) |
| ----------------- | ----------------------- | ------------------- | --------------------- |
| Joint 3 (Gripper) | ≥ 4                     | MG996R / DS3218     | 9–20                  |
| Joint 2 (Middle)  | ≥ 14                    | DS3218              | 20                    |
| Joint 1 (Base)    | ≥ 29                    | JX PDI-HV5932MG     | 30                    |

---

## 5. Case for 2 kg Load with Gears
For **2 kg**:

- Joint 3: \( 2 * 4 = 8 \, kg·cm \)  
- Joint 2: \( 2 * 14 = 28 \, kg·cm \)  
- Joint 1: \( 2 * 29 = 58 \, kg·cm \)  

If the servo torque is not enough, we can use **gear reduction** to increase torque.  
Example: A 2:1 gear ratio doubles the torque but halves the speed.

---

## 6. Drawbacks and Solutions

**Drawbacks**:
- Higher torque servos are heavier and more expensive.
- Increased current consumption.
- Slower movement if using gears.

**Solutions**:
- Choose higher torque servos.
- Use gear reduction to increase torque.
- Reduce the load weight or arm length.

---

## 7. References (Purchase Links)
- [DS3218 Servo on Amazon](https://www.amazon.sa/-/en/ZOSKAY-DS3218-Digital-Waterproof-Control/dp/B01MU7TQV8)
- [MG996R Servo on Amazon](https://www.amazon.sa/-/en/Deegoo-FPV-4-Pack-MG996R-Digital-Helicopter/dp/B07MFK266B?th=1)
- [JX PDI-HV5932MG Servo on Amazon](https://www.amazon.com/JX-Servo-PDI-HV5932MG-Torque-Digital/dp/B07SW44D53)
