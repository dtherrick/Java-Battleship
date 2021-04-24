Summary of the Steps Needed to Add a Row and a Column
-----------------------------------------------------

* Warning - there is a TON of hardcoded values in here. That makes this more challenging than we'd like. But let's play anyway.
* Follow the initial code flow to understand how it sets up the board.
   * the rows and columns are in there.
   * Begin in `Battleship.java`. This is where the game initializes
     * Specifically: Line 7: `public static void main(String[] args)`
   * There are two instances of the `Player` class - one for the human, one for the computer.
   * Each player has its own `setup` function, so need to go into that.
   * Before doing that, understand what a `Player` class contains. It's in the file `Player.java`
   * A `Player` consists of:
     * Two native type constants:
       * An array with the ship lengths
       * An int with the total number of ships
     * A `Ship` array that describes the ships
     * A `Grid` for your board
     * A `Grid` for your opponent's board.
   * We likely want to look at how the grids are set up to determine how to add a row and a column.
   * Lines 7 and 8 look promising:
     * ```public static final int NUM_ROWS = 10;```
     * ```public static final int NUM_COLS = 10;```

**TO ADD A ROW AND A COLUMN:**
1. change value of Grid.NUM_ROWS and Grid.NUM_COLS to equal 11.
2. In `Battleship.setup()` change:
   1. Line 144: "A-J" becomes "A-K"
   2. Line 147: "1-10" becomes "1-11"
3. In `Battleship.convertLetterToInt()` add a case statement for "K" that mirrors what is done for "A" - "J"
4. In `Battleship.convertIntToLetter()` add a case statement for 10 that mirrors what is done for the other valid values.
5. In `Battleship.convertUserColToProCol()` add a case statement for 11.
6. In `Battleship.convertCompColToRegular()` add a case statement for 10.
7. In `Battleship.setup()` line 158: make sure col is <= 10, not 9 as it is to start.
8. In `Battleship.setupComputer()` lines 203 and 204: make sure column total is to 10, not 9.
9. In `Battleship.hasErrors()` line 231: set row to 11 not 10
10. In `Battleship.hasErrorsComp()` line 292 and line 303: checker is < 11, not 10
11. In `Battleship.compMakeGuess()` lines 51, 52, 57, 58 make sure upper bound is 10
12. In `Battleship.askForGuess()`:
    1.  Line 95: A-K
    2.  Line 101: 1-11
    3.  Line 108: col <= 11