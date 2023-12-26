Project Description: In this project, implementation has been done using a microcontroller, an LCD, a motor, a BUZZER, and a button for a microwave. The basic operation is as follows: a button for turning the microwave on or off is connected to port D1. Additionally, a button to stop the timer is considered and connected to port D6. For simulating the microwave door, I used another button connected to port D5. This microwave is programmed for three tasks:

1. PROGRAM1: The first program, with a short timer, is used for heating liquids.
2. PROGRAM2: The second program, with a timer in minutes, is used for heating food.
3. PROGRAM3: The third program, with a timer in hours, is used for cooking meals.

For each of these programs, a button is considered to prevent excessive wiring, using the DEFAULT tool from the Terminal section. Similarly, a button is implemented for reuse (RESTART) to enable reuse of the microwave after pressing the button again.

For the inside of the microwave, a motor and an LED are considered. The motor is connected to a transistor via a 1-kilohm resistor for on/off control of the current. On the other side, a POWER source is included. Like other microwaves that alert the user with a sound after completing the operation, I used a buzzer connected to a transistor so that it produces sound when the input current is obtained.

Finally, for displaying the timer, an LCD is used to show messages such as "Door Closed," "PAUSE," "READY," and "Press Buttons."

Code Description: This code includes two functions:

1. Process function: This function takes three inputs for setting the timer for operation. These three values are passed to it through the main function. After defining the necessary variables such as seconds, minutes, hours, and the LCD size, I wrote a while loop that continuously checks several conditions. In the first condition, it checks whether the microwave door is closed; otherwise, in the else part of this if statement, it displays the message "Close the door." In the second condition, it checks the PAUSE button; if this button is not pressed, the heating operation begins. If this button is pressed, in the else part, it stops the heating, motor rotation, and LED light and displays the "PAUSE" message to the user. If both conditions are true, we reach the second-counting operation. In this operation, we decrement the seconds one by one until it reaches 0. When it reaches zero, we decrement one unit from the minutes, and when the minutes reach 0, we decrement one unit from the hours. In the same manner, when all three units become 0, we stop the motor and other operations, clear the LCD, display the "READY" message, and alert the user with a buzzer about the completion of the operation.

2. Main function: In this function, using an if statement, I wrote that if the user turns on the microwave, the while loop starts working to prompt the user to select a button. If any button is pressed, the process function starts working with the given values. The first program runs for 15 seconds, the second program for 1 minute, and the third program for 2 hours. Note that buttons should be fully pressed.
