# Servo-motor-Brushless-DC-control-system-using-Arduino.

# Brushless DC :
```
void setup()
{
   pinMode(13, OUTPUT);
   pinMode(12, OUTPUT);
  
}
void loop()
{
  digitalWrite(13, HIGH);
  digitalWrite(12, LOW);
}
```
![‪Circuit design Brushless DC _ Tinkercad - Google Chrome‬ 19_12_43 10_32_52 ص](https://user-images.githubusercontent.com/107868812/179477169-c21d0ea1-98e8-4ad4-aeb1-065bbd290f62.png)




https://user-images.githubusercontent.com/107868812/179477297-fbf78947-1e02-4529-bd60-fb656956a3c1.mp4



# Servo motor:

We are going to run a servo motor using Arduino
#the connection should be something like this

![‫بلا عنوان - Google Chrome‬ 19_12_43 11_58_14 ص](https://user-images.githubusercontent.com/107868812/179478345-1bde79ed-0d3b-4549-ae95-7a96ccfa2597.png)

- the black wire on the ground.
- red wire 5v.
- the third wire you can connect it with any pin, in my example it was pin 11

Now let's move to the coding part

to create a servo object to control a servo and variable to store the servo position
```
#include <Servo.h>

Servo myservo;  
int pos = 0;    
```
now attach the servo on pin 11 to the servo object
```
void setup() {

  myservo.attach(11);  

}
```
we are going to use for loop to goes from 0 degrees to 180 degrees, by using "Write" we tell servo to go to position
in variable 'pos'. using "delay" to waits 10ms for the servo to reach the position.
```
void loop() {

  for (pos = 0; pos <= 180; pos += 1) { 

    myservo.write(pos);              
    delay(10);                      
  }
  ```
  using for loop to move from 180 degrees to 0 degrees, tell servo to go to position in variable 'pos'. waits 10ms for the servo to reach the position
  ```
  for (pos = 180; pos >= 0; pos -= 1) { 
  myservo.write(pos);              
  delay(10);                       // waits 15ms for the servo to reach the position

}

}
```
the result should be like this: 




https://user-images.githubusercontent.com/107868812/179480795-0e59d491-8b5a-4815-aaa6-4876e0d55f9f.mp4

