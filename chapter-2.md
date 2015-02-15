#Chapter 2


##Looping a triangle

Write a loop that makes seven calls to console.log to output the following triangle:

```javascript
#
##
###
####
#####
######
#######
```

#### Solution

```javascript
var content = '';

for (var i = 0; i < 7; i++) {
    content = content + '#';
    console.log(content);
}
```


##FizzBuzz

Write a program that uses console.log to print all the numbers from 1 to 100, with two exceptions. For numbers divisible by 3, print `Fizz` instead of the number, and for numbers divisible by 5 (and not 3), print `Buzz` instead.

When you have that working, modify your program to print `FizzBuzz`, for numbers that are divisible by both 3 and 5 (and still print `Fizz` or `Buzz` for numbers divisible by only one of those).

#### Solution

```javascript
for (i=1; i<=100; i++) {
    if ( !(i%5) && !(i%3) ) {
        console.log('FizzBuzz');
    } else if ( !(i%5) && (i%3)) {
        console.log('Buzz');
    } else if ( !(i%3) ) {
        console.log('Fizz');
    } else {
        console.log(i);
    }
}
```


##Chess board

Write a program that creates a string that represents an 8×8 grid, using newline characters to separate lines. At each position of the grid there is either a space or a `#` character. The characters should form a chess board.

Passing this string to `console.log` should show something like this:

```javascript
 # # # #
# # # #
 # # # #
# # # #
 # # # #
# # # #
 # # # #
# # # #
```
When you have a program that generates this pattern, define a variable `size = 8` and change the program so that it works for any `size`, outputting a grid of the given width and height.

#### Solution

```javascript
var size = 8;
var block = '#';
var space = ' ';

for (var i = 1; i <= size; i++) {
  var line = '';

  for (var y = 1; y <= size; y++){
    if (i%2) {
        if (y%2) {
            line = line + space;
        } else {
            line = line + block;
        }
    } else {
        if (y%2) {
            line = line + block;
        } else {
            line = line + space;
        }
    }
  }

  console.log(line);
}

```