Car Game in C++
Overview
This is a simple console-based Car Game implemented in C++. The player controls a car using keyboard inputs, avoiding oncoming enemies (other cars) to score points. The game features a dynamic score system, enemy generation, collision detection, and a menu-driven interface.

Features
Dynamic Enemies: Randomly generated enemy cars moving towards the player.

Score Tracking: Points increase as enemies are avoided.

Collision Detection: Game over when the player's car collides with an enemy.

Menu System: Start game, view instructions, or quit.

Console-Based Graphics: Uses ASCII characters for rendering.

How to Play
Objective: Avoid incoming enemy cars to increase your score.

Controls:

A or a: Move the car left.

D or d: Move the car right.

ESC: Exit the game mid-session.

Game Over: Colliding with an enemy ends the game. Press any key to return to the menu.

Functions Explanation
1. gotoxy(int x, int y)
Purpose: Moves the console cursor to specified coordinates (x, y).

Usage: Essential for positioning text and game elements.

2. setcursor(bool visible, DWORD size)
Purpose: Controls cursor visibility and size.

Usage: Hides the cursor during gameplay for a cleaner look.

3. drawBorder()
Purpose: Draws the game's borders using + characters.

Details: Creates left, right, and outer boundaries.

4. genEnemy(int ind)
Purpose: Generates a random X-coordinate for enemy ind.

Range: Enemies spawn between columns 17 and 49.

5. drawEnemy(int ind) & eraseEnemy(int ind)
Purpose: Renders or removes an enemy car using ASCII art.

Condition: Only active enemies (flagged) are drawn.

6. resetEnemy(int ind)
Purpose: Resets enemy ind to the top of the screen with a new position.

Trigger: Called when an enemy exits the screen.

7. drawCar() & eraseCar()
Purpose: Draws or erases the player's car using the car[][] array.

Design: The car is a 4x4 ASCII art using + characters.

8. collision()
Purpose: Checks if the player's car collides with an enemy.

Logic: Compares enemy and car positions when enemies are near the bottom.

9. gameover()
Purpose: Displays a "Game Over" screen and returns to the menu.

Trigger: Called on collision detection.

10. updateScore()
Purpose: Updates and displays the current score on the right panel.

11. instructions()
Purpose: Shows game controls and rules.

12. play()
Purpose: Main game loop.

Handles player input (movement).

Manages enemy movement and spawning.

Updates the score and checks for collisions.

Runs at a fixed delay (Sleep(50)) for smooth gameplay.

13. main()
Purpose: Entry point with a menu system.

Options: Start Game, Instructions, Quit.

Uses getch() for menu navigation.

Compilation and Execution
Requirements:
Windows OS: Uses Windows-specific headers (windows.h, dos.h).

Compiler: Compatible with C++11 or newer (e.g., Code::Blocks, Dev-C++).

Steps:
Compile:

Run:
Copy
car_game.exe
Code Structure
Global Variables:

enemyY[], enemyX[]: Track enemy positions.

enemyFlag[]: Flags to activate enemies.

carPos: Player's car X-coordinate.
score: Current score.
Art Assets:
Player's car: Stored in car[4][4].
Enemies: Rendered as **** and ** patterns.

