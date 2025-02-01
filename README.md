

https://github.com/user-attachments/assets/1af90dc7-4f06-4379-9f57-1a645dd92d0a


Variables Declaration

•	ledPins[]: An array that holds the pin numbers {8, 9, 10, 11, 12} where the LEDs are connected.

•	brightness: A variable that tracks the brightness level of the LEDs.

•	fadeAmount: The amount by which brightness changes in each step (5).

•	index: A variable used as a loop counter to iterate through the LEDs.

Setup Function

•	The setup() function runs once when the program starts.

•	A while loop initializes each pin in ledPins[] as an output using pinMode().

•	The index variable is used to loop through all five LEDs.

Loop Function

•	The loop() function runs continuously, creating a fading effect on the LEDs.

•	It has two main phases:

Fading In All LEDs

1.	A while loop iterates through the ledPins[] array.
   
2.	Each LED is gradually brightened using fadeSettings(ledPins[index], true);.
   
Fading Out All LEDs

1.	Another while loop iterates through the ledPins[] array.
   
2.	Each LED gradually dims using fadeSettings(ledPins[index], false);.
   
Adjusting the Brightness

•	The brightness value is updated by adding fadeAmount.

•	If brightness reaches 0 or 255, fadeAmount is reversed (-fadeAmount), switching the fade direction.

fadeSettings(int pin, bool fadeIn) Function

•	This function controls the fading effect for a single LED.

•	It takes two parameters:

o	pin: The LED pin number.

o	fadeIn: A boolean (true for fading in, false for fading out).

•	Inside the function:

o	brightness is initialized to 0 if fading in or 255 if fading out.

o	fadeAmount is set to 5 for fading in and -5 for fading out.

o	A while loop gradually increases or decreases brightness using analogWrite(pin, brightness);.
o	A delay(30); is added to control the speed of the fade.

Program Behavior

•	LEDs fade in one by one, reaching full brightness.
•	Once all LEDs are bright, they fade out one by one.
•	This cycle repeats indefinitely, creating a smooth fading effect.
This program demonstrates how to control multiple LEDs with PWM (Pulse Width Modulation) using analogWrite(), making it ideal for smooth lighting effects. 🚀

