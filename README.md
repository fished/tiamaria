# tiamaria

*Work in Progress!*

The Tia Maria programming language attempts to bring a minimalist, consistent syntax to Node without undue influence from existing programming languages.

## Goals

* Easy to read and easy to follow!  Easy to learn, easy to parse!
* There should be a one-to-one, reversible mapping to and from Javascript.
* Event cascades should be easy to read and easy to follow.

## Examples

### General syntax

Lines are delimited either by ';' or by newlines ("\n").  Carriage returns ("\r") are ignored if followed by a newline.

### Comments
Accepts all common comment styles

```
# This is a comment.
// This is too!
/* Even this! */
```

### Literals

#### Single Quoted (') Strings

A single quoted string represents a string literal, with no modification of the underlying string, no escape sequences, etc.
```
'This is a string' # This is a string
string2='string too'; 'This is a string #{string2}' # This is a string #{string2}
'This is a string with an escape sequence: \nnext line' # This is a string with an escape sequence: \nnext line
```

#### Double Quoted (") Strings

Double quotes strings are subject to some processing by the interpreter at creation time.
```
"This is a string." # This is a string.
string2='string too'; "This is a string #{string2}" # This is a string too 
"This is a string with an escape sequence: \nnext line" # This is a string with an escape sequence:
                                                        # next line
```

#### Integers
```
1 # 1
1045 # 1045
```

#### Floating point
```
1234.5 # 12345.6
```

