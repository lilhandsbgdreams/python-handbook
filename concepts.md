---
layout: page
title: Concepts
---

Covers some basic concepts that you'll encounter in Python and other languages. As you get further in your learning, you'll discover that the concepts listed here are just the beginning.

1. [Control structures](#controlstructures)
2. [Functions](#functions)
3. [Input & output](#inputoutput)
4. [Data types](#datatypes)
5. [Sequence types](#sequencetypes)

# <a name="controlstructures">Control structures</a>

A control structure refers to one of three logical designs that determine the order in which statements execute in a program, as seen in [Figure 1](#structuresimage).

<a name="structuresimage">![control structures](https://raw.githubusercontent.com/lilhandsbgdreams/python-handbook/master/public/control_structures.gif "control structures")</a>
<sub><sup>**Figure 1**. Diagram of the three programming structures. \[Author unknown\]. PL/SQL User's Guide and Reference. http://docs.oracle.com/cd/A87860_01/doc/appdev.817/a77069/03_struc.htm.</sup></sub>

### Sequence structure
A program whose statements execute in the order that they appear, no matter what the circumstances, follows a sequence structure (Gaddis, 2015).

### Selection structure
A selection (or decision) structure has different paths it can take depending on the existing conditions (Gaddis, 2015). This structure can be created using an `if`, `if-else`, or `if-elif-else` condition in combination with some kind of Boolean expression. This Boolean expression can include a relational operator (`>=`, `<=`, `==`, `!=`) and even a logical operator (`and`, `or`, `not`).

### Repetition structure
Finally, a repetition (or iteration) structure causes the computer to repeat certain statements either a particular number of times or depending on whether a condition is being met (Gaddis, 2015). When we talk about loops in Python, we're talking about repetition structures. A for loop is a count-controlled loop. You might use this if you know exactly how many times you want some code to repeat. There are also while loops, which are condition-controlled loops. If the number of times a loop iterates (i.e., repeats) depends on a condition that could change at any point, you'll need a while loop.

These three control structures can be used to describe any program that exists. That's because the programs that you write could comprise of one, two or three of these control structures depending on the task at hand.

# <a name="functions">Functions</a>

A function is a collection of statements within a program that is designed to do a certain task (Gaddis, 2015). Imagine the tasks that go into getting ready in the morning. Each one of those tasks involves a series of subtasks. Those subtasks resemble functions because they are units of steps that must be executed in order to complete a larger task.

Creating functions is referred to as defining a function. A function definition in Python looks like this:

{% highlight py %}
def function_name(parameter1, parameter2, ...):
    statements...
{% endhighlight %}

Keep in mind that not all functions have to receive parameters. Not all functions send data to the line of code that called it either. These void functions, as they're called, simply terminate after they complete their task. Value-returning functions on the other hand have a return statement at the end of their statement block which sends data back to the line that invoked it.

# <a name="inputoutput">Input & output</a>

Input is data that is entered by the user of your program. A username entered into a game, a price entered into a digital cash register, or even a phrase typed into Google are all examples of input. Python uses the input() function to take user input. But in order to do something with that input, it must be assigned to a variable that the program can manipulate. Such an assignment statement would look like this: 

{% highlight py %}
var_name = input("string to prompt user")
{% endhighlight %}

Everything inside the quotes is the prompt that the user will see, and whatever she or he enters (aka, his or her input) in return gets assigned as a string to its assigned variable. Now because input() always returns a string, even if the user entered a number, you can use the int() and float() functions to convert that input into integers and floating-point numbers, respectively, that can be used in math calculations.

Output is data that a program sends to any one of the computer's output devices, such as the monitor or speakers. AS a beginning Python programmer, you'll mostly be concerned with the built-in `print()` function that sends string data to the monitor for the user to see. This function can accept one or many strings or variables (that can represent strings or numbers). `print("this string")` will print the string "this string" while `print("this string", this_var)` will print a string and whatever the variable `this_var` represents. Notice that strings are encased in either double or single qoutes. Also note that a comma separates the arguments passed to the `print()` function; when printed, there will automatically be a space between the string and the variable data.

# <a name="datatypes">Data types</a>

Different types of data are stored in different ways in computer memory. Data types are used in Python to reflect these data and the means by which they can be manipulated. As you start learning Python, keep in mind the type of data that you are handling because certain operations behave differently with different data types (Gaddis, 2015).

Table 1 shows the built-in data types that you are most likely to encounter as you begin with Python.

**Table 1.** Basic Python data types (Not a complete list of all built-in data types)<sup>1</sup>

|Python Syntax|Name/Description|Type|
|------------+-----------------+------|
|bool|Boolean value (either True or False)|Boolean|
|int|integer|Numeric|
|float|Floating-point number (real number)|Numeric|
|str|String|Sequence|
|list|List|Sequence|
|tuple|Tuple|Sequence|

<sub><sup><sup>1</sup><i>Source:</i> Gaddis, T. (2015). <i>Starting out with python.</i> Boston: Pearson.</sup></sub>

# <a name="sequencetypes">Sequence types</a>

The word sequence can be used to describe a control structure, but it is also a type of object that holds more than one piece of data (Gaddis, 2015). When we talk about sequences such as list and tuples, we are talking about data types (as discussed earlier). Lists and tuples are two sequence types that you are most likely to encounter when you begin learning programming, and thus they merit the following short discussion. 

The general syntax for a list looks something like this:

{% highlight py %}
list_name = [element0, element1, ...]
{% endhighlight %}

The data stored in a list is referred to as an element of that list. A list can, but doesn't necessarily have to, contain data of different types in each element. The most important thing to remember about a list is that it is mutable, which means that its contents can be altered. This is done by way of methods, functions and/or concatenation.

The general syntax for a tuple looks something like this:

{% highlight py %}
tuple_name = (element0, element1, ...)
{% endhighlight %}

Tuples differ from lists in that they are immutable, which means that their contents cannot be altered. Although tuples cannot be used with methods and functions that might alter their contents, they can still be used with methods and functions that don't post this threat. Using a tuple over a list can have some advantages. Tuples process faster than lists, making them useful when processing large sets of data. They are also useful when you want to protect a collection of data from being altered because of their immutability (Gaddis, 2015).

When working with both lists and tuples, you'll often find the need to take out and use just one, or a few, of the elements rather than the entire list of elements. In order to do this, you'll need to be familiar with what is referred to as indexing. Each list has an index, which keeps track of where in line each piece of data is in the list. The numbering for this index starts at 0. So a hypothetical list with three elements may have a length of 3, but its contents have indexes numbered 0, 1, and 2. When you refer to a particular element index in your code, you use subscript notation such as `list_name[x]`, where `x` is either the element's index number or a variable that holds a number.

&nbsp;


##### References
Built-in functions. (2015, November 23). Retrieved November 16, 2015 from https://docs.python.org/3/library/functions.html

Gaddis, T. (2015). <i>Starting out with python.</i> Boston: Pearson.

Langley, N. (2003). Python programs for beginners. <i>Computer Weekly</i>, 40. 

\[Untitled diagram of the three programming structures\]. (n.d.). Retrieved from http://docs.oracle.com/cd/A87860_01/doc/appdev.817/a77069/03_struc.htm
