HELLO ! The code assumes you have:

2 IR sensors connected to the Arduino.
1 motor connected through a relay or motor driver.
2 fans connected through relays or motor drivers.
Circuit Setup
IR Sensor 1: Output pin connected to Arduino digital pin 2.
IR Sensor 2: Output pin connected to Arduino digital pin 3.
Motor: Controlled via a relay/motor driver, connected to Arduino digital pin 4.
Fan 1: Controlled via a relay/motor driver, connected to Arduino digital pin 5.
Fan 2: Controlled via a relay/motor driver, connected to Arduino digital pin 6.

How It Works :

IR Sensors: When both sensors detect an object (both irSensor1 and irSensor2 return HIGH), the sequence starts.
Motor Activation: The motor connected to motorPin turns on for 10 seconds.
Fan Activation: After the motor stops, both fans (connected to fan1Pin and fan2Pin) turn on for 40 seconds.
Notes :

Adjust the pin numbers in the code according to your wiring.
Ensure you have appropriate protection circuits (like diodes) for relays or motor drivers.
Test each component (motor, fans, sensors) individually before running the complete setup.





