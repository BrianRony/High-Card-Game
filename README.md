# High Card Game By Byte Brigade

## Introduction
This is a simple card game implemented in JavaScript. The game simulates a competition between a user and a computer. The goal of the game is to reach a high score of 5 by drawing and comparing cards.

## Game Rules
The game is played with a deck of 13 cards, with each card having a value from 1 to 13. At the beginning of the game, both the user and the computer have a score of 0. The game proceeds in turns, with the user going first.

During each turn, the user can choose to "shuffle" or "hold". If the user chooses to shuffle, a random card is dealt to the user and the user's score is updated accordingly. The user can shuffle up to a certain limit, which is reset at the beginning of each turn. If the user chooses to hold, a random card is dealt to the computer and the cards are compared. The player with the higher card value wins the round and their score is updated.

The game continues in this manner until one of the players reaches the high score, at which point the game ends and the winner is displayed.

## Code Structure
The code is organized into several functions, each responsible for a specific aspect of the game. Here's a detailed overview of the functions:

### newGame()
This function resets the game, including the scores, shuffle limits, and card images. It is called when the "New Game" button is clicked. The function first resets the scores and shuffle limits to their default values. It then resets the card images to the back of the card and updates the player titles to "Player" and "Computer". Finally, it enables the "Shuffle" button.

### shuffle() 
This function deals a random card to the user. It is called when the "Draw Card" button is clicked. The function first checks if the user's score is not equal to the high score. If it is, the function does nothing. Otherwise, the function resets the player title to "Player" and the computer's card image to the back of the card. It then generates a random number between 1 and 13, which represents the card value. The function updates the user's card image to the corresponding card and updates the user's score. Finally, the function decrements the shuffle limit and enables the "Hold" button if the shuffle limit is greater than 0.

### hold()
This function deals a random card to the computer, compares the cards, and updates the scores. It is called when the "Hold" button is clicked. The function first checks if the user's score is not equal to the high score. If it is, the function does nothing. Otherwise, the function generates a random number between 1 and 13, which represents the computer's card value. The function updates the computer's card image to the corresponding card and compares the card values. If the user's card value is higher, the user's score is incremented. If the computer's card value is higher, the computer's score is incremented. If the card values are equal, neither score is incremented. Finally, the function resets the shuffle limit to 3 and disables the "Hold" button.

The code also uses the HTML DOM to manipulate the webpage elements, such as changing the text of an element or the source of an image.

## How to Play
To play the game, follow these steps:

1. Click the "New Game" button to start a new game.
2. Click the "Shuffle" button to draw a random card and update your score.
3. Repeat step 2 until you are satisfied with your score.
4. Click the "Hold" button to let the computer draw a card and compare the cards.
5. Repeat steps 2-4 until one of the players reaches the high score.

## Conclusion
This simple card game is a fun and engaging way to learn about JavaScript and HTML DOM manipulation. With its clear rules and intuitive interface, it is suitable for players of all skill levels. The game demonstrates the use of functions, variables, conditional statements, and loops to create a dynamic and interactive experience. It also showcases the power of the HTML DOM to manipulate webpage elements and create a visually appealing game. Overall, this simple card game is a great starting point for anyone interested in learning JavaScript and web development. Enjoy!