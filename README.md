# cs61a---Hog
In this project, we will develop a simulator and multiple strategies for the dice game Hog. We will need to use control statements and higher-order functions together.

In Hog, two players alternate turns trying to be the first to end a turn with at least 100 total points. On each turn, the current player chooses some number of dice to roll, up to 10. That player's score for the turn is the sum of the dice outcomes.

To spice up the game, we will play with some special rules:

Pig Out. If any of the dice outcomes is a 1, the current player's score for the turn is 1.

Example 1: The current player rolls 7 dice, 5 of which are 1's. They score 1 point for the turn.
Example 2: The current player rolls 4 dice, all of which are 3's. Since Pig Out did not occur, they score 12 points for the turn.
Free Bacon. A player who chooses to roll zero dice scores 2 * tens - ones, or 1, whichever is higher; where tens, ones are the digits of the opponent's score

Example 1: The opponent has 46 points, and the current player chooses to roll zero dice. 2 * 4 - 6 = 2; which is greater than 1, so the current player gains 2 points.
Example 2: The opponent has 73 points, and the current player chooses to roll zero dice. 2 * 7 - 3 = 11; which is greater than 1, so the current player gains 11 points.
Example 3: The opponent has 27 points, and the current player chooses to roll zero dice. 2 * 2 - 7 = -3; which is less than or equal to 1, so the current player gains 1 point.
Example 4: The opponent has 7 points, and the current player chooses to roll zero dice. 2 * 0 - 7 = -7; which is less than or equal to 1, so the current player gains 1 point.
Swine Swap. After points for the turn are added to the current player's score, if the absolute difference between the last two digits of the current score and the last two digits of the opponent's score are the same, the scores are swapped
