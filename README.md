# Hengxu Fu
 
const int sensorPin = 2;
const int ledPin1 = 3;
const int ledPin2 = 4;
const int motorPin1 = 5;
const int motorPin2 = 6;

void setup() {
  pinMode(sensorPin, INPUT);
  pinMode(ledPin1, OUTPUT);
  pinMode(ledPin2, OUTPUT);
  pinMode(motorPin1, OUTPUT);
  pinMode(motorPin2, OUTPUT);
}

void loop() {
  int sensorState = digitalRead(sensorPin);

  if (sensorState == HIGH) {
    digitalWrite(ledPin1, HIGH);
    digitalWrite(ledPin2, HIGH);
    delay(1000);
    digitalWrite(ledPin1, LOW);
    digitalWrite(ledPin2, LOW);
    delay(1000);

    digitalWrite(motorPin1, HIGH);
    digitalWrite(motorPin2, HIGH);
  } else {
    digitalWrite(ledPin1, LOW);
    digitalWrite(ledPin2, LOW);

    digitalWrite(motorPin1, LOW);
    digitalWrite(motorPin2, LOW);
  }
}
