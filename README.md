# Author: Alex Nguyen
## Gettysburg Colege

### Good morning, today I want to introduce to you guys reality game with my own embed system on the Arduino based car. The game is called “mBot crasher arcade.” My embedded system on the car involve the active use of sensors (line following, ultrasonic, and infrared) and devices (led, sound, and motor). It also optimizes the use of mathematics with the appearance of sigmoid function. But first, let’s talk about the rule of the game.

### Note: You can view the powerpoint, script, in the mBot Reference folder.

### In order to implement your own system into the mBot and test it out, follow these step:

- Download makeblock program from this [link](https://www.mblock.cc/en-us/download/)
- Import the file .mblock into the program by using File -> Import from this computer
- Connect to your mBot and click upload.
- Have fun.

-------------

## Here is some words (script I will present):

- [Slide 1] Good morning, today I want to introduce to you guys reality game with my own embed system on the Arduino based car. The game is called “mBot crasher arcade.” My embedded system on the car involve the active use of sensors (line following, ultrasonic, and infrared) and devices (led, sound, and motor). [Slide 2] It also optimizes the use of mathematics with the appearance of sigmoid function. But first, let’s talk about the rule of the game.

- [Slide 3] There are two players in the game. Each player controls an mBot by an infrared controller. Each mBot has its own point system, and one earn points by crashing to the other by the front of the his or her mBot. Or one can earn point by collecting black dot on the ground, this mean you have to move your top of the car over the black dot, so the line follower sensor can detect the black.

- And as the point goes up, the sound will be more frequent, and when one acheive the maximum of the point, the led light will turn green and his or her mBot will celebrate by playing a winning melody that I have put into it.
[Slide 4] Furthermore, the last rule of the game, we are not allowed to see the car, we are just allowed to see the front view of the car by viewing the camera from the car. For the restriction of the lack of hardware, the process of development is actually not done yet. So, I am demoing the version without virtual reality.

- [Slide 6] Now you all know how to play game, it’s simple right? But to win the game, you have to think a bit!
First, if you hit to their front, they will score points, too. So, try to hit into the opponent’s back or sides to actually gain point advantages. This seems like slither.io game but more reality huh? You can always rotate (Show) or do a wheelie (Show) to counter the opponent’s attack. Like this. (Show)

- Second, when the opponent is collecting black dots, stop them by crashing into them to change their angle. 
Third, you can always do a wheelie to step on other’s mBot. You will also gain point doing, too.

- [Slide 7] And last. Always remember, the point you earn when crashing is more than the point you earn on collecting black dots or stepping on others. But you can win if you step on black dots first and nobody stop you. So, choose your strategy wisely.

- [Slide 8] Now I really want to talk about the technology behind that. [Slide 9] There are four main ideas that makes the game that I really want to share with you. First is connection through infrared wave, next is ultrasonic sensor, next is line follower sensor, and last is a little bit of data processing algorithm.

- First is infrared wave processing. As you can see, the code is simple, if the key is pressed, then run the code. But to get what code responding to what button, there must involve encoding and decoding.
Second, I use ME Ultrasonic sensor library provided by makeblock. 
About line following controller, I expect that when the sensor detects black color, it would raise the point up.

- And lastly, I store the frequency data in order to calculate points in the point system. First, I normalize frequency data by subtracting the mean of hearable frequency value range, and then I put in to sigmoid function. Because the sigmoid function will always return value between the range of 0 and 1. So we can imagine that is percent point.

- So that’s the whole project, thank you very much. Enjoy.

----------------
