This code implements a smart alarm system using an ESP32 with a combination of sensors
and outputs to create an interactive alarm experience. The system incorporates an ultrasonic
sensor for motion detection, a light sensor to adjust tone levels, and a buzzer to play a Harry
Potter theme melody. The alarm responds to motion and light levels, stops the music if
significant motion is detected, and adjusts the melody's tone based on light intensity.
The system also features an LED that serves as an indicator. The LED is turned on a few
seconds after the music starts playing, and it turns off once the motion threshold is
exceeded, indicating that the music has stopped due to detected motion.

Description of the Electronic Circuit:
The electronic circuit for this smart alarm system involves the following components
connected to an ESP32 microcontroller:
1. Ultrasonic Sensor (HC-SR04):
○ TRIGGER_PIN (Pin 16): Connected to the trigger pin of the ultrasonic sensor
to send the signal.
○ ECHO_PIN (Pin 17): Connected to the echo pin of the ultrasonic sensor to
receive the reflected signal and measure distance.
2. Light Sensor (Analog Sensor, e.g., LDR or photoresistor):
○ LIGHT_SENSOR_PIN (Pin 34): Connected to the analog pin of the ESP32 to
read the ambient light level. The sensor adjusts the tone of the music based on
light intensity.
3. Buzzer (for music playback):
○ BUZZER_PIN (Pin 26): Connected to a piezo buzzer to play the Harry Potter
melody when triggered by the alarm.
4. LED (Indicator light):
○ LED_PIN (Pin 13): Connected to a basic LED to visually indicate when the
music is playing. The LED is turned on when the music starts and turned off
when significant motion is detected

Demo: https://www.youtube.com/watch?v=zjsMZAP2yBw
