# Ultrasonic Parking Assistant System

A smart embedded system that detects nearby obstacles and assists drivers in avoiding collisions while parking. It uses an ultrasonic sensor to measure distance and provides real-time feedback via an LCD display, RGB LEDs, and a buzzer.

---

## Features

- Automatic Lighting Control based on ambient light intensity (LDR sensor).
- Fan Speed Control based on temperature readings from the LM35 sensor.
- Flame Detection & Alert System using a flame sensor and buzzer for emergencies.
- Real-Time Monitoring displayed on an LCD screen including:
  - Current Temperature
  - Light Intensity (as a percentage)
  - Fan status (ON/OFF)
  - Flame alerts

---

## Drivers Used

- GPIO – for controlling LEDs, buzzer, and sensors.
- ADC – to read analog values from LM35 and LDR.
- PWM – for controlling DC motor speed (fan).
- LM35 Sensor – for temperature measurement.
- LDR Sensor – for ambient light intensity detection.
- Flame Sensor – for fire/flame detection.
- LCD – for displaying real-time data and alerts.
- Buzzer – for flame detection alert.
- DC Motor – represents a fan controlled by PWM based on temperature.

---

## Hardware & Tools

- Microcontroller: ATmega32
- Development Tools: Eclipse / AVR-GCC / Proteus for simulation

## Display Format

```
Line 0: Distance=XX cm
```

- XX is the measured distance from the obstacle in centimeters.

---


## System Behavior

| Distance (cm) | LED Status              | Buzzer |
|---------------|--------------------------|--------|
| ≤ 5           | Red + Green + Blue ON    | ON     |
| 6–10          | Red + Green + Blue ON    | OFF    |
| 11–15         | Red + Green ON           | OFF    |
| 16–20         | Red ON                   | OFF    |
| > 20          | All LEDs OFF             | OFF    |

---

## Author

Yousef – Developed as part of the Standard Embedded Diploma course.

---

## License

This project is open-source and available under the [MIT License](LICENSE).
