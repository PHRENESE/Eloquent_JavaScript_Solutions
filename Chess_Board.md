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

Marijn Haverbeke's solution: 
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
