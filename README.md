# RoboArmControl
//Controlling Robotic arm using servo motor
#include <Servo.h>
Servo servo1;
Servo servo2;

int pot1=A1;
int pot2=A2;

int valpot1;
int valpot2; 
void setup()
{
servo1.attach(3);
servo2.attach(9);
}
void loop()
{
valpot1 = analogRead(pot1);
valpot1=map(valpot1, 0 ,1023, 0, 180);
servo1.write(valpot1);
delay(15);  
valpot2 = analogRead(pot2);
valpot2= map(valpot2, 0 ,1023, 0, 180);
servo2.write(valpot2);
delay(15);
}
