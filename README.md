# MotionKit
Calliope mini python library for the DFRobot/TinySuperlab MotionKit V2.

The interface library is implemented in 
- motionkit.py

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

robot_servo.py requires one or two external servo motor(s) such as SG90.
robot_measuredistance.py requires that the ultra sound sensor is mounted.


class Maqueen contains following methods:

    # value: 0,1
    def led_right(self, value):
    
    # red: 0-255
    # green: 0-255
    # blue: 0-255
    def rgb_front_left(self, red, green, blue)
    
    # red: 0-255
    # green: 0-255
    # blue: 0-255
    def rgb_rear_left(self, red, green, blue)
    
    # red: 0-255
    # green: 0-255
    # blue: 0-255
    def rgb_rear_right(self, red, green, blue)
    
    # red: 0-255
    # green: 0-255
    # blue: 0-255
    def rgb_front_right(self, red, green, blue)
    
    # speed: 0-255
    # direction: 0,1
    def motor_left(self, speed=0, direction=0)
    
    # speed: 0-255
    # direction: 0,1
    def motor_right(self, speed=0, direction=0)
    
    # return: 0,1
    def line_left(self)
    
    # return: 0,1
    def line_right(self)
    
    # angle: 0-180
    def servo_one(self, angle=0)
    
    # angle: 0-180
    def servo_two(self, angle=0)
    
    # return: distance in cm
    def ultrasound_measure(self)
    
Import the library and create a single instane of the Maqueen class and call the member functions.

    from maqueen import Maqueen
    robot = Maqueen()
    robot.led_right(1)
    
If you have a Maqueen robot and want to make use this code. Have fun!    
