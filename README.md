# Project 10

## Project Goals
The goal of this project is to:
1.	familiarize students with **2D Arrays**
    - use the <a href="https://erinkeith.github.io/135/quick_guides/2d_arrays">2D Arrays Quick Guide</a> for short syntax reminders!
2.	provide students with continued practice using **everything else!**
    - use my <a href="https://erinkeith.github.io/cs135">website</a> for refreshers on previous topics!
   
## Important Notes
1.	**Filename**: Save your program as `memory.c`

# Program
Don't forget to remember!

## Background
This project is loosely based on the game <a href="https://en.wikipedia.org/wiki/Concentration_(card_game)">Concentration</a>, but with the modifications outlined below.

## Behavior
The game should start by displaying a grid which represents where “cards” are on the board. The user should be prompted for board locations of two cards they’d like to look at. The symbols in those locations are then revealed to the user. If they match, the user also sees a message and those symbols are displayed on the board for the rest of the game. 

The user is then prompted to continue playing. If they choose to keep playing, they are prompted for more card locations until they’ve matched all the pairs or choose not to continue playing, at which point the state of their game is saved for the next time they start the program.  

The user may enter a card location even if they’ve already discovered a match there. If a user enters a location which would be out of bounds of the board, they should receive an error message and be prompted to enter a new location. 

## Hints
- If you want to reset the game, you have to modify the `saved_game.txt` file.
- **Remember!** If a chunk of code starts to feel too complicated because it's doing too much, you may need to split it up into functions!
- My program had **9** functions
    - I had **2** functions with a `FILE*` parameter.
    - I did ***NOT*** have any functions which used explicit [pass by address](https://erinkeith.github.io/135/quick_guides/pass_by_address) syntax (with pointers).
    - **7** of my functions had **2D Array** parameters (which are automatically passed by address), **5** of which used the `const` keyword to prevent the arrays from being modified.

## Requirements
- Your program must have ***at least 6 functions***, in addition to the `main` function.
- **You may *NOT* use any libraries other than `stdio` and `stdbool`.**
- All opening and closing of files must be done in the `main` function.
   - This is a very good practice for testing, [coupling](https://en.wikipedia.org/wiki/Coupling_(computer_programming)), and [cohesion](https://en.wikipedia.org/wiki/Cohesion_(computer_science)). Even though you'll learn more about these concepts later, we're going to start some good habits now!
- If the file cannot be opened in one of the modes, the program should end before anything else happens.
   - While there should be a check for opening the file to modify, you should not be able to force this behavior to execute.
   - However, you _can_ test when the program fails to open the file to read.
- The games state file should be called `saved_game.txt`.
   - An initial version of the `saved_game.txt` file with a new game is included in this repository. 
   - Your program should use the `saved_game.txt` file to "load" the game state before playing the game.
   - Your program should overwrite the `saved_game.txt` file with the current game state when the user chooses to quit playing the game.
- Global variables are not allowed.
- Function parameters should be used to provide input to a function or to return multiple values from a function through pass by address.
    - Do not use parameters as a way to avoid declaring local variables.
- Parameters are for storing function input and/or using *pass by address* to output multiple values.
    - They should not be used as substitutes for *local variables*.

## Example Program Execution
An example executable (program) is provided in this repository. You should be able to run it from your project folder after cloning the repository in your Linux environment, in the same way you would run an executable you create.
- To **_run_** the example executable, use the ```./memoryExecutable``` command after changing directories into your repository folder.
- If you encounter a **permission denied** error when attempting to run the executable, use the ```chmod u+x memoryExecutable``` command in the terminal before trying again (using the command above).

# Extra Credit
***Extra credit code will not be graded unless the required functionality described in the previous sections is complete.***
   
## Important Notes
1.	**Filename**: Save your extra credit program in a different file called `memory_ec.c`
2.	Submitted code will be graded for up to 25% extra points.

# Program
Sometimes my memory can be so random!

## Behavior
Add the option to randomly generate a new game by incorporating a menu at the start of the game.

## Requirements
- In addition to the functionality described above, make sure that if the user chooses to play a saved game but that game is already "complete", a new game is generated automatically.
- In addition to `stdio` and `stdbool`, **you may use the `stdlib` and `time` libraries**  to generate random positions when creating a new game.
    - We'll go over the `srand()`, `time()` and `rand()` functions briefly in class. In the meantime, you can find more information <a href="https://www.w3schools.com/c/ref_stdlib_srand.php">here</a>.

## Example Program Execution
An example executable (program) is provided in this repository. You should be able to run it from your project folder after cloning the repository in your Linux environment, in the same way you would run an executable you create.
- To **_run_** the example executable, use the ```./ecMemoryExecutable``` command after changing directories into your repository folder.
- If you encounter a **permission denied** error when attempting to run the executable, use the ```chmod u+x ecMemoryExecutable``` command in the terminal before trying again (using the command above).
