#include <Servo.h>

#define button A0 
#define y_pin A1 
#define x_pin A2 

int Mode=0, flag=0;
 
int val_x=0, val_y=0;
int servo1, servo2;

Servo myservo1;
Servo myservo2;

void setup() { // put your setup code here, to run once 
pinMode(x_pin, INPUT);
pinMode(y_pin, INPUT);

pinMode(button, INPUT_PULLUP);

myservo1.attach(8); 
myservo2.attach(9);

delay(100); // Waiting for a while
}

void loop(){

if(digitalRead(button)==0){
if(flag==0){ flag=1;
Mode = !Mode;  
delay(100); 
 }
}else{flag=0;}

if(Mode==0){
val_y = analogRead(y_pin);
servo1 = map(val_y, 0, 1023, 20, 160);

val_x = analogRead(x_pin);
servo2 = map(val_x, 0, 1023, 20, 160);  
}

myservo1.write(servo1);
myservo2.write(servo2);

delay(10); 
}
