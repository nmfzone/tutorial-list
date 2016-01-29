# How to use GOlang
In this section, i will show you how to use GO programming languages

# Introduction
GOlang is programming language that created by Google inc.

## Setup The Environment

## Start working with code
### Compile and Running
* Goto your Golang working directory
* Type `go install`

### Retrive input from STDIN
##### The convention
Symbol | Description
------ | -----------
%d | int (signed decimal integer)
%u | unsigned decimal integer
%f | floating point values (fixed notation) - float, double
%e | floating point values (exponential notation)
%s | string
%c | character
##### Scanf()
```
Scanf() doesnt like getline() in C++ or nextLine() in Java
```

## Troubleshooting Errors
##### no new variables on left side of :=
[Reference](http://stackoverflow.com/questions/13329154/golang-no-new-variables-on-left-side-of)
Because use you use `:=` instead of `=` or vice versa.
Remember, `:=` is shorthand for declaration and initialization. If you just need to initialization,
use `=`.