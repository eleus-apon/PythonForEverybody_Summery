# Programming for Everybody (Getting Started with Python)
This is the first course of this specialization.

## Chapter 1:Introductions
### Why We Program
Writing programs (or programming) is a very creative and rewarding activity. You can write programs for many reasons, ranging from making your living to solving a difficult data analysis problem to having fun to helping someone else solve a problem. This book assumes that everyone needs to know how to program, and that once you know how to program you will figure out what you want to do with your newfound skills.

### Why Python
Pyhton is one of the top 10 popular programming languages of 2017. Python is a general purpose and high level programming language. You can use Python for developing desktop GUI applications, websites and web applications. Also, Python, as a high level programming language, allows you to focus on core functionality of the application by taking care of common programming tasks. The simple syntax rules of the programming language further makes it easier for you to keep the code base readable and application maintainable. There are also a number of reasons why you should prefer Python to other programming languages.

7 Reasons Why We can Consider Writing Software Applications in Python
1. Readable and Maintainable Code
2. Multiple Programming Paradigms
3. Compatible with Major Platforms and Systems
4. Robust Standard Library
5. Many Open Source Frameworks and Tools
6. Simplify Complex Software Development
7. Adopt Test Driven Development

### Installing & Using Python
We can download and install python form [here](https://www.python.org/downloads/)!

## Chapter 2: Variables
### Values and data types
A value is one of the fundamental things — like a letter or a number — that a program manipulates. The values we have seen so far are 2 (the result when we added 1 + 1), and "Hello, World!".

These values belong to different data types: 2 is an integer, and "Hello, World!" is a string, so-called because it contains a string of letters. You (and the interpreter) can identify strings because they are enclosed in quotation marks.

The print statement also works for integers.
```
>>> print 4
4
```
If you are not sure what type a value has, the interpreter can tell you.
```
>>> type("Hello, World!")
<type 'str'>
>>> type(17)
<type 'int'>
```
Not surprisingly, strings belong to the type str and integers belong to the type int. Less obviously, numbers with a decimal point belong to a type called float, because these numbers are represented in a format called floating-point.
```
>>> type(3.2)
<type 'float'>
```
What about values like "17" and "3.2"? They look like numbers, but they are in quotation marks like strings.
```
>>> type("17")
<type 'str'>
>>> type("3.2")
<type 'str'>
```
They’re strings.

Strings in Python can be enclosed in either single quotes (‘) or double quotes (”):
```
>>> type('This is a string.')
<type 'str'>
>>> type("And so is this.")
<type 'str'>
```
Double quoted strings can contain single quotes inside them, as in "Bruce's beard", and single quoted strings can have double quotes inside them, as in 'The knights who say "Ni!"'.

When you type a large integer, you might be tempted to use commas between groups of three digits, as in 1,000,000. This is not a legal integer in Python, but it is legal:
```
>>> print 1,000,000
1 0 0
```
Well, that’s not what we expected at all! Python interprets 1,000,000 as a list of three items to be printed. So remember not to put commas in your integers.

### Variables
One of the most powerful features of a programming language is the ability to manipulate variables. A variable is a name that refers to a value.

The assignment statement creates new variables and gives them values:
```
>>> message = "What's up, Doc?"
>>> n = 17
>>> pi = 3.14159
```
This example makes three assignments. The first assigns the string "What's up, Doc?" to a new variable named message. The second gives the integer 17 to n, and the third gives the floating-point number 3.14159 to pi.

The assignment operator, =, should not be confused with an equals sign (even though it uses the same character). Assignment operators link a name, on the left hand side of the operator, with a value, on the right hand side. This is why you will get an error if you enter:
```
>>> 17 = n
```
A common way to represent variables on paper is to write the name with an arrow pointing to the variable’s value. This kind of figure is called a state diagram because it shows what state each of the variables is in (think of it as the variable’s state of mind). This diagram shows the result of the assignment statements:

State diagram
The print statement also works with variables.
```
>>> print message
What's up, Doc?
>>> print n
17
>>> print pi
3.14159
```
In each case the result is the value of the variable. Variables also have types; again, we can ask the interpreter what they are.
```
>>> type(message)
<type 'str'>
>>> type(n)
<type 'int'>
>>> type(pi)
<type 'float'>
```
The type of a variable is the type of the value it refers to.

### Variable name & Keywords
Programmers generally choose names for their variables that are meaningful — they document what the variable is used for.

Variable names can be arbitrarily long. They can contain both letters and numbers, but they have to begin with a letter. Although it is legal to use uppercase letters, by convention we don’t. If you do, remember that case matters. `Bruce` and `bruce` are different variables.

The underscore character (_) can appear in a name. It is often used in names with multiple words, such as `my_name` or `price_of_tea_in_china`.

If you give a variable an illegal name, you get a syntax error:
```
>>> 76trombones = "big parade"
SyntaxError: invalid syntax
>>> more$ = 1000000
SyntaxError: invalid syntax
>>> class = "Computer Science 101"
SyntaxError: invalid syntax
```
`76trombones` is illegal because it does not begin with a letter. more$ is illegal because it contains an illegal character, the dollar sign. But what’s wrong with class?

It turns out that class is one of the Python **keywords**. Keywords define the language’s rules and structure, and they cannot be used as variable names.

Python has thirty-one keywords:
|         |       |        |        |        |          |
|---------|-------|--------|--------|--------|----------|
| and     | as    | assert | break  | class  | continue |
| def     | del   | elif   | else   | except | exec     |
| finally | for   | from   | global | if     | import   |
| in      | is    | lambda | not    | or     | pass     |
| print   | raise | return | try    | while  | with     |
| yield   |       |        |        |        |          |

### Statements
A statement is an instruction that the Python interpreter can execute. We have seen two kinds of statements: print and assignment.

When you type a statement on the command line, Python executes it and displays the result, if there is one. The result of a print statement is a value. Assignment statements don’t produce a result.

A script usually contains a sequence of statements. If there is more than one statement, the results appear one at a time as the statements execute.

For example, the script
```
print 1
x = 2
print x
```
produces the output:
```
1
2
```
Again, the assignment statement produces no output.

### Evaluating Expressiopns
An expression is a combination of values, variables, and operators. If you type an expression on the command line, the interpreter evaluates it and displays the result:
```
>>> 1 + 1
2
```
The evaluation of an expression produces a value, which is why expressions can appear on the right hand side of assignment statements. A value all by itself is a simple expression, and so is a variable.
```
>>> 17
17
>>> x
2
```
Confusingly, evaluating an expression is not quite the same thing as printing a value.
```
>>> message = "What's up, Doc?"
>>> message
"What's up, Doc?"
>>> print message
What's up, Doc?
```
When the Python shell displays the value of an expression, it uses the same format you would use to enter a value. In the case of strings, that means that it includes the quotation marks. But the print statement prints the value of the expression, which in this case is the contents of the string.

In a script, an expression all by itself is a legal statement, but it doesn’t do anything. The script
```
17
3.2
"Hello, World!"
1 + 1
```
produces no output at all. How would you change the script to display the values of these four expressions?

### Operators and operands
Operators are special symbols that represent computations like addition and multiplication. The values the operator uses are called operands.

The following are all legal Python expressions whose meaning is more or less clear:

```20+32   hour-1   hour*60+minute   minute/60   5**2   (5+9)*(15-7)```
The symbols +, -, and /, and the use of parenthesis for grouping, mean in Python what they mean in mathematics. The asterisk (*) is the symbol for multiplication, and ** is the symbol for exponentiation.

When a variable name appears in the place of an operand, it is replaced with its value before the operation is performed.

Addition, subtraction, multiplication, and exponentiation all do what you expect, but you might be surprised by division. The following operation has an unexpected result:
```
>>> minute = 59
>>> minute/60
0
```
The value of minute is 59, and 59 divided by 60 is 0.98333, not 0. The reason for the discrepancy is that Python is performing integer division.

When both of the operands are integers, the result must also be an integer, and by convention, integer division always rounds down, even in cases like this where the next integer is very close.

A possible solution to this problem is to calculate a percentage rather than a fraction:
```
>>> minute*100/60
98
```
Again the result is rounded down, but at least now the answer is approximately correct. Another alternative is to use floating-point division. We’ll see in the chapter 4 how to convert integer values and variables to floating-point values.

### Order of Operations
Order of operations
When more than one operator appears in an expression, the order of evaluation depends on the rules of precedence. Python follows the same precedence rules for its mathematical operators that mathematics does. The acronym PEMDAS is a useful way to remember the order of operations:

1. Parentheses have the highest precedence and can be used to force an expression to evaluate in the order you want. Since expressions in parentheses are evaluated first, 2 * (3-1) is 4, and (1+1)**(5-2) is 8. You can also use parentheses to make an expression easier to read, as in (minute * 100) / 60, even though it doesn’t change the result.
2. Exponentiation has the next highest precedence, so 2**1+1 is 3 and not 4, and 3*1**3 is 3 and not 27.
3. Multiplication and Division have the same precedence, which is higher than Addition and Subtraction, which also have the same precedence. So 2*3-1 yields 5 rather than 4, and 2/3-1 is -1, not 1 (remember that in integer division, 2/3=0).
3. Operators with the same precedence are evaluated from left to right. So in the expression minute*100/60, the multiplication happens first, yielding 5900/60, which in turn yields 98. If the operations had been evaluated from right to left, the result would have been 59*1, which is 59, which is wrong.

### Operations on strings
In general, you cannot perform mathematical operations on strings, even if the strings look like numbers. The following are illegal (assuming that message has type string):
```
message-1   "Hello"/123   message*"Hello"   "15"+2
```
Interestingly, the + operator does work with strings, although it does not do exactly what you might expect. For strings, the + operator represents concatenation, which means joining the two operands by linking them end-to-end. For example:
```
fruit = "banana"
baked_good = " nut bread"
print fruit + baked_good
```
The output of this program is banana nut bread. The space before the word nut is part of the string, and is necessary to produce the space between the concatenated strings.
The * operator also works on strings; it performs repetition. For example, 'Fun'*3 is 'FunFunFun'. One of the operands has to be a string; the other has to be an integer.
On one hand, this interpretation of + and * makes sense by analogy with addition and multiplication. Just as 4*3 is equivalent to 4+4+4, we expect "Fun"*3 to be the same as "Fun"+"Fun"+"Fun", and it is. On the other hand, there is a significant way in which string concatenation and repetition are different from integer addition and multiplication. Can you think of a property that addition and multiplication have that string concatenation and repetition do not?

### Input
There are two built-in functions in Python for getting keyboard input:
```
n = raw_input("Please enter your name: ")
print n
n = input("Enter a numerical expression: ")
print n
```
A sample run of this script would look something like this:
```
$ python tryinput.py
Please enter your name: Arthur, King of the Britons
Arthur, King of the Britons
Enter a numerical expression: 7 * 3
21
```
Each of these functions allows a prompt to be given to the function between the parentheses.

### Composition
So far, we have looked at the elements of a program — variables, expressions, and statements — in isolation, without talking about how to combine them.

One of the most useful features of programming languages is their ability to take small building blocks and compose them. For example, we know how to add numbers and we know how to print; it turns out we can do both at the same time:
```
>>>  print 17 + 3
20
```
In reality, the addition has to happen before the printing, so the actions aren’t actually happening at the same time. The point is that any expression involving numbers, strings, and variables can be used inside a print statement. You’ve already seen an example of this:
```
print "Number of minutes since midnight: ", hour*60+minute
```
You can also put arbitrary expressions on the right-hand side of an assignment statement:
```
percentage = (minute * 100) / 60
```
This ability may not seem impressive now, but you will see other examples where composition makes it possible to express complex computations neatly and concisely.

Warning: There are limits on where you can use certain expressions. For example, the left-hand side of an assignment statement has to be a variable name, not an expression. So, the following is illegal: minute+1 = hour.

### Comments
As programs get bigger and more complicated, they get more difficult to read. Formal languages are dense, and it is often difficult to look at a piece of code and figure out what it is doing, or why.

For this reason, it is a good idea to add notes to your programs to explain in natural language what the program is doing. These notes are called comments, and they are marked with the # symbol:
```
# compute the percentage of the hour that has elapsed
percentage = (minute * 100) / 60
```
In this case, the comment appears on a line by itself. You can also put comments at the end of a line:
```
percentage = (minute * 100) / 60     # caution: integer division
```
Everything from the # to the end of the line is ignored — it has no effect on the program. The message is intended for the programmer or for future programmers who might use this code. In this case, it reminds the reader about the ever-surprising behavior of integer division.


## Chapter 3: Conditional Code
### Boolean expressions
A boolean expression is an expression that is either true or false. The following examples use the operator ==, which compares two operands and produces True if they are equal and False otherwise:
```
>>> 5 == 5
>>> 5 == 6
True
False
```
True and False are special values that belong to the class bool; they are not strings:
```
>>> type(True)
<class 'bool'>
>>> type(False)
<class 'bool'>
```
The == operator is one of the comparison operators; the others are:
```
      x != y               # x is not equal to y
      x > y                # x is greater than y
      x < y                # x is less than y
      x >= y               # x is greater than or equal to y
      x <= y               # x is less than or equal to y
      x is y               # x is the same as y
      x is not y           # x is not the same as y      
```
Although these operations are probably familiar to you, the Python symbols are different from the mathematical symbols for the same operations. A common error is to use a single equal sign (=) instead of a double equal sign (==). Remember that = is an assignment operator and == is a comparison operator. There is no such thing as =< or =>.

### Logical operators
There are three logical operators: and, or, and not. The semantics (meaning) of these operators is similar to their meaning in English. For example,
```
x > 0 and x < 10
```
is true only if x is greater than 0 and less than 10.

### Conditional execution
In order to write useful programs, we almost always need the ability to check conditions and change the behavior of the program accordingly. Conditional statements give us this ability. The simplest form is the if statement:
```
if x > 0 :
    print('x is positive')
```
The boolean expression after the if statement is called the condition. We end the if statement with a colon character (:) and the line(s) after the if statement are indented.

### Alternative execution
A second form of the if statement is alternative execution, in which there are two possibilities and the condition determines which one gets executed. The syntax looks like this:
```
if x%2 == 0 :
    print('x is even')
else :
    print('x is odd')
```
If the remainder when x is divided by 2 is 0, then we know that x is even, and the program displays a message to that effect. If the condition is false, the second set of statements is executed.

### Chained conditionals
Sometimes there are more than two possibilities and we need more than two branches. One way to express a computation like that is a chained conditional:
```
if x < y:
    print('x is less than y')
elif x > y:
    print('x is greater than y')
else:
    print('x and y are equal')
```
elif is an abbreviation of "else if." Again, exactly one branch will be executed. There is no limit on the number of elif statements. If there is an else clause, it has to be at the end, but there doesn't have to be one.

### Nested conditionals
One conditional can also be nested within another. We could have written the three-branch example like this:
```
if x == y:
    print('x and y are equal')
else:
    if x < y:
        print('x is less than y')
    else:
        print('x is greater than y')
```
The outer conditional contains two branches. The first branch contains a simple statement. The second branch contains another if statement, which has two branches of its own. Those two branches are both simple statements, although they could have been conditional statements as well.
Although the indentation of the statements makes the structure apparent, nested conditionals become difficult to read very quickly. In general, it is a good idea to avoid them when you can.

Logical operators often provide a way to simplify nested conditional statements. For example, we can rewrite the following code using a single conditional:
```
if 0 < x:
    if x < 10:
        print('x is a positive single-digit number.')
```
The print statement is executed only if we make it past both conditionals, so we can get the same effect with the and operator:
```
if 0 < x and x < 10:
    print('x is a positive single-digit number.')
```
### Catching exceptions using try and except
Earlier we saw a code segment where we used the input and int functions to read and parse an integer number entered by the user. We also saw how treacherous doing this could be:
```
>>> prompt = "What...is the airspeed velocity of an unladen swallow?\n"
>>> speed = input(prompt)
What...is the airspeed velocity of an unladen swallow?
What do you mean, an African or a European swallow?
>>> int(speed)
ValueError: invalid literal for int() with base 10:
>>>
```
When we are executing these statements in the Python interpreter, we get a new prompt from the interpreter, think "oops", and move on to our next statement.

However if you place this code in a Python script and this error occurs, your script immediately stops in its tracks with a traceback. It does not execute the following statement.

Here is a sample program to convert a Fahrenheit temperature to a Celsius temperature:
```
inp = input('Enter Fahrenheit Temperature: ')
fahr = float(inp)
cel = (fahr - 32.0) * 5.0 / 9.0
print(cel)
```
If we execute this code and give it invalid input, it simply fails with an unfriendly error message:
```
python fahren.py
Enter Fahrenheit Temperature:72
22.22222222222222
```
```
python fahren.py
Enter Fahrenheit Temperature:fred
Traceback (most recent call last):
  File "fahren.py", line 2, in <module>
    fahr = float(inp)
ValueError: could not convert string to float: 'fred'
```
There is a conditional execution structure built into Python to handle these types of expected and unexpected errors called "try / except". The idea of try and except is that you know that some sequence of instruction(s) may have a problem and you want to add some statements to be executed if an error occurs. These extra statements (the except block) are ignored if there is no error.

You can think of the try and except feature in Python as an "insurance policy" on a sequence of statements.

We can rewrite our temperature converter as follows:
```
inp = input('Enter Fahrenheit Temperature:')
try:
    fahr = float(inp)
    cel = (fahr - 32.0) * 5.0 / 9.0
    print(cel)
except:
    print('Please enter a number')
```
Python starts by executing the sequence of statements in the try block. If all goes well, it skips the except block and proceeds. If an exception occurs in the try block, Python jumps out of the try block and executes the sequence of statements in the except block.
```
python fahren2.py
Enter Fahrenheit Temperature:72
22.22222222222222
```
```
python fahren2.py
Enter Fahrenheit Temperature:fred
Please enter a number
```
Handling an exception with a try statement is called catching an exception. In this example, the except clause prints an error message. In general, catching an exception gives you a chance to fix the problem, or try again, or at least end the program gracefully.

### Short-circuit evaluation of logical expressions
When Python is processing a logical expression such as x >= 2 and (x/y) > 2, it evaluates the expression from left to right. Because of the definition of and, if x is less than 2, the expression x >= 2 is False and so the whole expression is False regardless of whether (x/y) > 2 evaluates to True or False.

When Python detects that there is nothing to be gained by evaluating the rest of a logical expression, it stops its evaluation and does not do the computations in the rest of the logical expression. When the evaluation of a logical expression stops because the overall value is already known, it is called short-circuiting the evaluation.

While this may seem like a fine point, the short-circuit behavior leads to a clever technique called the guardian pattern. Consider the following code sequence in the Python interpreter:
```
>>> x = 6
>>> y = 2
>>> x >= 2 and (x/y) > 2
True
>>> x = 1
>>> y = 0
>>> x >= 2 and (x/y) > 2
False
>>> x = 6
>>> y = 0
>>> x >= 2 and (x/y) > 2
Traceback (most recent call last):
  File "<stdin>", line 1, in <module>
ZeroDivisionError: division by zero
>>>
```
The third calculation failed because Python was evaluating (x/y) and y was zero, which causes a runtime error. But the second example did not fail because the first part of the expression x >= 2 evaluated to False so the (x/y) was not ever executed due to the short-circuit rule and there was no error.

We can construct the logical expression to strategically place a guard evaluation just before the evaluation that might cause an error as follows:
```
>>> x = 1
>>> y = 0
>>> x >= 2 and y != 0 and (x/y) > 2
False
>>> x = 6
>>> y = 0
>>> x >= 2 and y != 0 and (x/y) > 2
False
>>> x >= 2 and (x/y) > 2 and y != 0
Traceback (most recent call last):
  File "<stdin>", line 1, in <module>
ZeroDivisionError: division by zero
>>>
```
In the first logical expression, x >= 2 is False so the evaluation stops at the and. In the second logical expression, x >= 2 is True but y != 0 is False so we never reach (x/y).

In the third logical expression, the y != 0 is after the (x/y) calculation so the expression fails with an error.

In the second expression, we say that y != 0 acts as a guard to insure that we only execute (x/y) if y is non-zero.

## Chapter 4:Functions
### Function calls
In the context of programming, a function is a named sequence of statements that performs a computation. When you define a function, you specify the name and the sequence of statements. Later, you can "call" the function by name. We have already seen one example of a function call:
```
>>> type(32)
<class 'int'>
```
The name of the function is type. The expression in parentheses is called the argument of the function. The argument is a value or variable that we are passing into the function as input to the function. The result, for the type function, is the type of the argument.

It is common to say that a function "takes" an argument and "returns" a result. The result is called the return value.

### Built-in functions
Python provides a number of important built-in functions that we can use without needing to provide the function definition. The creators of Python wrote a set of functions to solve common problems and included them in Python for us to use.

The max and min functions give us the largest and smallest values in a list, respectively:
```
>>> max('Hello world')
'w'
>>> min('Hello world')
' '
>>>
```
The max function tells us the "largest character" in the string (which turns out to be the letter "w") and the min function shows us the smallest character (which turns out to be a space).

Another very common built-in function is the len function which tells us how many items are in its argument. If the argument to len is a string, it returns the number of characters in the string.
```
>>> len('Hello world')
11
>>>
```
These functions are not limited to looking at strings. They can operate on any set of values, as we will see in later chapters.

You should treat the names of built-in functions as reserved words (i.e., avoid using "max" as a variable name).

### Type conversion functions
Python also provides built-in functions that convert values from one type to another. The int function takes any value and converts it to an integer, if it can, or complains otherwise:
```
>>> int('32')
32
>>> int('Hello')
```
ValueError: invalid literal for int() with base 10: 'Hello'
int can convert floating-point values to integers, but it doesn't round off; it chops off the fraction part:
```
>>> int(3.99999)
3
>>> int(-2.3)
-2
```
float converts integers and strings to floating-point numbers:
```
>>> float(32)
32.0
>>> float('3.14159')
3.14159
```
Finally, str converts its argument to a string:
```
>>> str(32)
'32'
>>> str(3.14159)
'3.14159'
```
### Random numbers
Given the same inputs, most computer programs generate the same outputs every time, so they are said to be deterministic. Determinism is usually a good thing, since we expect the same calculation to yield the same result. For some applications, though, we want the computer to be unpredictable. Games are an obvious example, but there are more.

Making a program truly nondeterministic turns out to be not so easy, but there are ways to make it at least seem nondeterministic. One of them is to use algorithms that generate pseudorandom numbers. Pseudorandom numbers are not truly random because they are generated by a deterministic computation, but just by looking at the numbers it is all but impossible to distinguish them from random.

The random module provides functions that generate pseudorandom numbers (which I will simply call "random" from here on).

The function random returns a random float between 0.0 and 1.0 (including 0.0 but not 1.0). Each time you call random, you get the next number in a long series. To see a sample, run this loop:
```
import random

for i in range(10):
    x = random.random()
    print(x)
```
This program produces the following list of 10 random numbers between 0.0 and up to but not including 1.0.
```
0.11132867921152356
0.5950949227890241
0.04820265884996877
0.841003109276478
0.997914947094958
0.04842330803368111
0.7416295948208405
0.510535245390327
0.27447040171978143
0.028511805472785867
```

### Math functions
Python has a math module that provides most of the familiar mathematical functions. Before we can use the module, we have to import it:
```
>>> import math
```
This statement creates a module object named math. If you print the module object, you get some information about it:
```
>>> print(math)
<module 'math' (built-in)>
```
The module object contains the functions and variables defined in the module. To access one of the functions, you have to specify the name of the module and the name of the function, separated by a dot (also known as a period). This format is called dot notation.
```
>>> ratio = signal_power / noise_power
>>> decibels = 10 * math.log10(ratio)

>>> radians = 0.7
>>> height = math.sin(radians)
```
The first example computes the logarithm base 10 of the signal-to-noise ratio. The math module also provides a function called log that computes logarithms base e.

The second example finds the sine of radians. The name of the variable is a hint that sin and the other trigonometric functions (cos, tan, etc.) take arguments in radians. To convert from degrees to radians, divide by 360 and multiply by 2π:
```
>>> degrees = 45
>>> radians = degrees / 360.0 * 2 * math.pi
>>> math.sin(radians)
0.7071067811865476
```
The expression math.pi gets the variable pi from the math module. The value of this variable is an approximation of π, accurate to about 15 digits.

If you know your trigonometry, you can check the previous result by comparing it to the square root of two divided by two:
```
>>> math.sqrt(2) / 2.0
0.7071067811865476
```
### Adding new functions
So far, we have only been using the functions that come with Python, but it is also possible to add new functions. A function definition specifies the name of a new function and the sequence of statements that execute when the function is called. Once we define a function, we can reuse the function over and over throughout our program.

Here is an example:
```
def print_lyrics():
    print("I'm a lumberjack, and I'm okay.")
    print('I sleep all night and I work all day.')
```
def is a keyword that indicates that this is a function definition. The name of the function is print_lyrics. The rules for function names are the same as for variable names: letters, numbers and some punctuation marks are legal, but the first character can't be a number. You can't use a keyword as the name of a function, and you should avoid having a variable and a function with the same name.

The empty parentheses after the name indicate that this function doesn't take any arguments. Later we will build functions that take arguments as their inputs.

The first line of the function definition is called the header; the rest is called the body. The header has to end with a colon and the body has to be indented. By convention, the indentation is always four spaces. The body can contain any number of statements.

The strings in the print statements are enclosed in quotes. Single quotes and double quotes do the same thing; most people use single quotes except in cases like this where a single quote (which is also an apostrophe) appears in the string.

If you type a function definition in interactive mode, the interpreter prints ellipses (...) to let you know that the definition isn't complete:
```
>>> def print_lyrics():
...     print("I'm a lumberjack, and I'm okay.")
...     print('I sleep all night and I work all day.')
...
```
To end the function, you have to enter an empty line (this is not necessary in a script).

Defining a function creates a variable with the same name.
```
>>> print(print_lyrics)
<function print_lyrics at 0xb7e99e9c>
>>> print(type(print_lyrics))
<class 'function'>
```
The value of print_lyrics is a function object, which has type "function".

The syntax for calling the new function is the same as for built-in functions:
```
>>> print_lyrics()
I'm a lumberjack, and I'm okay.
I sleep all night and I work all day.
```
Once you have defined a function, you can use it inside another function. For example, to repeat the previous refrain, we could write a function called repeat_lyrics:
```
def repeat_lyrics():
    print_lyrics()
    print_lyrics()
```
And then call repeat_lyrics:
```
>>> repeat_lyrics()
I'm a lumberjack, and I'm okay.
I sleep all night and I work all day.
I'm a lumberjack, and I'm okay.
I sleep all night and I work all day.
```
But that's not really how the song goes.

### Definitions and uses
Pulling together the code fragments from the previous section, the whole program looks like this:
```
def print_lyrics():
    print("I'm a lumberjack, and I'm okay.")
    print('I sleep all night and I work all day.')


def repeat_lyrics():
    print_lyrics()
    print_lyrics()

repeat_lyrics()
```
This program contains two function definitions: print_lyrics and repeat_lyrics. Function definitions get executed just like other statements, but the effect is to create function objects. The statements inside the function do not get executed until the function is called, and the function definition generates no output.

### Flow of execution
In order to ensure that a function is defined before its first use, you have to know the order in which statements are executed, which is called the flow of execution.

Execution always begins at the first statement of the program. Statements are executed one at a time, in order from top to bottom.

Function definitions do not alter the flow of execution of the program, but remember that statements inside the function are not executed until the function is called.

A function call is like a detour in the flow of execution. Instead of going to the next statement, the flow jumps to the body of the function, executes all the statements there, and then comes back to pick up where it left off.

That sounds simple enough, until you remember that one function can call another. While in the middle of one function, the program might have to execute the statements in another function. But while executing that new function, the program might have to execute yet another function!

Fortunately, Python is good at keeping track of where it is, so each time a function completes, the program picks up where it left off in the function that called it. When it gets to the end of the program, it terminates.

What's the moral of this sordid tale? When you read a program, you don't always want to read from top to bottom. Sometimes it makes more sense if you follow the flow of execution.

### Parameters and arguments
Some of the built-in functions we have seen require arguments. For example, when you call math.sin you pass a number as an argument. Some functions take more than one argument: math.pow takes two, the base and the exponent.

Inside the function, the arguments are assigned to variables called parameters. Here is an example of a user-defined function that takes an argument:
```
def print_twice(bruce):
    print(bruce)
    print(bruce)
```
This function assigns the argument to a parameter named bruce. When the function is called, it prints the value of the parameter (whatever it is) twice.

This function works with any value that can be printed.
```
>>> print_twice('Spam')
Spam
Spam
>>> print_twice(17)
17
17
>>> import math
>>> print_twice(math.pi)
3.141592653589793
3.141592653589793
```
The same rules of composition that apply to built-in functions also apply to user-defined functions, so we can use any kind of expression as an argument for print_twice:
```
>>> print_twice('Spam '*4)
Spam Spam Spam Spam
Spam Spam Spam Spam
>>> print_twice(math.cos(math.pi))
-1.0
-1.0
```
The argument is evaluated before the function is called, so in the examples the expressions "Spam '*4andmath.cos(math.pi)` are only evaluated once.
You can also use a variable as an argument:
```
>>> michael = 'Eric, the half a bee.'
>>> print_twice(michael)
Eric, the half a bee.
Eric, the half a bee.
```
The name of the variable we pass as an argument (michael) has nothing to do with the name of the parameter (bruce). It doesn't matter what the value was called back home (in the caller); here in print_twice, we call everybody bruce.

### Fruitful functions and void functions
Some of the functions we are using, such as the math functions, yield results; for lack of a better name, I call them fruitful functions. Other functions, like print_twice, perform an action but don't return a value. They are called void functions.

When you call a fruitful function, you almost always want to do something with the result; for example, you might assign it to a variable or use it as part of an expression:
```
x = math.cos(radians)
golden = (math.sqrt(5) + 1) / 2
```
When you call a function in interactive mode, Python displays the result:
```
>>> math.sqrt(5)
2.23606797749979
```
But in a script, if you call a fruitful function and do not store the result of the function in a variable, the return value vanishes into the mist!
```
math.sqrt(5)
```
This script computes the square root of 5, but since it doesn't store the result in a variable or display the result, it is not very useful.

Void functions might display something on the screen or have some other effect, but they don't have a return value. If you try to assign the result to a variable, you get a special value called None.
```
>>> result = print_twice('Bing')
Bing
Bing
>>> print(result)
None
```
The value None is not the same as the string "None". It is a special value that has its own type:
```
>>> print(type(None))
<class 'NoneType'>
```
To return a result from a function, we use the return statement in our function. For example, we could make a very simple function called addtwo that adds two numbers together and returns a result.
```
def addtwo(a, b):
    added = a + b
    return added

x = addtwo(3, 5)
print(x)
```
When this script executes, the print statement will print out "8" because the addtwo function was called with 3 and 5 as arguments. Within the function, the parameters a and b were 3 and 5 respectively. The function computed the sum of the two numbers and placed it in the local function variable named added. Then it used the return statement to send the computed value back to the calling code as the function result, which was assigned to the variable x and printed out.

### Why functions?
It may not be clear why it is worth the trouble to divide a program into functions. There are several reasons:

Creating a new function gives you an opportunity to name a group of statements, which makes your program easier to read, understand, and debug.

Functions can make a program smaller by eliminating repetitive code. Later, if you make a change, you only have to make it in one place.

Dividing a long program into functions allows you to debug the parts one at a time and then assemble them into a working whole.

Well-designed functions are often useful for many programs. Once you write and debug one, you can reuse it.

Throughout the rest of the book, often we will use a function definition to explain a concept. Part of the skill of creating and using functions is to have a function properly capture an idea such as "find the smallest value in a list of values". Later we will show you code that finds the smallest in a list of values and we will present it to you as a function named min which takes a list of values as its argument and returns the smallest value in the list.


## Chapter 5: Iterations & Loops
## Updating variables
A common pattern in assignment statements is an assignment statement that updates a variable, where the new value of the variable depends on the old.
```
x = x + 1
```
This means "get the current value of x, add 1, and then update x with the new value."

If you try to update a variable that doesn't exist, you get an error, because Python evaluates the right side before it assigns a value to x:
```
>>> x = x + 1
```
NameError: name 'x' is not defined
Before you can update a variable, you have to initialize it, usually with a simple assignment:
```
>>> x = 0
>>> x = x + 1
```
Updating a variable by adding 1 is called an increment; subtracting 1 is called a decrement.

### The while statement
Computers are often used to automate repetitive tasks. Repeating identical or similar tasks without making errors is something that computers do well and people do poorly. Because iteration is so common, Python provides several language features to make it easier.

One form of iteration in Python is the while statement. Here is a simple program that counts down from five and then says "Blastoff!".
```
n = 5
while n > 0:
    print(n)
    n = n - 1
print('Blastoff!')
```
You can almost read the while statement as if it were English. It means, "While n is greater than 0, display the value of n and then reduce the value of n by 1. When you get to 0, exit the while statement and display the word Blastoff!"

More formally, here is the flow of execution for a while statement:

Evaluate the condition, yielding True or False.

If the condition is false, exit the while statement and continue execution at the next statement.

If the condition is true, execute the body and then go back to step 1.

This type of flow is called a loop because the third step loops back around to the top. We call each time we execute the body of the loop an iteration. For the above loop, we would say, "It had five iterations", which means that the body of the loop was executed five times.

The body of the loop should change the value of one or more variables so that eventually the condition becomes false and the loop terminates. We call the variable that changes each time the loop executes and controls when the loop finishes the iteration variable. If there is no iteration variable, the loop will repeat forever, resulting in an infinite loop.

### Infinite loops
An endless source of amusement for programmers is the observation that the directions on shampoo, "Lather, rinse, repeat," are an infinite loop because there is no iteration variable telling you how many times to execute the loop.

In the case of countdown, we can prove that the loop terminates because we know that the value of n is finite, and we can see that the value of n gets smaller each time through the loop, so eventually we have to get to 0. Other times a loop is obviously infinite because it has no iteration variable at all.

### "Infinite loops" and break
Sometimes you don't know it's time to end a loop until you get half way through the body. In that case you can write an infinite loop on purpose and then use the break statement to jump out of the loop.

This loop is obviously an infinite loop because the logical expression on the while statement is simply the logical constant True:
```
n = 10
while True:
    print(n, end=' ')
    n = n - 1
print('Done!')
```
If you make the mistake and run this code, you will learn quickly how to stop a runaway Python process on your system or find where the power-off button is on your computer. This program will run forever or until your battery runs out because the logical expression at the top of the loop is always true by virtue of the fact that the expression is the constant value True.

While this is a dysfunctional infinite loop, we can still use this pattern to build useful loops as long as we carefully add code to the body of the loop to explicitly exit the loop using break when we have reached the exit condition.

For example, suppose you want to take input from the user until they type done. You could write:
```
while True:
    line = input('> ')
    if line == 'done':
        break
    print(line)
print('Done!')
```
Each time through, it prompts the user with an angle bracket. If the user types done, the break statement exits the loop. Otherwise the program echoes whatever the user types and goes back to the top of the loop.
This way of writing while loops is common because you can check the condition anywhere in the loop (not just at the top) and you can express the stop condition affirmatively ("stop when this happens") rather than negatively ("keep going until that happens.").

### Finishing iterations with continue
Sometimes you are in an iteration of a loop and want to finish the current iteration and immediately jump to the next iteration. In that case you can use the continue statement to skip to the next iteration without finishing the body of the loop for the current iteration.

Here is an example of a loop that copies its input until the user types "done", but treats lines that start with the hash character as lines not to be printed (kind of like Python comments).
```
while True:
    line = input('> ')
    if line[0] == '#':
        continue
    if line == 'done':
        break
    print(line)
print('Done!')
```
Here is a sample run of this new program with continue added.
```
> hello there
hello there
> # don't print this
> print this!
print this!
> done
Done!
```
All the lines are printed except the one that starts with the hash sign because when the continue is executed, it ends the current iteration and jumps back to the while statement to start the next iteration, thus skipping the print statement.

### Definite loops using 'for'
Sometimes we want to loop through a set of things such as a list of words, the lines in a file, or a list of numbers. When we have a list of things to loop through, we can construct a definite loop using a for statement. We call the while statement an indefinite loop because it simply loops until some condition becomes False, whereas the for loop is looping through a known set of items so it runs through as many iterations as there are items in the set.

The syntax of a for loop is similar to the while loop in that there is a for statement and a loop body:
```
friends = ['Joseph', 'Glenn', 'Sally']
for friend in friends:
    print('Happy New Year:', friend)
print('Done!')
```
In Python terms, the variable friends is a list1 of three strings and the for loop goes through the list and executes the body once for each of the three strings in the list resulting in this output:
```
Happy New Year: Joseph
Happy New Year: Glenn
Happy New Year: Sally
Done!
```
Translating this for loop to English is not as direct as the while, but if you think of friends as a set, it goes like this: "Run the statements in the body of the for loop once for each friend in the set named friends."

Looking at the for loop, for and in are reserved Python keywords, and friend and friends are variables.
```
for friend in friends:
    print('Happy New Year:', friend)
```
In particular, friend is the iteration variable for the for loop. The variable friend changes for each iteration of the loop and controls when the for loop completes. The iteration variable steps successively through the three strings stored in the friends variable.

### Loop patterns
Often we use a for or while loop to go through a list of items or the contents of a file and we are looking for something such as the largest or smallest value of the data we scan through.
These loops are generally constructed by:
> Initializing one or more variables before the loop starts
> Performing some computation on each item in the loop body, possibly changing the variables in the body of the loop
> Looking at the resulting variables when the loop completes

We will use a list of numbers to demonstrate the concepts and construction of these loop patterns.

#### Counting and summing loops
For example, to count the number of items in a list, we would write the following for loop:
```
count = 0
for itervar in [3, 41, 12, 9, 74, 15]:
    count = count + 1
print('Count: ', count)
```
We set the variable count to zero before the loop starts, then we write a for loop to run through the list of numbers. Our iteration variable is named itervar and while we do not use itervar in the loop, it does control the loop and cause the loop body to be executed once for each of the values in the list.

In the body of the loop, we add 1 to the current value of count for each of the values in the list. While the loop is executing, the value of count is the number of values we have seen "so far".

Once the loop completes, the value of count is the total number of items. The total number "falls in our lap" at the end of the loop. We construct the loop so that we have what we want when the loop finishes.

Another similar loop that computes the total of a set of numbers is as follows:
```
total = 0
for itervar in [3, 41, 12, 9, 74, 15]:
    total = total + itervar
print('Total: ', total)
```
In this loop we do use the iteration variable. Instead of simply adding one to the count as in the previous loop, we add the actual number (3, 41, 12, etc.) to the running total during each loop iteration. If you think about the variable total, it contains the "running total of the values so far". So before the loop starts total is zero because we have not yet seen any values, during the loop total is the running total, and at the end of the loop total is the overall total of all the values in the list.
As the loop executes, total accumulates the sum of the elements; a variable used this way is sometimes called an accumulator.
Neither the counting loop nor the summing loop are particularly useful in practice because there are built-in functions len() and sum() that compute the number of items in a list and the total of the items in the list respectively.

#### Maximum and minimum loops
To find the largest value in a list or sequence, we construct the following loop:
```
largest = None
print('Before:', largest)
for itervar in [3, 41, 12, 9, 74, 15]:
    if largest is None or itervar > largest :
        largest = itervar
    print('Loop:', itervar, largest)
print('Largest:', largest)
```
When the program executes, the output is as follows:
```
Before: None
Loop: 3 3
Loop: 41 41
Loop: 12 41
Loop: 9 41
Loop: 74 74
Loop: 15 74
Largest: 74
```
The variable largest is best thought of as the "largest value we have seen so far". Before the loop, we set largest to the constant None. None is a special constant value which we can store in a variable to mark the variable as "empty".

Before the loop starts, the largest value we have seen so far is None since we have not yet seen any values. While the loop is executing, if largest is None then we take the first value we see as the largest so far. You can see in the first iteration when the value of itervar is 3, since largest is None, we immediately set largest to be 3.

After the first iteration, largest is no longer None, so the second part of the compound logical expression that checks itervar > largest triggers only when we see a value that is larger than the "largest so far". When we see a new "even larger" value we take that new value for largest. You can see in the program output that largest progresses from 3 to 41 to 74.

At the end of the loop, we have scanned all of the values and the variable largest now does contain the largest value in the list.

To compute the smallest number, the code is very similar with one small change:
```
smallest = None
print('Before:', smallest)
for itervar in [3, 41, 12, 9, 74, 15]:
    if smallest is None or itervar < smallest:
        smallest = itervar
    print('Loop:', itervar, smallest)
print('Smallest:', smallest)
```
Again, smallest is the "smallest so far" before, during, and after the loop executes. When the loop has completed, smallest contains the minimum value in the list.

Again as in counting and summing, the built-in functions max() and min() make writing these exact loops unnecessary.

The following is a simple version of the Python built-in min() function:
```
def min(values):
    smallest = None
    for value in values:
        if smallest is None or value < smallest:
            smallest = value
    return smallest
```
In the function version of the smallest code, we removed all of the print statements so as to be equivalent to the min function which is already built in to Python.


Ref:
1. https://medium.com/@mindfiresolutions.usa/python-7-important-reasons-why-you-should-use-python-5801a98a0d0b#:~:text=Python%20is%20a%20general%20purpose,care%20of%20common%20programming%20tasks.
2. https://www.openbookproject.net/thinkcs/python/english2e/ch02.html
3. https://books.trinket.io/pfe/index.html
