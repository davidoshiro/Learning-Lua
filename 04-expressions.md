Expressions
===========

Lua evaluates and calculates values via expressions. An expression may use one or more values to calculate another value. There are two types of expressions in Lua; arithmetic and relational.

Arithmetic Expressions
----------------------

We are all familiar with arithmetic expressions. `1 + 2` is a simple arithmetic expression. Expressions may be simple such as the previous example, or can be very complex such as `((1 + 2) * x) / y`. 

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

Relational Expressions
----------------------

