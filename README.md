# CODE-FOR-ARDUINO-UNO-BASED-AUTOMATIC-HAND-WASHER-AND-DRYER
ARDUINO BASED AUTOMATIC HAND WASHER AND HAND DRYER 
How It Works :
IR Sensors: When both sensors detect an object (both irSensor1 and irSensor2 return HIGH), the sequence starts.
Motor Activation: The motor connected to motorPin turns on for 10 seconds.
Fan Activation: After the motor stops, both fans (connected to fan1Pin and fan2Pin) turn on for 40 seconds.
Notes :
Adjust the pin numbers in the code according to your wiring.
Ensure you have appropriate protection circuits (like diodes) for relays or motor drivers.
Test each component (motor, fans, sensors) individually before running the complete setup.
