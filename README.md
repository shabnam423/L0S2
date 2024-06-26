Introduction:
The provided code in connect4.c file, aims to play a game in the terminal of IDE. The game is called "Connect4", which is a fun game played by 2 players. I wrote this code in C as asked, and used stdio.h , time.h, stdlib.h libraries.
Code Structure:
I've used several functions in the code and added few comments for the understandability of some functions. The functions are predominantly invoked within the 'main' function, which serves as the primary entry point in the C programming language.
Function Descriptions:
As one of the important rules of programming, naming is necessary. I tried to name things as what they do. i hope you understand.
So, here is the functionality of each function (and some of the lines) in the simplest way:
-                       initialize_board()
It basically tells the computer "here is an empty array of char board[ROWS][COLS] which you should save in the memory". Time Complexity: It has to go through every cell in the board to set it to empty.

-                       void display_board()
This little dude will print the things we saved in previous function. 6 rows, each has 7 elements as wished.Time Complexity: It has to go through every cell in the board to print its content.

-                        CompOrUser()
As you see in main, after first two, i called this part of the code. Which does nothing but ask if the user wants to play against a bot or a friend of theirs.The comment in there is a simple note of the function:  '0'means against computer and '1' means against user.
And if user inputs something else than 'B' or 'U' (here they should take into consideration the case sensitivity), it'll ask again and again till they input one of the asked ones.Time Complexity: It just asks a single question and checks the answer, so it doesn't depend on the size of anything.

-                           gravity()
As you can guess, in real life connect4 game is with stones which will fall to the last row which has no element in inputted column. Well this is the explanation of this function. User just writes the column number and it automatically goes down till there is already an element. And returns the row number it was added to.Time Complexity: It has to check each row in the column until it finds an empty space. 

-                           checkThecell()
This function checks the content of the cell at the specified row and column indices on the game board. It returns an integer indicating the content of the cell: 0 for empty, 1 for a red token, and -1 for a yellow token.Time Complexity: It only has to look at one cell, so it doesn't matter how big the board is. Think of it like looking at a single item in a box; it doesn't take longer to find it if the box is bigger.

-                           CompTurn():
This function randomly selects a column for the computer's move.
Time Complexity: It does a fixed amount of work regardless of the size of the game board. Think of it like flipping a coin; it takes the same amount of time each time you flip it, no matter how many times you do it.

-                           checkWinner()
This function checks for a winner by iterating through the rows, columns, and diagonals of the game board.
Time Complexity: It has to look at every cell of the game board at least once, so the time it takes depends on the size of the board.

-                           The main() 
In here, it orchestrates the gameplay and alternates between user and computer turns until there is a winner.
The time complexity of main() depends on the complexity of the functions it calls, particularly checkWinner(), gravity(), and CompTurn().

Conclusion:
To sum up and put all the things in a nutshell we can say that the time complexity of the functions in the given code varies depending on the specific operations performed within each function. Overall, the time complexity of the program is primarily determined by the size of the game board, as most operations involve iterating through the board's cells.