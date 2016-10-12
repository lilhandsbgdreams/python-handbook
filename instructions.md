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

To check whether a variable is within a range, you would use a statement such as:

{% highlight js %}
x >= 10 and x <= 15
{% endhighlight %}

Follow these steps to create a statement like the one above:
1. **Determine the range that your variable should be within.** You'll need to know the lowest and highest integers that the variable could equal.
2. **Type a relational statement that checks whether a variable is greater than or equal to the low end of your range.** For example, if 10 is the smallest number that the variable x can equal in order for this relational statement to be true, you'd type:
`x >= 10`
3. **Type `and` after your first relational statement**. You'll use the `and` logical operator because you want to make sure that the variable is both greater than another integer *and* smaller than yet another integer.
4. **To the right of `and`, type a relational statement that checks whether the variable is less than or equal to the high end of your range.** For example, if 15 is the largest number that the variable x can equal in order for this relational statement to be true, you'd type: `x <= 15`

>*Note:* In the above example, `x >= 10 and x <= 15` would be true if `x` were assigned the integer 10, 11, 12, 13, 14, or 15. However, if `x` were assigned anything outside of the range such as 9 or 16, the statement would return false.



# <a name="functiondef">Defining a function</a>

# <a name="functioncall">Calling a function</a>

# <a name="for">Writing for loops</a>

# <a name="while">Writing while loops</a>

&nbsp;


##### References
Built-in functions. (2015, November 23). Retrieved November 16, 2015 from https://docs.python.org/3/library/functions.html

Gaddis, T. (2015). Starting out with python. Boston: Pearson.

Langley, N. (2003). Python programs for beginners. Computer Weekly, 40. 

\[Untitled diagram of the three programming structures\]. (n.d.). Retrieved from http://docs.oracle.com/cd/A87860_01/doc/appdev.817/a77069/03_struc.htm
