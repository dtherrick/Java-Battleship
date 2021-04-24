Summary of the Steps Needed to Add a Row and a Column
-----------------------------------------------------

**TO ADD A ROW AND A COLUMN:**
`Grid.java`
1. change value of Grid.NUM_ROWS and Grid.NUM_COLS to equal 11.

`Battleship.java`   
1. In `Battleship.setup()` change:
   1. Line 144: "A-J" becomes "A-K"
   2. Line 147: "1-10" becomes "1-11"
2. In `Battleship.convertLetterToInt()` add a case statement for "K" that mirrors what is done for "A" - "J"
3. In `Battleship.convertIntToLetter()` add a case statement for 10 that mirrors what is done for the other valid values.
4. In `Battleship.convertUserColToProCol()` add a case statement for 11.
5. In `Battleship.convertCompColToRegular()` add a case statement for 10.
6. In `Battleship.setup()` line 158: make sure col is <= 10, not 9 as it is to start.
7. In `Battleship.setupComputer()` lines 203 and 204: make sure column total is to 10, not 9.
8. In `Battleship.hasErrors()` line 231: set row to 11 not 10
9.  In `Battleship.hasErrorsComp()` line 292 and line 303: checker is < 11, not 10
10. In `Battleship.compMakeGuess()` lines 51, 52, 57, 58 make sure upper bound is 10
11. In `Battleship.askForGuess()`:
    1.  Line 95: A-K
    2.  Line 101: 1-11
    3.  Line 108: col <= 11