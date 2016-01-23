
http://eloquentjavascript.net/02_program_structure.html#h_5Hz2kiaaXp

Write a program that creates a string that represents an 8×8 grid, using newline characters to separate lines. At each position of the grid there is either a space or a “#” character. The characters should form a chess board.

Passing this string to console.log should show something like this:

" 0 0 0 0"
<br>
"0 0 0 0 "
<br>
" 0 0 0 0"
<br>
"0 0 0 0 "
<br>
" 0 0 0 0"
<br>
"0 0 0 0 "
<br>
" 0 0 0 0"
<br>
"0 0 0 0 "
<br>

When you have a program that generates this pattern, define a variable size = 8 and change the program so that it works for any size, outputting a grid of the given width and height.

My solution:
```javascript
function checkerMaker(size, symbols) {
  for (i = 0; i < size; i++) {
    var line = "";
    if (i % 2 === 0) {
      for (j = 0; j < (size/2); j++) {
        line += symbols;
      }
        console.log(line);  
    } else {
      var altSymbols = symbols.split("").reverse().join("");
      for (j = 0; j < (size/2); j++) {
        line += altSymbols;
      }
        console.log(line); 
    }
  }
}

checkerMaker(8, " #");
```
I knew I was repeating myself when I wrote the second inner for loop...

Marijn Haverbeke's solution (I took the liberty to pass symbol1 and symbol2 as args): 
```javascript
function checkerMaker(size, symbol1, symbol2) {
var board = "";
  for (var y = 0; y < size; y++) {
    for (var x = 0; x < size; x++) {
      if ((x + y) % 2 == 0)
        board += symbol1;
      else
        board += symbol2;
    }
    board += "\n";
  }
  console.log(board);
}
checkerMaker(8, " ", "#");
```
