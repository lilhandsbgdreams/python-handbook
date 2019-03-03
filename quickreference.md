---
layout: page
title: Quick Reference
---

Tables and lists for those moments when you need to quickly find a bit of Python information.

1. [Built-in functions](#builtin)
2. [Keywords](#keywords)
3. [Math operator precedence](#opprecedence)
4. [Modifying lists](#modlists)
5. [Number formatting](#numformat)
6. [Operators](#operators)
7. [Sequence slicing](#seqslice)
8. [Variable naming rules](#varnaming)

# <a name="builtin">Built-in functions</a>

Table 2 shows the built-in functions that come with the Python interpreter upon installation. 

**Table 2. Python's built-in functions**<sup>1</sup>

|`abs()`|`enumerate()`|`issubclass()`|`range()`|
|`all()`|`eval()`|`iter()`|`repr()`|
|`any()`|`exec()`|`len()`|`reversed()`|
|`ascii()`|`filter()`|`list()`|`round()`|
|`bin()`|`float()`|`locals()`|`set()`|
|`bool()`|`format()`|`map()`|`setattr()`|
|`bytearray()`|`frozenset()`|`max()`|`slice()`|
|`bytes()`|`getattr()`|`memoryview()`|`sorted()`|
|`callable()`|`globals()`|`min()`|`staticmethod()`|
|`chr()`|`hasattr()`|`next()`|`str()`|
|`classmethod()`|`hash()`|`object()`|`sum()`|
|`compile()`|`help()`|`oct()`|`super()`|
|`complex()`|`hex()`|`open()`|`tuple()`|
|`delattr()`|`id()`|`ord()`|`type()`|
|`dict()`|`input()`|`pow()`|`vars()`|
|`dir()`|`int()`|`print()`|`zip()`|
|`divmod()`|`isinstance()`|`property()`|`__import__()`|

<sub><sup><sup>1</sup><i>Source:</i> Built-in functions. (2015, November 23). Retrieved November 16, 2015 from [https://docs.python.org/3/library/functions.html](https://docs.python.org/3/library/functions.html)</sup></sub>

# <a name="keywords">Keywords</a>

Table 3 shows Python's keywords (aka, reserved words). Each of these serves a special purpose, so remember that they can't be used for variable names (Gaddis, 2015).

**Table 3. Python keywords**<sup>1</sup>

|`and`|`del`|`from`|`None`|`True`|
|`as`|`elif`|`global`|`nonlocal`|`try`|
|`assert`|`else`|`if`|`not`|`while`|
|`break`|`except`|`import`|`or`|`with`|
|`class`|`False`|`in`|`pass`|`yield`|
|`continue`|`finally`|`is`|`raise`||
|`def`|`for`|`lambda`|`return`||

<sub><sup><sup>1</sup><i>Source:</i> Gaddis, T. (2015). <i>Starting out with python.</i> Boston: Pearson.</sup></sub>

# <a name="operators">Math operators</a>

Table 4 shows Python's math, relational and logical operators. These can be used to do various things such as perform math operations, write statements, write Boolean expressions, or create control structures.

**Table 4. Python operators**<sup>1</sup>

Operator | Name/Description | Type
----- | ----- | -----
`+` | Additon | Math
`-` | Subtraction | Math
`*` | Multiplication | Math
`/` | Division| Math
`//` | Integer division, returns a whole number quotient. Either drops the fractional part if the quotient is positive or rounds away from zero if the quotient is negative. | Math
`%`| Modulus, divides two numbers but only returns the remainder of the quotient. | Math
`**` | Exponent | Math
`>` | Greater than | Relational
`>=` | Greater than or equal to | Relational
`<` | Less than | Relational
`<=` | Less than or equal to | Relational
`==` | Equal to, returns true if the operands to its left and right are equal to each other. Otherwise, it returns false. | Relational
`!=` | Not equal, returns true if the operands to its left and right are not equal to each other. Otherwise, it returns false. | Relational
`and` | Returns true if the Boolean expressions to its left and right are both true. Otherwise, it returns false. | Logical
`or` | Returns true if at least one of the Boolean expressions to its left and right is true. If neither is true, it returns false. | Logical
`not` | Only evaluates one Boolean expression to its right for its opposite truth. Returns true if the expression is false. Returns false if the expression is true. | Logical

<sub><sup><sup>1</sup><i>Source:</i> Gaddis, T. (2015). <i>Starting out with python.</i> Boston: Pearson.</sup></sub>

# <a name="opprecedence">Math operator precedence</a>

The order of operations in Python is similar to that which you probably learned in math class, except that some operations are grouped into tiers. The following list shows the order in which math operations are performed in Python (Gaddis, 2015):

1. Anything in parenthesis is done first.
   * `()`
2. Then exponents are performed.
   * `**`
3. Then multiplication, remainder and division operators are performed as they appear from left to right in the statement.
   * `*` `/` `//` `%` 
4. Finally, addition and subtraction are performed as they appear from left to right in the statement.
   * `+` `-`

# <a name="modlists">Modifying lists</a>

Table 5 shows some methods and functions that can be used to modify lists. The table's examples work with the following list:

{% highlight py %}
my_list = [11, 12, 3, 4, 5]
{% endhighlight %}

**Table 5. Methods and functions for modifying lists**<sup>1</sup>

|Method or Function|Result|Description|
|-----------+-----------+-------|
|<sub>`my_list.append(10)`</sub>|<sup><sub>`[11, 12, 3, 4, 5, 10]`</sub></sup>|<sub>This method appends an item to the list's end.</sub>|
|<sub>`my_list.insert(2, 10)`</sub>|<sup><sub>`[11, 12, 10, 3, 4, 5]`</sub></sup>|<sub>This method inserts an item (the second argument) into a specific index (indicated by the first argument).</sub>|
|<sub>`my_list.remove(5)`</sub>|<sup><sub>`[11, 12, 3, 4]`</sub></sup>|<sub>This method looks for an item and removes it from the list.</sub>|
|<sub>`my_list.index(3)`</sub>|<sup><sub>`2`</sub></sup>|<sub>This method returns the index where an item is found in the list.</sub>|
|<sub>`my_list.sort()`</sub>|<sup><sub>`None`</sub></sup>|<sub>Nothing is returned, but the list is sorted in ascending order.</sub>|
|<sub>`my_list.reverse()`</sub>|<sup><sub>`None`</sub></sup>|<sub>Nothing is returned, but the list is sorted in descending order.</sub>|
|<sub>`del my_list[1]`</sub>|<sup><sub>`[11, 3, 4, 5]`</sub></sup>|<sub>This function deletes an item from a specific index in the list.</sub>|
|<sub>`min(my_list)`</sub>|<sup><sub>`3`</sub></sup>|<sub>Returns the largest value from the list.</sub>|
|<sub>`max(my_list)`</sub>|<sup><sub>`12`</sub></sup>|<sub>Returns the smallest value from the list.</sub>|

<sub><sup><sup>1</sup><i>Source:</i> Gaddis, T. (2015). <i>Starting out with python.</i> Boston: Pearson.</sup></sub>

# <a name="numformat">Number formatting</a>

You can format floating-point numbers, integers, numbers in scientific notation, and percentages by using the built-in `format()` function. The `format()` function accepts two arguments: a number and a notation (within quotes) which specifies how to format the number. Table 6 shows some examples of how this function works.

**Table 6. Examples of the various uses of the `format()` function**<sup>1</sup>

|Example `format()`|Result|Description|
|-----------+-----------+-------|
|<sub>`format(1111.9876, '.2f')`</sub>|<sup><sub>`111.99`</sub></sup>|<sub>`.2` specifies the decimal place to which the number should be rounded. This number can  be changed depending on your needs. Meanwhile, `f` specifies that its a floating point number.</sub>|
|<sub>`format(111.9876, 'f')`</sub>|<sup><sub>`1,111.9876`</sub></sup>|<sub>The comma in the second argument indicates that the number should be comma separated.</sub>|
|<sub>`format(1.9876, '15f')`</sub>|&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;<sup><sub>`1.9876`</sub></sup>|<sub>`15` specifies the minimum number of spaces that the number should occupy. This number can be changed depending on your needs.</sub>|
|<sub>`format(1111.9876, '15,.2f)`</sub>|&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;<sup><sub>`1,111.99`</sub></sup>|<sub>This shows a combination of all of the above formats. Any combination of the above can be used depending on your needs.</sub>|
|<sub>`format(1111, ',d')`</sub>|<sup><sub>`1,111`</sub></sup>|<sub>The comma in the second argument indicates that the number should be comma separated. The `d` indicates that the number is an integer.</sub>|
|<sub>`format(1111, '15,d')`</sub>|&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;<sup><sub>`1,111`</sub></sup>|<sub>`15` specifies the minimum number of spaces that the integer should occupy. This number can be changed depending on your needs.</sub>|
|<sub>`format(0.9876, '.2%')`</sub>|<sup><sub>`98.76%`</sub></sup>|<sub>`%` multiplies the number by 100 and appends a percent sign to the end. `.2` specifies the decimal place to which the floating-point number should be rounded; this can be omitted or modified to fit your needs</sub>|

<sub><sup><sup>1</sup><i>Source:</i> Gaddis, T. (2015). <i>Starting out with python.</i> Boston: Pearson.</sup></sub>


# <a name="seqslice">Sequence slicing</a>

A slice is a portion of a sequence (Gaddis, 2015). Slices can be taken from lists, tuples or strings using the sequence index numbering system (in which the first item is numbered 0). The general syntax for a slice looks something like:

{% highlight py %}
sequence_variable[start:limit:interval]
{% endhighlight %}

Table 7 reflects slices of the following list and string variables.

{% highlight py %}
my_list = [10, 11, 12, 13, 14, 15]
str_var = 'This is my string.'
{% endhighlight %}

**Table 7. Examples of sequence slices**<sup>1</sup>

Example slice format | Result | Description
----- | ----- | -----
<sub>`my_list[1:5]`</sub> | <sub>`[11, 12, 13, 14]` </sub>| <sub>The slice starts at index 1 in the sequence. It goes up to, but does not include, index 5.</sub>
<sub>`str_var[1:5]`</sub> | <sub>`'his '` </sub>| <sub>In string sequences, spaces are part of the index numbering system.</sub>
<sub>`my_list[1:5:2]` </sub>| <sub>`[11, 13]` </sub>| <sub>Here, 2 indicates that the slice should start at index 1 and retrieve every other value.</sub>
<sub>`str_var[1:10:2]`</sub> | <sub>`'hsi y'` </sub>| <sub>(See previous description)</sub>
<sub>`my_list[1:]` </sub>| <sub>`[11, 12, 13, 14, 15]` </sub>| <sub>A blank end value returns everything all the way to the sequence's end.</sub>
<sub>`str_var[8:]`</sub> | <sub>`'my string.'`</sub> | <sub>(See previous description)</sub>
<sub>`my_list[:5]` </sub>| <sub>`[10, 11, 12, 13, 14]`</sub> | <sub>A blank start value returns everything from the beginning of the sequence up to the specified index value.</sub>
<sub>`str_var[:11]`</sub> | <sub>`'This is my '` </sub>| <sub>(See previous description)</sub>
<sub>`my_list[:]` </sub>| <sub>`[10, 11, 12, 13, 14, 15]` </sub>| <sub>Blank start and end values return everything in the sequence.</sub>
<sub>`str_var[:]`</sub> | <sub>`'This is my string.'`</sub> | <sub>(See previous description)</sub>
<sub>`my_list[-5:-1]` </sub>|<sub> `[11, 12, 13, 14]` </sub>| <sub>Negative values represent positions relative to the sequence's end.</sub>
<sub>`str_var[-10:]`</sub> |<sub> `'my string.'` </sub>| <sub>(See previous description)</sub>
<sub>`my_list[2:8]`</sub> | <sub>`[12, 13, 14, 15]` </sub>| <sub>The end value is greater than the length of the list. So, the list's length is used as the end.</sub>
<sub>`str_var[8:30]`</sub> | <sub>`'my string.'` </sub>| <sub>(See previous description)</sub>
<sub>`my_list[5:2]` </sub>|<sub> `[]` </sub>| <sub>An empty list is returned if the start value is greater than the end value.</sub>
<sub>`str_var[10:2]` </sub>| <sub>`''` </sub>| <sub>(See previous description)</sub>

<sub><sup><sup>1</sup><i>Source:</i> Gaddis, T. (2015). <i>Starting out with python.</i> Boston: Pearson.</sup></sub>

# <a name="varnaming">Variable naming rules</a>

The following rules must be followed when naming variables in your code.

1. Do not use Python keywords as variable names.
2. Do not put spaces in variable names.
3. Variable names must start with a letter between a-z, between A-Z, or an underscore.
   * All the other characters must be either letters a-z, A-Z, digits 0-9, or underscore characters.

<p class="message"><i>Note:</i> Variable names are case sensitive. So even though two variable names may have the same spelling, they are two distinct variables if they differ in lower or uppercase letter usage (Gaddis, 2015, p. 43).</p>

&nbsp;


##### References
Built-in functions. (2015, November 23). Retrieved November 16, 2015 from https://docs.python.org/3/library/functions.html

Gaddis, T. (2015). <i>Starting out with python.</i> Boston: Pearson.

Langley, N. (2003). Python programs for beginners. <i>Computer Weekly</i>, 40. 

\[Untitled diagram of the three programming structures\]. (n.d.). Retrieved from http://docs.oracle.com/cd/A87860_01/doc/appdev.817/a77069/03_struc.htm
