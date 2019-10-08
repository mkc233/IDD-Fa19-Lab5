# IDD-Fa19-Lab5

Lab by Michael Chan

1. Arduino Code

```
#include <Servo.h>

Servo myservo;  // create servo object to control a servo
// twelve servo objects can be created on most boards

int pos = 0;    // variable to store the servo position
int button = 7;

void setup() {
  myservo.write(0);
  Serial.begin(9600);
  myservo.attach(9);// attaches the servo on pin 9 to the servo object
  pinMode(button,INPUT_PULLUP);
}

void loop() {
  Serial.print(digitalRead(button));
  if(digitalRead(button) == 0){
  for (pos = 0; pos <= 120; pos += 1) { // goes from 0 degrees to 180 degrees
    // in steps of 1 degree
    myservo.write(pos);              // tell servo to go to position in variable 'pos'
    delay(15);                       // waits 15ms for the servo to reach the position
   }
  }
}
```
2. Jack File
[Jack in the Box!](https://github.com/mkc233/IDD-Fa19-Lab5/blob/master/Jack%20in%20the%20box.jpg)
3. Photo
4. Video
