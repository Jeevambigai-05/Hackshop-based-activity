Overview

This application features two guessing games: User Guessing and Machine Guessing. In the User Guessing mode, the computer selects a random number,
and the user attempts to guess it. In the Machine Guessing mode, the user thinks of a number, and the machine tries to guess it using a binary search strategy.

1. display_rules(mode)
This function displays the rules of the game based on the selected mode.

Parameters:
mode (str): Specifies which game's rules to display—either "User Guessing" or "Machine Guessing".
Functionality:
Uses Streamlit to create subheaders and write the rules in a user-friendly format.

2. user_guessing_game()
This function implements the User Guessing game.

Inputs:

User defines the lower and upper bounds for the guessing range and sets a maximum number of attempts.
Game Logic:

The game initializes a random secret number if it's a new game.
Users make guesses and receive feedback (too low, too high, or correct).
The game tracks the number of attempts and ends when the user either guesses correctly or reaches the maximum attempts.
Session State:

Utilizes Streamlit's session state to maintain the game's state across user interactions (e.g., secret number, attempts).

3. machine_guessing_game()
This function implements the Machine Guessing game.

Inputs:

Similar to the user guessing game, users set the bounds and maximum attempts, but they think of a number instead of guessing one.
Game Logic:

The machine guesses a number using a binary search method. After each guess, the user provides feedback.
The machine adjusts its guessing range based on the feedback (too low, too high, or correct).
The game also tracks the number of attempts and ends when the machine guesses correctly or reaches the maximum attempts.
Session State:

Like the user game, it uses session state to track the guessing range and attempts.

4. main()
The main function orchestrates the entire application.

Functionality:
Displays a title and allows the user to select the game mode.
Calls the display_rules() function to show the rules based on the selected mode.
Depending on the selected mode, it invokes either the user_guessing_game() or machine_guessing_game().
