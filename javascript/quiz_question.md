[Question1: What is the name of programs in JavaScript language? ](#question1)  

[Question2: How can JavaScript be executed not only in the browser, but also on the server, or on any device? ](#question2)  


[Question3: What makes JavaScript unique?](#question3)

[Question4: What is JS Virtual Machine?](#question4)

[Question5: Name some IDE/editors?](#question5)

[Question6: Which key is used to open the developer tools?](#question6)

[Question7: Is this correct statement? The type and language attributes are not required in JS.](#question7)

[Question8: What are the hotkeys to do comments in JS?.](#question8)

[Question9: What is "use strict"?](#question9)

[Question10: What are variables? Which keyword is used to declare the variable?](#question10)

[Question11: Can we decalre a variable twice?](#question11)

[Question12: What would be the output of this code?](#question12)
```ruby
let let = 5;

let return = 7;
```

[Question13: What are constants? Give syntax?](#question13)


[Question14: Number datatype supports what kind of number values?](#question14)

[Question15: In JavaScript, the “number” type cannot represent integer values larger than (2^53-1)? What is the solution for this limitation?  ](#question15)


## Question1

#### Answer

The programs in this language are called scripts. 

## Question2

#### Answer

Today, JavaScript can execute not only in the browser, but also on the server, or actually on any device that has a special program called the JavaScript engine.

## Question3

#### Answer

There are at least three great things about JavaScript:

- Full integration with HTML/CSS.
- Simple things are done simply.
- Support by all major browsers and enabled by default.


## Question4

#### Answer

The browser has an embedded engine sometimes called a “JavaScript virtual machine”.

Different engines have different “codenames”. For example:

V8 – in Chrome, Opera and Edge.
SpiderMonkey – in Firefox.

## Question5

#### Answer

###### IDE

- Visual Studio Code (cross-platform, free).
- WebStorm (cross-platform, paid).

###### Editors

- Atom (cross-platform, free).
- Sublime Text (cross-platform, shareware).
- Notepad++ (Windows, free).
- Vim and Emacs are also cool if you know how to use them.


## Question6

#### Answer

Most other browsers use F12 to open developer tools.


## Question7

#### Answer

Yes. The type and language attributes are not required.



## Question8

#### Answer

In most editors, a line of code can be commented out by pressing the Ctrl+/ hotkey for a single-line comment and something like Ctrl+Shift+/ – for multiline comments (select a piece of code and press the hotkey).



## Question9

#### Answer

The directive looks like a string: "use strict" or 'use strict'. When it is located at the top of a script, the whole script works the “modern” way.


## Question10

#### Answer

A variable is a “named storage” for data. We can use variables to store goodies, visitors, and other data.

To create a variable in JavaScript, use the let keyword.

The statement below creates (in other words: declares) a variable with the name “message”:
```ruby
let message;
```

## Question11

#### Answer

A variable should be declared only once.

A repeated declaration of the same variable is an error:

```ruby
let message = "This";

// repeated 'let' leads to an error
let message = "That"; // SyntaxError: 'message' has already been declared
```

## Question12

#### Answer

There is a list of reserved words, which cannot be used as variable names because they are used by the language itself.

For example: let, class, return, and function are reserved.

The code below gives a syntax error:

```ruby
let let = 5; // can't name a variable "let", error!
let return = 5; // also can't name it "return", error!
```
## Question13

#### Answer

To declare a constant (unchanging) variable, use const instead of let:

```ruby
const myBirthday = '18.04.1982';
```
Variables declared using const are called “constants”. They cannot be reassigned. An attempt to do so would cause an error


## Question14

#### Answer
The number type represents both integer and floating point numbers.


## Question15

#### Answer

BigInt type was recently added to the language to represent integers of arbitrary length.

A BigInt value is created by appending n to the end of an integer.

