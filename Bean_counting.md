http://eloquentjavascript.net/03_functions.html#h_3rsiDgC2do

Write a function countBs that takes a string as its only argument and returns a number that indicates how many uppercase “B” characters are in the string.

Next, write a function called countChar that behaves like countBs, except it takes a second argument that indicates the character that is to be counted (rather than counting only uppercase “B” characters). Rewrite countBs to make use of this new function.

```javascript
function countBs(str) {
  var count = 0;
  for (i = 0; i < str.length; i++) {
    if (str.charAt(i) === "B") {
      count += 1;
    }
  }
  return count;
}

function countChar(str, letter) {
  var count = 0;
  for (i = 0; i < str.length; i++) {
    if (str.charAt(i) === letter) {
      count += 1;
    }
  }
  return count;
}

console.log(countBs("BBC"));
// → 2
console.log(countChar("kakkerlak", "k"));
// → 4
```
