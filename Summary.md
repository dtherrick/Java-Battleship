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