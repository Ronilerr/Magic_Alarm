#  Light & Motion Reactive Harry Potter Melody

This Arduino project combines a **buzzer**, **light sensor**, **ultrasonic sensor**, and **LED** to play a portion of the *Harry Potter* theme song. The melody playback dynamically reacts to ambient **light levels** and stops automatically upon detecting **motion**.

---

## Features

- **Motion Detection**: Uses an ultrasonic sensor to detect changes in distance.
- **Light-Based Frequency Adjustment**: Increases tone frequency when light level is high.
- **Auto-Stop Music**: Music stops playing when movement is detected.
- **LED Indicator**: LED turns on while music is playing.
- **10-Second Delay**: Starts playing after a short delay to give the system time to settle.

---

## Hardware Requirements

- 1 x Arduino-compatible board (ESP32 recommended)
- 1 x Piezo Buzzer
- 1 x Ultrasonic Sensor (HC-SR04 or similar)
- 1 x Light Sensor (e.g., photoresistor or analog light sensor)
- 1 x LED
- Resistors as needed (e.g., 220Ω for LED)
- Breadboard and jumper wires

---

##  Pin Configuration

| Component        | Pin (ESP32)     |
|------------------|-----------------|
| Buzzer           | 26              |
| Light Sensor     | 34 (Analog In)  |
| LED              | 13              |
| Ultrasonic Trigger | 16            |
| Ultrasonic Echo  | 17              |

---

##  How It Works

1. **Startup Delay**: Waits 10 seconds after powering on.
2. **Music Playback**: Plays a Harry Potter melody.
3. **Light Response**: Adjusts the pitch of notes if ambient light is above a set threshold.
4. **Motion Detection**: Monitors for motion using ultrasonic sensor. If motion is detected:
   - Music stops
   - LED turns off
   - Execution halts

---

##  Melody

The melody played is a recognizable snippet of the Harry Potter theme, controlled via a `melody[]` array with corresponding `durations[]`.

You must include the `pitches.h` file which defines standard note frequencies:
```cpp
#define NOTE_D4 294
#define NOTE_G4 392
...
