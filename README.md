# sudokubuilder
Simple HTML/Javascript page that attempts to generate sudoku puzzles and solve them

## Why?
Just playing around, but I was interested to see how different the process of creating a puzzle was from solving one, how often one created invalid puzzles or had to make a nondeterminant guess, etc.  Turns out that the process of building a puzzle and solving one can be pretty similar, and that one can generally create a puzzle pretty reliably without conflicts for smaller sizes but not for larger sizes.  Or possibly more complex conflict-detection logic is required to create the bigger puzzles.

## What is it doing?
To build the puzzle it is just putting a number down and then filling in the next box that has the least number of options available.  That's why you will see it build in a pattern - filling up a box or a line first.  It is looking at the other numbers in each scope to see how many options there are for any particular box.  It is also animating so that you can see what it's doing at each step.  You can see it color boxes where there is only one choice.

If you tell it to create a puzzle, it is simply taking the completed puzzle and unsetting some random set of numbers.  Then you can click step-by-step and watch it try to solve.  If it has to "guess" at any point - choosing a box that has more than one option - then it will color that number as well.  It is randomly guessing when it has to guess, so you can undo back to the guess and let it choose something different to see if it is successful.
