---
layout: page
title: Instructions
---

These instructions will help you perform some, though not all, common tasks in Python programming.

1. [Checking whether a variable is inside/outside of a range](#range)
2. [Defining a function](#functiondef)
3. [Calling a function](#functioncall)
4. [Writing for loops](#for)
5. [Writing while loops](#while)

# <a name="range">Checking whether a variable is inside/outside of a range</a>

Relational and logical operators can be used to quickly determine whether a variable is inside or outside a given range of numbers. The following steps refer specifically to an integer variable, but they can easily be used with a floating-point variable.

### To check whether a variable is within a range, you would use a statement such as:

{% highlight py %}
x >= 10 and x <= 15
{% endhighlight %}

Follow these steps to create a statement like the one above:

1. **Determine the range that your variable should be within.** You'll need to know the lowest and highest integers that the variable could equal.
2. **Type a relational statement that checks whether a variable is greater than or equal to the low end of your range.** For example, if 10 is the smallest number that the variable x can equal in order for this relational statement to be true, you'd type:
`x >= 10`
3. **Type `and` after your first relational statement**. You'll use the `and` logical operator because you want to make sure that the variable is both greater than another integer *and* smaller than yet another integer.
4. **To the right of `and`, type a relational statement that checks whether the variable is less than or equal to the high end of your range.** For example, if 15 is the largest number that the variable x can equal in order for this relational statement to be true, you'd type: `x <= 15`
   <p class="message"><i>Note:</i> In the above example, `x >= 10 and x <= 15` would be true if `x` were assigned the integer 10, 11, 12, 13, 14, or 15. However, if `x` were assigned anything outside of the range such as 9 or 16, the statement would return false.</p>

### To check whether a variable is outside of a range, you would use a statement such as:

{% highlight py %}
x < 10 or x > 15
{% endhighlight %}

Follow these steps to create a statement like the one above:

1. **Determine the range that your variable should be outside of.** You'll need to know the lowest and highest integers that the variable should not equal.
2. **Type a relational statement that checks whether the variable is less than the low end of your range.** For example, if variable `x` can equal anything lower than, but excluding, `10`, you'd type: `x < 10`
3. **Type `or` into your statement.** You'll use the `or` logical operator because you want to make sure that the variable is either less than another integer *or* greater than yet another integer.
4. **Type a relational statement that checks whether the variable is greater than the high end of your range.** For example, if the variable `x` can equal anything greater than, but not including, `15` , you'd type: `x > 15`.
   <p class="message"><i>Note:</i> In the above example, `x < 10 or x > 15` would be true if `x` were assigned an integer less than or equal to 9 or an integer greater than or equal to 16. However, if `x` were assigned the integer 10, 11, 12, 13, 14 or 15, the statement would be false.</p>

# <a name="functiondef">Defining a function</a>

The basic syntax for a defining a function looks like this:

{% highlight py %}
def function_name(parameter1, parameter2, ...):
    statement
    statement...
{% endhighlight %}

To define your own function:

1. **First, you need to know what your function should do and how it should do it.** You should know:
   * **The inputs your function will take in.** These could be parameters passed to it or variables assigned to user inputs within the function.
   * **The processes it should perform on those inputs.** What steps will your function take to accomplish its task? You should consider the control structures discussed earlier in this handbook.
   * **The outputs that your function will produce.** A void function doesn't return data to the code line that calls it, but it can still print something to the screen for the user to read. A value-returning function returns data to the line of code that calls it, so you'll want to consider what data your function needs to send to the rest of the program.
2. **Write your function header.** This is the first line in a function definition.
   * **Type `def` to indicate that you are defining a function.**
   * **Type your function name.** Function names generally adhere to the same variable naming conventions. Giving your function a name that describes what it does is helpful.
   * **Type `():` and use the space between the parentheses to define whether the function will take parameters.**
      * **Function with parameters:** Type the parameter names(s) within the parentheses. Remember that the parameter names(s) only exist within the function as a shorthand way for the function's statements to reference the data that was passed in. So, parameter names are meaningless to any statements outside of the function.
      * **Function without parameters:** Don't type anything within the parentheses.
3. **Write the function's statement block.** These are all the statements which work together to accompish the function's processes and produce its outputs. Indent these lines under the function header so that the interpreter knows that they belong only to the function definition.

# <a name="functioncall">Calling a function</a>

The basic syntax for calling a function looks like this:

{% highlight py %}
func_name(argument1, argument2, ...)
{% endhighlight %}

To call a function that has been defined:

1. **Type the function's name.**
2. **Type `()`, then:**
   * **If the function accepts arguments, type values or variable names into the parentheses.** How many arguments you type depends on how many paramenters the function accepts. To know if the function accepts arguments, and how many, look at the function's header for parameters. You will have to research how many arguments a built-in function takes.
   * **If the function does not accept arguments, don't type anything within the parentheses.** To know if the function accepts arguments, and how many, look at the function's header for parameters. You will have to research how many arguments a built-in function takes.

# <a name="for">Writing `for` loops</a>

`for` loops are called count-controlled loops because the number of times they iterate is controlled by a number. The general syntax of a for loop is:

{% highlight py %}
for var_name in [sequence_item1, seq_item2, ...]:
    statement
    statement...
{% endhighlight %}

<p class="message"><b>Caution:</b><br>Before executing code that involves loops, make sure that your loop's logic and statements have a way of reaching an end and terminating. Infinite loops that have no way of terminating may cause the computer to freeze or crash.</p>

To write your own for loop:

1. **Write the first line.**
   * **Type `for` to indicate the loop type.**
   * **Type a target variable name that will hold a different value from the list each time the loop iterates.** This target variable is only a shorthand way for the loop to reference the data that it's processing from the list. So, remember that it will only exist within the loop and is meaningless to any statements outside the loop.
   * **Type `in` after your variable name.**
   * **Type one of the following next:**
      * A list; e.g. `[item1, item2, ...]`
      * A tuple; e.g. `(item1, item2, ...)`
      * A variable that references a list, tuple or string; e.g. `my_list`, `my_tuple`, or `my_string`
      * A range numbers; e.g. `range(5)`, `range(len(my_list))`, `range(1,100,2)`, etc.
   * **Type a colon symbol.** This indicate the end of the first line and the beginning of the statement block.
2. **Write the statement block.** Indent these statements to indicate they belong to the for loop. These statements will execute until the loop reaches the end of the sequence given in the for clause. The value held in the target variable each time the loop iterates may be helpful to include here.

<p class="message"><b>Caution:</b><br>Before executing code that involves loops, make sure that your loop's logic and statements have a way of reaching an end and terminating. Infinite loops that have no way of terminating may cause the computer to freeze or crash.</p>

# <a name="while">Writing `while` loops</a>

`while` loops are called condition-controlled loops because they iterate until a certain condition is met. They are also called pretest loops because they test for a condition before deciding whether to initiate the loop. The general syntax of a while loop is:

{% highlight py %}
condition = True
while condition:
    statement
    statement...
    // these must eventually set condition = False

{% endhighlight %}

<p class="message"><b>Caution:</b><br>Before executing code that involves loops, make sure that your loop's logic and statements have a way of reaching an end and terminating. Infinite loops that have no way of terminating may cause the computer to freeze or crash.</p>

To write your own `while` loop:

1. **Write the first line.**
   * **Type `while` to indicate the loop type.**
   * **Type a statement that serves as the condition.** As long as this condition is true, the loop will iterate. This can statement can look something like:
      * `boolean_variable` (here the loop will execute as long as this boolean variable name represents `True`)
      * `repeat_state = 'yes'`
      * `repeat_state != 'no'`
      * `num < 5` or some other condition you want to check for
      * ... etc.
   * **Type a colon symbol.** This indicate the end of the first line and the beginning of the statement block.
2. **Go one line above what you just typed and set the pretest condition.** In order for while to begin looping, its condition must be met initially. So, for whatever condition you created in step 1, you must write a statement that makes this condition initially true. This guarantees that while will execute at least once.
   <p class="message"><i>Note:</i> If you have a good understanding of the loop that you are writing, or if you plan in advance, you could perform this step first instead of second. </p>
3. **Go one line below where you typed `while`, and write the statement block.** Indent these statements to indicate they belong to the while loop. These statements will execute as long as the condition is still true. Using these statements, you must create a way for the condition to eventually become so that the loop can terminate.

<p class="message"><b>Caution:</b><br>Before executing code that involves loops, make sure that your loop's logic and statements have a way of reaching an end and terminating. Infinite loops that have no way of terminating may cause the computer to freeze or crash.</p>



&nbsp;


##### References
Built-in functions. (2015, November 23). Retrieved November 16, 2015 from https://docs.python.org/3/library/functions.html

Gaddis, T. (2015). <i>Starting out with python.</i> Boston: Pearson.

Langley, N. (2003). Python programs for beginners. <i>Computer Weekly</i>, 40. 

\[Untitled diagram of the three programming structures\]. (n.d.). Retrieved from http://docs.oracle.com/cd/A87860_01/doc/appdev.817/a77069/03_struc.htm
