# We all have made mistakes and will continue to, learn from them.

# List of mistakes and explanations:
1. Color Sensor
    1. Possible Strange I2C, navx2 I2C passthrough acting weird
    2. Cable is too long!
    3. Color sensor got crushed, cable unplugged
2. REV Robotics motor controller settings do not save reliably through code!
    - The terms "droopy arm" and "droopy gripper" still send chills down our spines. We wrongly configured the motor controller constants programmatically (through code) and then "burned" the flash (saved settings to persistent storage). There is a problem when doing this. The settings do not stick reliably. Every time the robot is turned on, there is a high chance of some of the constants not being configured properly. They are instead set to defaults. The defaults are 0 for PID constants, if it is zero, the motor will not react at all when target values are being set. Hence, the droopy appendages.
3. Limit switch
    - 

# Unverified issues
1. Gremlins on Roborio 2 caused by use of PWM ports?
2. Blinkin leds causing issues?


# Sensor usage issues
1. Limelight	
Make sure you save your pipeline settings
Make sure limelight software is up to date
Network switch may cause problems when used with limelight

2. Limit switch
    - Not setting the click position correctly
    - Make sure its mounted securely
        - Issue with zip tied limit switch slowly slipping back
    - Make sure cables are away from other robots or sharp metal areas
    - Small limit switch close to arm socket doesn't give much precision
    - Small limit switch gets bent/damaged over time



# Shuffleboard:
Be careful with camera bandwidth on shuffleboard
Be careful with too many widgets updating too often
	Causes loop overrun warning

# Swerve drive encoders:
Make sure encoder magnets are glued down and that they don't slip around
Whenever modules are taken apart double check swerve steering offsets
Make sure PID constants are good for swerve steering

# Network switch:
Don’t run roborio through switch, then to radio
