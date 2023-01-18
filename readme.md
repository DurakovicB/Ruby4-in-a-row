# Connect Four

Connect Four is a two-player connection board game, in which the players take turns dropping tokens into a vertically suspended grid. Whichever player manages to **connect 4 tokens** of the same token horizontally, vertically or diagonally wins the game.

The project was done as part of the **IT 305 Programming Languages** course at International Burch University, and implemented in the **Ruby** programming language.

## Team members
- [Bilal Duraković](https://github.com/DurakovicB/)
- Edvin Obralija
- [Ishak Kazić](https://github.com/)


## Running the project

To run the project, you will first need to install Ruby. You can follow the steps on [the official webpage](https://rubyinstaller.org/downloads/).

After installing Ruby, follow these steps to run the game:
```
git clone https://github.com/DurakovicB/Ruby4-in-a-row
cd Ruby4-in-a-row
ruby 4-in-a-row-v2
```

## Project Explanation


This is a Ruby Connect 4 game, where two players take turns dropping colored discs into a grid, trying to get four of their own color in a row either horizontally, vertically, or diagonally. The initialize method is a constructor that sets up the state of a new Board object. It takes one argument, an integer. If the integer is 0, it creates a new, empty board. If the integer is 1, it loads a previously saved board from a file called reload.txt. If the integer is anything else, it raises a TypeError.

The print_board method prints the current state of the board to the console. The update_column method updates a column of the board by adding the current player's disc to the first empty position in that column. The empty_board method prompts the user to enter the width and height of the board, and then creates a new, empty board with those dimensions. The loadBoard method loads a previously saved board from a file and updates the state of the Board object accordingly.

The full_row? method checks if a given row of the board is full, and returns true if it is, false otherwise. The winning_column_for_player? and winning_row_for_player? methods check if a given column or row, respectively, contains four consecutive discs of the current player's color. The winning_diagonal_for_player? method checks if there is a diagonal line of four consecutive discs of the current player's color on the board.

The game_over? method checks if the game is over by checking if the board is full or if any player has won. If the game is over, it returns true. Otherwise, it returns false. The play method implements the main game loop, where players take turns making moves until the game is over. The save method saves the current state of the board to a file called reload.txt.
The Board class is a Ruby class that represents the board for a Connect Four game. It has a number of methods that allow you to initialize the board, print the board, update the board by adding a piece to a column, check if a row is full, check if a player has won in a column or row, and save or load the board to/from a file.

The initialize method is the constructor for the Board class, and it has two cases:
•	If the first argument is 0, it initializes an empty board with the specified number of rows and columns. It also initializes the @@current_player variable to 1, the @@total_moves variable to 0, and the @@playeronemoves and @@playertwomoves arrays to empty arrays.
•	If the first argument is 1, it loads the board from a file called 'reload.txt'.
Here is a list of methods and a brief explanation of what they’re used for:
1.	The print_board method prints the current state of the board to the console. This method prints the board to the console. It prints a visual representation of the board, with X representing player 1's moves, O representing player 2's moves, and - representing empty spaces. It also prints a row of numbers at the bottom, representing the columns of the board.
2.	The update_column method adds a piece for the specified player to the specified column. This method updates the given column of the board by adding the move of the given player to the bottom-most available space in the column.

3.	The empty_board method prompts the user to enter the number of rows and columns for the board, and returns an empty board with the specified dimensions. This method returns an empty board with dimensions specified by the user at runtime. It prompts the user to enter the width and height of the board and continues to ask until the dimensions are within certain bounds.

4.	The loadBoard method loads the board from a file called 'reload.txt'. This method loads data from the file reload.txt to initialize the board. It reads the data and sets the instance variables of the Board object accordingly.

5.	The full_row? method returns true if the specified row is full (i.e., all positions are occupied), and false otherwise. This method returns a boolean indicating whether the given row is completely filled (i.e., it has no empty spaces).

6.	The winning_column_for_player? method returns true if the specified player has won in the specified column, and false otherwise. This method returns a boolean indicating whether the given column contains four consecutive moves made by the current player.

7.	The winning_row_for_player? method returns true if the specified player has won in the specified row, and false otherwise. This method returns a boolean indicating whether the given row contains four consecutive moves made by the current player.

8.	The winning_diagonal_for_player? method returns a boolean indicating whether the given diagonal (which is an array of board positions representing a diagonal of the board) contains four consecutive moves made by the current player.

9.	The check_vertical method checks if the specified player has won vertically in the board.

10.	The check_horizontal method checks if the specified player has won horizontally in the board.
11.	The check_diagonal method checks if the specified player has won diagonally in the board.

12.	The check_win method checks if the specified player has won in the board.

13.	The column_full? method returns true if the specified column is full (i.e., all positions are occupied), and false otherwise.

14.	 The game_over? method returns true if the game is over (i.e., either player has won or the board is full), and false otherwise. This method returns a boolean indicating whether the game is over, either because a player has won or the board is full.

15.	The play method allows the players to take turns adding pieces to the board until the game is over. This method represents a single turn in the game. It prompts the user to enter a column to play in, and then updates the board with the move. It also checks if the game is over after the move and declares a winner or a draw if necessary.

16.	The save_board method saves the current state of the board to a file called 'reload.txt'.
