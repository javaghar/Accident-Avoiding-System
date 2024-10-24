
          CODING
// Constants const int trigPin
= 4; const int echoPin = 2;
const int buzzerPin = 8;
const int led = 7;
// Setup void setup() {
pinMode(trigPin, OUTPUT);
pinMode(echoPin, INPUT);
pinMode(buzzerPin, OUTPUT);
pinMode(led,OUTPUT);
}
// Loop void
loop() {
long duration, distance;
// Send a short pulse on the trigger pin
digitalWrite(trigPin, LOW);
delayMicroseconds(2); digitalWrite(trigPin,
HIGH); delayMicroseconds(10);
digitalWrite(trigPin, LOW);
// Measure the time it takes for the pulse to return
duration = pulseIn(echoPin, HIGH);
// Convert the time into a distance distance =
(duration/2) / 29.1;
// If the distance is less than 200 cm, turn on the buzzer
// Otherwise, turn off the buzzer if
(distance < 200) {
digitalWrite(buzzerPin, HIGH);
digitalWrite(led,HIGH);
11
delay(500); } else
{
digitalWrite(buzzerPin,LOW); digitalWrite(led,LOW);
delay(500);
}
}
