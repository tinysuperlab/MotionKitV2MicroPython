# maqueen
micro:bit python library for the DFRobot Maqueen

To make some summmer holiday fun for a small group of kids with a few Maqueen robots.
We needed a simple microbit interface for programming with python.
And we needed it to run offline on linux, windows and mac.

The interface is implemented in 
- maqueen.py

It supports:
- motors
- servo motors
- red leds
- RGB leds
- ultrasound measurement in cm.
- line sensors

Please see the example py files to learn how each function is used.

- robot_frontlights.py
- robot_sidelights.py
- robot_motors.py
- robot_measuredistance.py
- robot_linesensors.py
- robot_servo.py

The Mu editor was used for coding.
All the files are copied to the mu_code folder.
maqueen.py is copied to the micro:bit.
One way to do is tobe copied use the Mu editor "Files" button.
Each example py file is programmed using the "Flash" button.

robot_servo.py requires an external servo motor such as SG90.
robot_measuredistance.py requires that the ultra sound sensor is mounted.

If you have a Maqueen robot and can use this code. Have fun!
