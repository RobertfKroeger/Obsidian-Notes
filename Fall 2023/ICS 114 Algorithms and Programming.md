Knowledge Base
## Algorithms
An algorithm is the solution to a specific problem with these 4 characteristics:
1) Be Unambiguous
	- having or exhibiting no uncertainty. At each step, from beginning to end it is clear precisely what must be done. Precise. Definite.
2) Be effective
	- the ability to produce a desire outcome or output. The solution is "correct".
3) Finite in terms of Time and Space
	- In terms of space and time the algorithm must have a logical conclusion. Cannot continue forever, cannot take an infinite amount of space.
4) Finite in terms of Input and Output
	- Must have a finite amount of inputs, zero or more, but finite.
	- at least one output, the "answer"

### Flowcharts and Pseudocode
- a useful tool in writing algorithms is to use a flowchart to represent the Flow of Control, these can be represented in a number of ways.
- Pseudocode: informal high level description of an Algorithm or Program. 
- It is best to write an algorithm in Pseudocode before beginning to implement anything.
## Top-down design and Stepwise Refinement

### Top-down Design
The first step Top-down design is the process of creating a **Top Level Algorithm**, generally these are very general steps of an algorithm and have very few specific details.
Each step of an algorithm is generally referred to as a **module**, and in Java they are implemented as **Methods**.

### Stepwise Refinement
- Generally refers to the acting of writing something, checking it's effectiveness or correctness via compilation or error testing then repeating the process. Often new programmers will think writing large blocks of code between testing is better, but this is foolhardy.

## Flow of Control
There are three major structures that control the flow of an algorithm:
1) Sequential
	- One step of the algorithm perform followed by the next and then the next.
	- An example of sequential control structure is the creation of an algorithm with the Top-down approach.
2) Selection or Conditional
	- perform or do not perform based on an action, generally a true or false condition. 0 for False, 1 for True.
3) Repetition
	- Perform one or more steps

### Conditionals
1) If Statements
	- Used to execute a statement or not, based on condition present in the system.
	- If condition is evaluated True, the code block inside the condition is executed.

``` java
if raining
	take umbrella
```
A Java syntax example of  If Statement
```java 
if(x >= 10) {
	System.out.print("X is greater than or equal to 10");
}
```
2) If...Else Statements
	- Used if there are two different possibilities and you want to pick one of them.
``` java
if raining
	drive to school
else
	take the bus
```
A Java Syntax example of If...Else
```java
if(x > 10) {
	System.out.print("X is greater than 10");
} else {
	System.out.print("X is not greater than 10");
}
```
3) Nested If...Else
	- Used to decide on something when there are multiple conditions
	- These are used to pick only one of many choices.
``` java
if peckish
	eat a light snack
else if hungry
	have a meal
else if starving
	eat a horse
else
	dont eat
```
A Java Syntax example of Nested If...Else
```java
if(x > 10) {
	System.out.print("X is greater than 10");
} else if(x < 10) {
	System.out.print("X is less than 10");
} else {
	System.out.print("X is equal to 10")
}
```
4) Switch Statement
	- An alternative to a Nested If...Else statement that can be used to make programs more readable.
	- Can be used with Integers, Characters, and Strings. 
	- Can only be used to assess equality, not relationships between numbers.


### Loops or Repetition
Formal repetition construct implemented in most programming languages. In general there are three main types of loops.

1) For loop
	- Also known as **definite** or **counted loops**, these loops are **pretested**.
	- executes a pre-defined amount of times before concluding.
	- we know how many times the loop will execute before it is executed.
	- may be executed 0 or more times
	- Termination of the loop does not depend on anything that happens within the loop body.
``` java
for all eggs in recipe
	crack eggs into bowl
```
A Java syntax example of a For Loop
``` java
for(int i = 0; i < loopValue; i++) {
	System.out.print("This is the loop's body");
}
System.out.print("This statement prints after the loop finishes executing.")
```
2) While loop
	 - an **indefinite** loop, these loops are **pre-tested**
	 - executes based on conditions established in the conditional of the loop
	 - always executed 1 or more times, and we do not generally know how many times the loop is executed.
``` java 
while butter and sugar is not light and fluffy
	cream butter and sugar
```
A Java Syntax example of a While loop
``` java
int x = 0;
while(x < 10) {
	System.out.print("This statement prints while the loop occurs");
	System.out.print("the incrementing value, in this case x must be increased if the loop is to end");
	x++;
}
```
1) Do-While loop
	- an **indefinite** loop, these loops are **post-tested**
	- executes based on conditions established in the conditional of the loop, and the condition is tested after the loop body takes place.
	- use whenever you always want to execute the loop body at least once.
``` java
do  
	salt what you are cooking
	
while cooking is bland and tasteless
```
The Java Syntax for the Do...While loop
``` java
do {
	System.out.print("This stuff is done initially and it independant of the conditional, in other words it always occurs at least once");
	System.out.print("These statements occurs while the variable is true and must be incremented");
	incrementVariable++;
} while (incrementVariable < 10);
```

