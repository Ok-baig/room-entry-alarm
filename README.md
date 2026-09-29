# Room Entry Counter & Alarm

An Arduino project that counts how many times someone enters a room and sounds an alarm on every entry. Built using parts from an earlier push-up counter project.

## Features
- Counts entries using an ultrasonic sensor
- Alarm triggers automatically on every detected entry
- Displays "STOP" and sounds a continuous buzzer until stopped
- Short button press stops the alarm (count is kept)
- Long button press (2 sec) resets the counter and clears the alarm
- Logs entry timestamps over Serial (for future data analysis in Python)

## Parts Used
- Arduino Uno
- HC-SR04 Ultrasonic Sensor
- TM1637 4-Digit 7-Segment Display
- Buzzer
- Push Button
- Breadboard + Jumper Wires

## Wiring

| Component      | Pin  |
|-----------------|------|
| Display CLK     | 6    |
| Display DIO     | 7    |
| Sensor Trig     | 10   |
| Sensor Echo     | 9    |
| Buzzer          | 8    |
| Button          | 2    |
| VCC (all parts) | 5V   |
| GND (all parts) | GND  |

## How It Works
1. The sensor detects when someone comes within 45 cm and increases the counter.
2. The alarm turns on automatically: display shows "STOP" and the buzzer sounds continuously.
3. A short button press stops the alarm while keeping the current count.
4. Holding the button for 2 seconds resets the counter to zero and clears the alarm.
5. Every entry is logged with a timestamp over Serial for future data analysis.

## Future Improvements
- Log entry data to a file and visualize entry patterns using Python (pandas/matplotlib)
- Add an arm/disarm mode so the alarm can be turned off entirely
- Add an entry delay before the alarm triggers

## Author
Abdul Quddoos
