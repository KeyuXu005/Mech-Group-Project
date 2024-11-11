# Mech-Group-Project

The motor control and MPU6050 sensor codes were integrated into a single file to be executed using one Arduino board.

The motor encoder and PID control code were written based on this public repository:
https://github.com/curiores/ArduinoTutorials.git 

The codes for stabilising the DC motor at the start of operation were written by myself after observing that the motor always rotated to a random position while sending the configuration to the Arduino board. This random movement is detrimental to exoskeleton’s periodic motion, as it could cause unexpectedly large ROM fluctuations that might harm the user’s wrist. To prevent unintended rotation during setup, the motor was programmed to remain stationary for 500 system clock counts. This initialisation duration can be adjusted depending on PID controller performance, allowing optimal alignment with the target position at the motor's start.

The code for voltage variation was also added. These additional lines serve as the function to collect the data via Arduino serial port.

MPU6050 sensor code was created with the assistance of Adafruit sensor library:
 https://github.com/adafruit/Adafruit_MPU6050.git
