# Korine-Keira
 ROBOT ARM
![image](https://github.com/nwashin59/Korine-Keira/assets/75768362/6c7190f2-5bed-4516-b100-ed7512baf955)
4-Swervos, 1- Big batter pack, 1- Metro board  3 breadboards and one button 

This is a picture of our design, Our plan is to  pick up any chess piece and move it to another location on a chess board we will be using the Materials listed on the paper. 
3-14-24 Today I and Korine did research on what we wanted our code to look like and what we wanted our design to look like 


April: Had a lot going on towards the end of the month.


May: starting to get back into the swing of things and coming to class.

march 5: added the screws to the robot arm, made sure that the pipe goes up and down before added the thing that are listed in numbers. 
march 5: Before adding the base and the rest of the robot arm here is the plane picture of the robot arm. 
![Screenshot 2024-05-29 1 59 54 PM](https://github.com/nwashin59/Korine-Keira/assets/75768362/080a58ac-6f16-4f86-a2e3-bb5d045e886c) 
# Wiring
![image_50365441](https://github.com/nwashin59/Korine-Keira/assets/75768362/424694c5-93c0-47e2-b634-a23f8fd2a4cc)

# Code 
import time
import board
import pwmio
from digitalio import DigitalInOut, Direction, Pull
from adafruit_motor import servo
import asyncio
import keypad
import digitalio
from adafruit_motor import StepperMotor 

# Set up the digital pins used for the four wires of the stepper motor. 
coils = (
    digitalio.DigitalInOut(board.D9),   # A1
    digitalio.DigitalInOut(board.D10),  # A2
    digitalio.DigitalInOut(board.D11),  # B1
    digitalio.DigitalInOut(board.D12),  # B2
)

# Sets each of the digital pins as an output.
for coil in coils:
    coil.direction = digitalio.Direction.OUTPUT

# Creates an instance of the stepper motor so you can send commands to it (using the Adafruit Motor library). 
motor = stepper.StepperMotor(coils[0], coils[1], coils[2], coils[3], microsteps=None)

motor.onestep()

motor.onestep(direction=stepper.BACKWARD)
motor.onestep(direction=stepper.FORWARD)

style=stepper.DOUBLE
       


# create a PWMOut object on Pin A2.
pwm = pwmio.PWMOut(board.D13, duty_cycle=2 ** 15, frequency=50)# pin for servo 
pwm2 = pwmio.PWMOut(board.D8, duty_cycle=2 ** 15, frequency=50)

# Create a servo object, my_servo.
my_servo1 = servo.Servo(pwm)
my_servo2 = servo.Servo(pwm2)# names the servo pwm 


while True:
    for step in range(STEPS):
        motor.onestep(direction=stepper.BACKWARD, style=stepper.DOUBLE)# runs the stepper motor
        time.sleep(DELAY)
    
    for angle in range(0, 180, 5):  # 0 - 180 degrees, 5 degrees at a time.
        my_servo1.angle = angle
        my_servo2.angle = angle# tells what servo to move 
         my_servo3.angle
          my_servo4.angle
        time.sleep(DELAY)
   
    for step in range(STEPS):
        motor.onestep(style=stepper.DOUBLE)
        time.sleep(DELAY)
    for angle in range(0, 180, 5):  # 0 - 180 degrees, 5 degrees at a time.
        my_servo1.angle = angle
        my_servo2.angle = angle
         my_servo3.angle
          my_servo4.angle
        time.sleep(DELAY)

    for step in range(STEPS):
        motor.onestep(direction=stepper.BACKWARD, style=stepper.DOUBLE)
        time.sleep(DELAY)
            
    for angle in range(0, 180, 5):  # 0 - 180 degrees, 5 degrees at a time.
        my_servo1.angle = angle
        my_servo2.angle = angle
         my_servo3.angle
          my_servo4.angle
        time.sleep(DELAY)
 
# Robot Arm
![Screenshot 2024-05-30 6 32 12 PM](https://github.com/nwashin59/Korine-Keira/assets/75768362/4bed280c-f6f5-414f-9681-f6c2f6b8fd46)
![Screenshot 2024-05-30 6 31 42 PM](https://github.com/nwashin59/Korine-Keira/assets/75768362/25a7bb68-5dd1-4531-ac45-a432627bbca8)
![Screenshot 2024-05-30 6 30 48 PM](https://github.com/nwashin59/Korine-Keira/assets/75768362/1be0bccf-7d2e-4757-87cc-870356ed5d9a)
![Screenshot 2024-05-30 6 31 07 PM](https://github.com/nwashin59/Korine-Keira/assets/75768362/ae7e4707-e2ef-41fa-91f8-cf8b0744195f)
# Description

Korine- I was assigned to create a robot arm that can move up and down using a button. It's equipped with four servos that control its movement. This arm is designed for visual demonstration, so it's best to observe its operation without the need for 
hands-on interaction.

Keira- I was assigned to code and wiring I first started off with trying to find an idea for a code and realized it was taking up most of my time. but, I ended up improvising by using a classmate's code and tweaking it to make it my own. Then when I started wiring I looked up a wiring diagram but made a power rail on my own.


# Reflection 

When I look back at when I started building my robot arm, I realize it's been a mix of challenges getting it done. The phases Keira and I had to tackle were very interesting we had to dive deep into designs and coding structures, which was both exciting and a bit difficult. This project is about how are we going to get the long pole in the middle to move by using four servos. In order to complete this task we are using a button to control the up and down motion without using our hands. The metro & breadboard really put a lot of power into the pole.  Looking at the completed robot arm (In onshape), I'm proud of what we've accomplished even though we couldn’t get it done in time to print out. 
Keira- When it came to the wiring part, I had my hands full with hooking up the 4 servos, one big battery pack, the Metro board, three breadboards, and a button. It was like a puzzle, figuring out where each wire was supposed to go and making sure everything was connected just right for the robot arm to work smoothly. Even though we weren't able to finish the robot arm to see how it fully works, we managed to complete the CAD and wiring, which was very exciting.



# Part Link 
https://cvilleschools.onshape.com/documents/596a87a0916aa92c54febbfc/w/d19d9f3d74cc915f0fcf5605/e/8b970db120f13409126678fc?renderMode=0&uiState=665ddb188fb9501bc72f2b2f