## Syntax 
- The rules that define the combinations of symbols that are considered to be correctly structured statements or expression in that language.
- Java follows a syntax that utilizes semicolons to mark the end of code blocks.
## High-level programming languages
## OOP
## Java Types
### Primitive Data Types
- Boolean: a Boolean variable is one that logically equates to true or false.
	-  aka Relational Operators
	1) == is equal to, whereas = is the assignment operator
	2) != is not equal to
	3) > greater than
	4) < less than
	5) >= greater than or equal to
	6) <= less than or equal to
This is how a Boolean variable is declared:
``` java
boolean tOrF = true;
```
- Integer
	- Integers are broken up into Long, Short and Integer values based upon the size that you want for them.
	- Floating point variable in Java come in the form of Double, Float and Long, these also depend on the size that you want them to be able to contain and have an implicit casting from smaller to larger but if you are going from a larger variable to a smaller you must specifically cast them.

Integers in Java are declared like this:
``` java
int thisIsAnInteger = 100;
```

This is how floating point variable are initialized and how to cast them:
``` java
float thisIsAFloat = 62.5f;
```

``` java
double castingToDouble = (double)thisIsAFloat;
```
When you are putting variables into floating point variable it is also important to state which kind of precision you are wanting to store them in. Such as the example above where the f has to follow the numbers to show that is should be stored in only float-level precision.
- Char
	- The Char data type holds one character and is initialized like this:
``` java
char thisIsAChar = 'A';
System.out.print("Notice how the char data type uses single quotes!");
```
- Strings 
	- in Java are not primitive data types in Java but are used so commonly that before we learn about Reference variable we will long be using String so we should know how they are initialized and declared.
``` java
String thisIsAString = "Hello, how are you? I am a string.";
System.out.print("Notice how the String uses double quotes, whereas Char uses one. This is important.");
```

### Class Types / Reference Variables


## Initialization and Assignment
Initialization and Assignment in Java takes the form of:

```java
dataType variable = value;
```

Where dataType represents a type, primitive or reference, variable is the name of the assigned variable, and value is the value assigned to variable. 

### Java Data Types
- Data types can be declared as a **constant** and use a Capital case with underscores to separate.
``` java
final int JAVA_FINAL_EXAMPLE = 100;
```
## Type Conversion and Casting
- Type conversion in Java is handled as a Widening or Shortening of size, where widening is done for free my the compiler and shortening will throw an error so as to not lose precision without the programmer knowing.
## Error Handling
- Error handling in Java is handled by Try and Catch statements.
- Errors in Java are called **Exceptions**

## Arrays
- Array can also be initialized in a parallel fashion for data that is related, they must be the same size as in their length must be the same.
- Array size will generally be declared with a constant value with the final attribute
- The purpose of arrays is to store and reference values, when you want to access data more than once.
### Array Declaration
- Arrays are declared and created in two steps:
1) A reference variable is declared, and is a reference to an Object.
2) To then Create the array
3) to assign the address of the array to the reference variable.
``` java
final int arraySize = 42;
int[] meaningOfLife = new int[arraySize];
System.out.print("This is the one step creation");
```
The size of the array is declared as a constant, then the reference variable for the array is created, then assigned to the address that is created when new is used. Arrays also have innate values of length used array.length()
### Array Initialization
- Arrays can be initialized by visiting individual elements, by using loops to visit each index in the element, and in the declaration of the array.
1) Initializing individual elements:
``` java
final int MAX = 6;
int[] numbers = new int[MAX];
number[0] = 7;
System.out.print("Position 0 is assigned the value of 7");
```
2) Initializing arrays with a loop:
``` java

```

## Array Traversal
- Traversing an array requires a definite loop because we are aware of how many elements are in the loop
- This method uses the classic for loop:
``` java
int numbers[] = new int[10];
for(int i = 0; i < numbers.length; i++) {
	System.out.print("This is the element of the array ->" + numbers[i]);
}
```
- For readability an enhanced for loop can be better when dealing with arrays:
``` java
for(int number: numbers) {
	System.out.print("This represents the element of the array ->" + number);
}
```
- Enhanced for loops are simply to traverse the loops and are not to change any values.
- They are also only designed to traverse every element from beginning to end.
## Reference variables
- Reference variables contain addresses to the object that they are referencing, when you reference it you are accessing it's address in main memory.
- In other languages reference variables are referred to as pointers.

## Writing Methods
- When writing methods certain things are important to consider
	1) The name of the method, pick something meaningful.
	2) The return type of the method
	3) The parameters of the method
	4) The action the method takes
``` java
public static int biggest (int value1, int value2) {
	System.out.print("This method will find the biggest of two values provided");
	if(value1 > value2) {
		return value1;
	} else {
		return value2;
	}
}
```