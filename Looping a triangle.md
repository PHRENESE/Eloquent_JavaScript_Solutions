http://eloquentjavascript.net/02_program_structure.html#h_umoXp9u0e7

Write a loop that makes seven calls to console.log to output the following triangle:

#
##
###
####
#####
######
#######

```javascript
function oneMore(num, str) {
  var line = "";
  for (i = 0; i < num; i++) {
    console.log(line += str);
  } 
}
oneMore(7, "#");
```
