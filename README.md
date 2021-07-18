# maqueen
micro:bit python library for the DFRobot Maqueen

This code was made to have some summmer holiday fun for a small group of kids with a Maqueen robots.
We needed a simple microbit interface for programming with python.
And we needed it to run offline on linux, windows and mac.

The interface library is implemented in 
- maqueen.py

It supports:
- motors
- servo motors
- red leds
- RGB leds
- ultrasound measurement in cm.
- line sensors

Please try the example files to learn how each function is used.

- robot_frontlights.py
- robot_sidelights.py
- robot_motors.py
- robot_measuredistance.py
- robot_linesensors.py
- robot_servo.py

get the source with git

    git clone https://github.com/kholm777/maqueen


The Mu editor was used for coding.
All the files are copied to the mu_code folder.
maqueen.py is copied to the micro:bit.
One way to copy is to use the Mu editor "Files" button and drag the file to "your device".
Each example py file is programmed using the "Flash" button.

On the mac i had some problems flashing the software using Mu 1.1.0 beta 5. 
A workaround is to use the editor Thonny instead.

robot_servo.py requires one or two external servo motor(s) such as SG90.
robot_measuredistance.py requires that the ultra sound sensor is mounted.


class Maqueen contains following methods:

    # value: {0,1}
    def led_right(self, value):
    
    # red: {0-255}
    # green: {0-255}
    # blue: {0-255}
    def rgb_front_left(self, red, green, blue)
    
    # red: {0-255}
    # green: {0-255}
    # blue: {0-255}
    def rgb_rear_left(self, red, green, blue)
    
    # red: {0-255}
    # green: {0-255}
    # blue: {0-255}
    def rgb_rear_right(self, red, green, blue)
    
    # red: {0-255}
    # green: {0-255}
    # blue: {0-255}
    def rgb_front_right(self, red, green, blue)
    
    # speed: {0-255}
    # direction: {0,1}
    def motor_left(self, speed=0, direction=0)
    
    # speed: {0-255}
    # direction: {0,1}
    def motor_right(self, speed=0, direction=0)
    
    # return: {0,1}
    def line_left(self)
    
    # return: {0,1}
    def line_right(self)
    
    # angle: {0-180}
    def servo_one(self, angle=0)
    
    # angle: {0-180}
    def servo_two(self, angle=0)
    
    # return: distance in cm
    def ultrasound_measure(self)
    
Import the library and create a single instane of the Maqueen class and call the member functions.

    from maqueen import Maqueen
    robot = Maqueen()
    robot.led_right(1)
    
If you have a Maqueen robot and want to make use this code. Have fun!    
