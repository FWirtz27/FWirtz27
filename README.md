In this assignment, you will be programming the classic computer game Snake. In this game, the player controls a snake that is moving across the screen. This snake will never stop moving, but the player can control the direction that the snake is moving in by using the arrow keys on the keyboard. The player has to try to move the snake in towards apples that appear on the screen. Every time that the snake eats an apple, it grows longer. When the snake hits itself, the game is over. Because the snake will increasingly grow longer as the game progresses, it continuously becomes harder to avoid collisions with the snake itself.

At the start of the game, the snake consists of two pieces, at the coordinates (0,0) and (1,0). The snake also has a direction that it will be moving in, which should be to the right at the start of the game. The snake should always be moving one coordinate in that direction per screen refresh, but the player can change the direction by pressing one of the arrow keys.

There should also be an apple on the screen at all times. If the snake hits the apple, the snake becomes one piece longer at the next screen refresh. A new apple should then be placed at a random empty coordinate, meaning that the apple should not be placed on top of the snake.

If the snake reaches the end of the screen, it should re-emerge on the other side.

Note that if the snake is moving in a certain direction, it can't move within in the opposite direction within one screen refresh (for instance, if the snake is going to the right and the player presses the left arrow key, nothing should happen).

This assignment uses the SnakeUserInterface from the LibUI. 

You can create one in the following way:

static final int WIDTH = 32;
static final int HEIGHT = 24;

SnakeUserInterface ui = UserInterfaceFactory.getSnakeUI(WIDTH, HEIGHT);
The width and height of the screen should be 32 and 24, respectively.

Information about the SnakeUserInterface can be found here. To generate a random location for the apple, you can use the method getRandom() from the UIAuxiliaryMethods class. This methos takes two parameters, both of type int. The method will return a random integer with as minimum value the first parameter (inclusive), and as maximum value the second parameter (exclusive). For example, UIAuxiliaryMethods.getRandom(0, 10) will return a random integer between 0 and 9.

Note: Before you start programming, think about how you are going to program this game. How will the snake and the apple be represented in your program? When will the snake be moving, and how will the snake be moving? Feel free to discuss this with your TA.

You are not allowed to import any classes other than Scanner, PrintStream, and any classes from the LibUI. Additionally, similar to the previous exercises, you are required to write your program in a structured manner, by dividing problems into subproblems, and solving those subproblems in a separate method in the appropriate class.
