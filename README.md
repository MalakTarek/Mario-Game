# Mario-Game
This C++ program is a simple Mario-style game with a 10x10 grid. You control a champion ('C') to collect gems ('G') and avoid obstacles ('x'). The game ends when health reaches zero or 40 gems are collected. You can generate new maps and receive a win or loss message.

Here's a breakdown of the code:

    Libraries: The program includes several C++ libraries for various functionalities such as random number generation and console input/output.

    Class Definitions:
        Map: Represents the game map and handles map-related operations.
        Point: Represents a point on the map and is used for coordinates.
        Champion: Represents the player character (Champion) and contains information about their location, health, and score.
        Game: Controls the game flow, including initializing the map, champion, and handling player input and game logic.

    main Function: The main function is where the game starts. It does the following:
        Creates an instance of the Game class.
        Offers the option to generate a new random map when the game starts.
        Accepts user input (arrow keys) to move the champion within the map.
        Checks if the game is over (either the champion's health reaches zero or the champion collects all 40 gems).

Here's a brief summary of the key functionality:

    The map is represented as a 10x10 grid with "G" representing gems, "x" representing obstacles, "C" representing the champion, and "n" representing empty cells.
    The champion starts at the top-left corner (9, 0) with 100 health and 0 gems collected.
    The champion can move using arrow keys (8 for up, 5 for down, 6 for right, and 4 for left).
    The champion can collect gems ("G") to increase their gem score or collide with obstacles ("x") to lose health.

The game continues until the champion's health reaches zero or the champion collects all 40 gems, at which point it displays a "You Lost" or "You Won" message and terminates.
