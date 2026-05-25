#include <Servo.h>

int in3 = 3;
int in4 = 4;
int enb = 5;
int incomingByte;
int servoPin = 10;
int shootPin = 11;
int dribblePin = 12;
int stopPin = 13;

Servo servo;

void setup() {
  Serial.begin(9600);
  servo.attach(10);
}

void loop() {
  if (digitalRead(dribblePin) == HIGH) {
    Serial.println("dribbling");
    servo.write(120);
    dribble();   
  } else if (digitalRead(shootPin) == HIGH) {
    Serial.println("shooting");
    servo.write(135);
    shoot();
  } else if (digitalRead(stopPin) == HIGH) {
    Serial.println("stopping");
    servo.write(60);
    stop();
  }
}

void dribble() {
  digitalWrite(in3, HIGH);
  digitalWrite(in4, LOW);
  analogWrite(enb, 100);

  digitalWrite(servoPin, LOW);
}

void shoot() {
  digitalWrite(in3, LOW);
  digitalWrite(in4, HIGH);
  analogWrite(enb, 255);

  digitalWrite(servoPin, LOW);
}

void stop() {
  digitalWrite(in3, LOW);
  digitalWrite(in4, LOW);
  analogWrite(enb, 0);

  digitalWrite(servoPin, LOW);
}
