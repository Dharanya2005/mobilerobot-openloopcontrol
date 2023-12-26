# MobileRobot-Openloopcontrol
## Aim:

To develop a python control code to move the mobilerobot along the predefined path.

## Equipments Required:
1. RoboMaster EP core
2. Python 3.7

## Procedure

# Step1:
Use from robomaster import robot

# Step2: 
Choose the x,y,z-axis movement distance(metres).

# Step3: 
Give ep_chassis.move to move straight.

# Step4: 
Give time.sleep() for a break.

# Step5:
 Give ep_chassis.drive_speed to have a circular movement.



## Program
```python


from robomaster import robot
import time
from robomaster import camera

if _name_ == '_main_':
    ep_robot = robot.Robot()
    ep_robot.initialize(conn_type="ap")

    ep_chassis = ep_robot.chassis
    ep_led = ep_robot.led
    ep_camera = ep_robot.camera

    print("Video streaming started.....")
    ep_camera.start_video_stream(display=True, resolution = camera.STREAM_360P)

    ep_chassis.move(x=2.64, y=0, z=0, xy_speed=1.0).wait_for_completed()
    ep_led.set_led(comp = "all",r=128,g=0,b=0,effect="on")

    ep_chassis.move(x=0.4, y=0, z=80, xy_speed=0.8).wait_for_completed()
    ep_led.set_led(comp = "all",r=255,g=0,b=0,effect="on")

    ep_chassis.move(x=1, y=0, z=0, xy_speed=1.0).wait_for_completed()
    ep_led.set_led(comp = "all",r=128,g=0,b=128,effect="on")

    ep_chassis.move(x=0, y=-1.5, z=0, xy_speed=1.2).wait_for_completed()
    ep_led.set_led(comp = "all",r=255,g=0,b=255,effect="on")

    ep_chassis.move(x=0, y=0, z=63, xy_speed=1.0).wait_for_completed()
    ep_led.set_led(comp = "all",r=128,g=0,b=128,effect="on")

    ep_chassis.move(x=1.6, y=0, z=0, xy_speed=1.0).wait_for_completed()
    ep_led.set_led(comp = "all",r=0,g=0,b=225,effect="on")

    ep_chassis.move(x=0, y=0, z=40, xy_speed=1.0).wait_for_completed()
    ep_led.set_led(comp = "all",r=128,g=0,b=128,effect="on")

    ep_chassis.move(x=1.35, y=0, z=0, xy_speed=1.0).wait_for_completed()
    ep_led.set_led(comp = "all",r=0,g=255,b=0,effect="on")

    ep_chassis.move(x=0, y=0, z=90, xy_speed=1.0).wait_for_completed()
    ep_led.set_led(comp = "all",r=0,g=0,b=128,effect="on") 

    ep_chassis.move(x=2, y=0, z=0, xy_speed=1.0).wait_for_completed()
    ep_led.set_led(comp = "all",r=255,g=102,b=0,effect="on")

    ep_chassis.move(x=0, y=0, z=80, xy_speed=1.0).wait_for_completed()
    ep_led.set_led(comp = "all",r=51,g=51,b=51,effect="on")    

    ep_chassis.move(x=0.6, y=0, z=0, xy_speed=1.0).wait_for_completed()
    ep_led.set_led(comp = "all",r=153,g=51,b=0,effect="on")    

    ep_chassis.move(x=0, y=0, z=0, xy_speed=0).wait_for_completed()
    ep_led.set_led(comp = "all",r=51,g=51,b=0,effect="on")   

    time.sleep(4)
    ep_camera.stop_video_stream()
    print("Stopped video streaming.....")

    ep_robot.close()

```

## MobileRobot Movement Image:

![robo](./img/robomaster.png)

![output](/WhatsApp%20Image%202023-12-26%20at%2018.00.02_45357ab0.jpg)


## MobileRobot Movement Video:

![IMAGE ALT TEXT HERE](https://youtu.be/p4HoSFZrcbQ?si=J8HucPYXssL-1JnK)

## Result:
Thus the python program code is developed to move the mobilerobot in the predefined path.


```
Mobile Robotics Laboratory
Department of Artificial Intelligence and Data Science/ Machine Learning
Saveetha Engineering College
```
