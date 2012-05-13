Expressions
===========

Lua evaluates and calculates values via expressions. An expression may use one or more values to calculate 
another value. There are two types of expressions in Lua; arithmetic and relational.

Arithmetic Operators
----------------------

Arithmetic operators are used to perform a calculation between two or more values. For example, 
`1 + 2` uses the `+` operator to add two numbers together. The expression returns a value of `3`.

Lua supports the following arithmetic operators:

* `+` (addition)
* `-` (subtraction)
* `*` (multiplication)
* `/` (division)
* `%` (modulo)
* `^` (exponentiation)
* `-` (negation)

    return 1 + 1 -- 1 plus 1
    => 2
    return 2 - 1 -- 2 minus 1
    => 1
    return 2 * 3 -- 2 multiplied by 3
    => 6
    return 5 / 2 -- 5 divided by 2
    => 2.5
    return 5 % 2 -- remainder of 5 / 2
    => 1
    return -(3 * 2)
    => -6

Relational Operators
--------------------

Relational operators are used to compare two or more values and return a `true` or `false` value. For 
example, `1 < 2` returns `true` since 1 is less than 2. `1 > 2` returns `false` since the expression is 
false.

Lua supports the following relational operators:

* `<` (less than)
* `>` (greater than)
* `<=` (less than or equal to)
* `>=` (greater than or equal to)
* `==` (equal to)
* `~=` (not equal to)

    return 1