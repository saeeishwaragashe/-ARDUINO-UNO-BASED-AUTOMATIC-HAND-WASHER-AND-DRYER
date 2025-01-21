# CODE-FOR-ARDUINO-UNO-BASED-AUTOMATIC-HAND-WASHER-AND-DRYER
// Define pin connections
const int irSensor1 = 2; // IR Sensor 1 pin
const int irSensor2 = 3; // IR Sensor 2 pin
const int motorPin = 4;  // Motor control pin
const int fan1Pin = 5;   // Fan 1 control pin
const int fan2Pin = 6;   // Fan 2 control pin
void setup() {
  // Set up pins as input or output
  pinMode(irSensor1, INPUT);
  pinMode(irSensor2, INPUT);
  pinMode(motorPin, OUTPUT);
  pinMode(fan1Pin, OUTPUT);
  pinMode(fan2Pin, OUTPUT);

  // Ensure motor and fans are off initially
  digitalWrite(motorPin, LOW);
  digitalWrite(fan1Pin, LOW);
  digitalWrite(fan2Pin, LOW);

  Serial.begin(9600); // For debugging
}
void loop() {
  // Read the IR sensors
  int sensor1State = digitalRead(irSensor1);
  int sensor2State = digitalRead(irSensor2);
  // Check if both sensors detect an object
  if (sensor1State == HIGH && sensor2State == HIGH) {
    Serial.println("Both sensors triggered. Turning on motor...");
    // Turn on motor for 10 seconds
    digitalWrite(motorPin, HIGH);
    delay(10000); // Wait for 10 seconds
    digitalWrite(motorPin, LOW);
    Serial.println("Motor off. Turning on fans...");
    // Turn on both fans for 40 seconds
    digitalWrite(fan1Pin, HIGH);
    digitalWrite(fan2Pin, HIGH);
    delay(40000); // Wait for 40 seconds
    digitalWrite(fan1Pin, LOW);
    digitalWrite(fan2Pin, LOW);
    Serial.println("Fans off.");
  }
}







