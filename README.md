# Hengxu Fu
 
#include <Servo.h>

int led1Pin = 2;
int led2Pin = 3;
int servoPin = 9;

Servo myServo;

void setup() {
  pinMode(led1Pin, OUTPUT);
  pinMode(led2Pin, OUTPUT);

  digitalWrite(led1Pin, HIGH);
  digitalWrite(led2Pin, HIGH);

  myServo.attach(servoPin);
  myServo.write(0);
}

void loop() {
  
  myServo.write(360);
  delay(10000);

 
  myServo.write(0);
  delay(0); 
}
