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

class Maqueen contains following methods:

    # value: {0,1}
    def led_right(self, value):
    
    # red: {0-255}
    # green: {0-255}
    # blue: {0-255}
    def rgb_front_left(self, red, green, blue):
    
    # red: {0-255}
    # green: {0-255}
    # blue: {0-255}
    def rgb_rear_left(self, red, green, blue):
    
    # red: {0-255}
    # green: {0-255}
    # blue: {0-255}
    def rgb_rear_right(self, red, green, blue):
    
    # red: {0-255}
    # green: {0-255}
    # blue: {0-255}
    def rgb_front_right(self, red, green, blue):
    
    # speed: {0-255}
    # direction: {0,1}
    def motor_left(self, speed=0, direction=0):
    
    # speed: {0-255}
    # direction: {0,1}
    def motor_right(self, speed=0, direction=0):
    
    # return: {0,1}
    def line_left(self):
    
    # return: {0,1}
    def line_right(self):
    
    # angle: {0-180}
    def servo_one(self, angle=0):
    
    # angle: {0-180}
    def servo_two(self, angle=0):
    
    # Trigger (P1), Echo (P2)
    def ultrasound_measure(self): 
    
Create a single instane of the Maqueen class and call the member functions.

    robot = Maqueen()
    robot.led_right(1)
    
If you have a Maqueen robot and want to use this code. Have fun!    
