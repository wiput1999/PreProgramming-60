# Condition Flow

## Lecture List

|Week 1|Week 2|Week 3|Week 4|Week 5|Week 6|Week 7|Week 8|Week 9|
|:-:|:-:|:-:|:-:|:-:|:-:|:-:|:-:|:-:|
|[Click](/Lecture%20Cheat%20Sheet/Week1%20-%20IO.md)|[Click](/Lecture%20Cheat%20Sheet/Week%202%20-%20Functions.md)|[Click](/Lecture%20Cheat%20Sheet/Week%203%20-%20Math%20Library.md%20)|[Click](/Lecture%20Cheat%20Sheet/Week%204%20-%20Strings.md)|[Click](/Lecture%20Cheat%20Sheet/Week%205%20-%20Condition.md%20)|[Click](/Lecture%20Cheat%20Sheet/Week%206%20-%20Loops.md)|[Click](/Lecture%20Cheat%20Sheet/Week%207%20-%20Lists%20+%20Tuples.md)|[Click](/Lecture%20Cheat%20Sheet/Week%208%20-%20Dictionary.md)|[Click](/Lecture%20Cheat%20Sheet/Week%209%20-%20Recursion.md)|

## Follow me on GitHub
|<a href="https://github.com/sagelga"><img src="https://avatars0.githubusercontent.com/u/13056824" width="100px"></a>  |
|:-:|  
|@sagelga|

Copyright by P' Kumamon IT14. <br>
For education purpose only.

![Built with love](http://forthebadge.com/images/badges/built-with-love.svg)

----------

# Introduction to condition flow

Condition flow makes the program think out of decision. Some decision is harder to make or some decision is complicate, Python have covered you.

# What makes the argument true
|1|2|3|4|5|
|:-:|:-:|:-:|:-:|:-:|
|Equation is correct|Comparison of string is identical|Integer is not 0 (can be negative or positive)|Boolean is true|Logically true|

# How to compare strings
```python
var1 = "Hello"
var2 = "Hello"

return num1 == num2 # This line will return boolean of true. Because both string is identical
```

# If statement
### If statement will run when the argument is true.
```python
How to use:
if (<argument>):
  # This set of code will run when argument is true

Example:
kumamon = 12
if (kumamon > 10):
    print("Happy kumamon")

# Returns "Happy kumamon"
```

### When If statement will not work
```python
kumamon = 9

if (kumamon > 10):
    print("Heavy kumamon")

### Returns <none> (Because the statement is now false)
```

### Indentation on if statement
```python
kumamon = 9

if (kumamon = 9):
    print("Happy")
print("Kumamon")

# Returns "Happy Kumamon"
```

### If from variables
```python
if kumamon:
    print("Happy Kumamon")

# If kumamon = 1 returns "Happy Kumamon"
# If kumamon = 10 returns "Happy Kumamon"
# If kumamon = -1 returns "Happy Kumamon"
# If kumamon = 0 returns nothing
```

# If - Else statement

### Introduction to Else statement (Requires If statement)
If the IF statement is true, the IF line will run, else the else line will run. <br>
This case, the example shows how the program input different number.
```python
if kumamon > 10:
    print("Heavy kumamon")
else:
    print("Cute kumamon")

# If kumamon = 9, it returns: "Cute kumamon"
# If kumamon = 11, it returns: "Heavy kumamon"
```

### Bound of Else to If
This case, the second if is bound to else. So, when the second if is false, it also runs the else statement.
```python
kumamon = 10
if kumamon == 10:
    print("Happy Happy kumamon")
if kumamon > 10:
    print("Heavy kumamon")
else:
    print("Cute kumamon")

Returns:
"Happy Happy kumamon"
"Cute kumamon"
```

### Else will not do when
This thing does not work at all. Else cannot be left alone without if statement.
```python
kumamon = 10
else:
    print("Happy Kumamon")

# Program will not compile because syntax error (as they have no bound to if statement)
```

# If - Elif statement
If and elif is used together to make more decision than just a plain if statement.

### Introduction to Elif
Elif is shorthanded for `else if` so it will check statement when the first if statement is false
```python
kumamon = 10:
if kumamon == 11:
    print("Happy Kumamon")
elif kumamon == 10:
    print("Not Happy Kumamon")

# Returns "Not Happy Kumamon
```

### Writing elif in longer form
```python
kumamon = 10:
if kumamon == 11:
    print("Happy Kumamon")
else:
    if kumamon == 10:
        print("Not Happy Kumamon")

# Returns "Not Happy Kumamon
```

# If - Elif - Else statement
You can pull the full power of Python by using these 3 statements

### Using all checker
```python
kumamon = 11

if kumamon == 10:
    print("Happy Happy kumamon")
elif kumamon > 10:
    print("Heavy kumamon")
else: #This condition will run when kumamon < 10
    print("Cute kumamon")

Returns:
"Heavy kumamon"
```

# Nested control flow
Do anything you like, but beware of [too many branch](https://github.com/sagelga/PreProgramming-60/blob/master/Lecture%20List/Week%20Extra%20-%20PyLint.md#11-too-many-branch)

### If Nested Flow
Try not to do this. As they are harder to debug.
```python
    if kumamon > 5:
      if kumamon > 4:
        if kumamon > 3:
          if kumamon > 2:
            if kumamon > 1:
              print("Happy Happy Kumamon 1")
            print("Happy Happy Kumamon 2")
          print("Happy Happy Kumamon 3")
        print("Happy Happy Kumamon 4")
      print("Happy Happy Kumamon 5")
```

### More nested flow
```python
    if kumamon == 10:
      print("Happy Happy kumamon")
      if kumamon == 10:
        print("Happy Happy kumamon")
        if kumamon == 10:
          print("Happy Happy kumamon")
        elif kumamon > 10:
          print("Heavy kumamon")
        else:
          print("Cute kumamon")
      elif kumamon > 10:
        print("Heavy kumamon")
      else:
        print("Cute kumamon")
    elif kumamon > 10:
      print("Heavy kumamon")
    else:
      print("Cute kumamon")
      if kumamon == 10:
        print("Happy Happy kumamon")
      elif kumamon > 10:
        print("Heavy kumamon")
      else:
        print("Cute kumamon")
```

# Switch statement
In C, Java and many other have this feature, called switch. <br>
Swith is like if - elif - else statement, but look cleaner. <br>
WARNING : This is an equivalent to other language switch statement, so use this as your warning.

### Example of Switch statement
```python
def zero():
    print("You typed zero.")

def sqr():
    print("n is a perfect square")

def even():
    print("n is an even number")

def prime():
    print("n is a prime number")

# map the inputs to the function blocks
options = {
0 : zero,
1 : sqr,
2 : even,
3 : prime,
4 : sqr,
5 : prime,
7 : prime,
9 : sqr,
}

options[number]()

# If number = 0, it returns "You typed zero."
# If number = 1, it returns "n is a perfect square"
# If number = 2, it returns "n is an even number"
# If number = 7, it returns "n is a prime number"
```
