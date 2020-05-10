# PCA9685-PWMExpander
PharoTings code for the PCA9685 I2C PWM expander

I am the driver for the PCA9685 16 port PWM/Servo extender.
I am controlled through the I2C bus. There can be 62 of me on the bus. 

You can change my frequency  (30 - 3000 Hz) and on/off ratio. 
I start in sleep mode.
 
The internal clock is nominally 25 MHz. If you need more precise timing, you can alter this for use in the internal calculations (>>adjustedClockFrequency:).

Pin numbers run from 0 to 15, because that is what is used in the datasheet and also on the print.

Main methods: 
>>wakeUp - start from sleep
>>frequency: - freqeuncy. Typically 50 Hz for driving servo motors, or up to 3000 Hz for LEDs
>>pwmForPin:  microSeconds: - on-time, used for servos in range 500 - 2500
pwmForPin:  percentage: - percentage on-time 
pinOn: and pinOff: - to turn a pin fully ON or OFF
