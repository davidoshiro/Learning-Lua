Strings
=======

Strings are probably the most commonly used data type. We already covered enclosing quotes in the previous lesson.
In this lesson we will cover the following:

* Multiline Quotes
* Escape Sequences
* Concatenation
* String Library
  * Find patterns in a string
  * Formatting a string
  * Replace patterns in a string
  * Convert string to lower case
  * Convert string to upper case
  * Reverse a string

Multiline Quotes
----------------

You can specify a multiline string via the double-bracket notation. 

    x = [[This is a very long string that contains
    line breaks. You can add any amount of text
    here with single and double quotes, but cannot
    use escape sequences.]]
    print(x)
    => This is a very long string that contains
    line breaks. You can add any amount of text
    here with single and double quotes, but cannot
    use escape sequences.

Escape Sequences
----------------

An escape sequence is preceded with a backslash `\` in a string. It allows you to safely add items in your 
strings without errors. Double-bracketed strings do not recognize escape sequences.

    x = "\"Lua rocks!\" said the programmer."
    print(x)
    => "Lua rocks!" said the programmer.
    y = "Hello\nWorld"
    print(y)
    => Hello
    World
    z = [[Hello\nWorld]]
    print(z)
    => Hello\nWorld

Concatenation
-------------

You can join one or more strings together via the `..` notation.

    x = "Hello World."
    y = "Lua Rocks!"
    print(x .. " " .. y)
    => Hello World. Lua Rocks!
    
The String Library
------------------

The string library allows you to manipulate strings even further.
    
Find the first occurance of a pattern in a string. Returns the start and end of the found pattern.

    x = "Hello World"
    print(x:find("or"))
    => 8      9
    print(x:find("zip"))
    => nil
    
Find a pattern and substitute all occurances with a string.

    x = "Hello World"
    print(x:gsub("World", "David"))
    => Hello David
    print(x:gsub("o", "."))
    => Hell. W.rld
    
Convert a string to lower case.

    x = "Hello World"
    print(x:lower)
    => hello world
    
Convert a string to upper case.

    x = "Hello World"
    print(x:upper)
    => HELLO WORLD
    
Get string length.

    x = "Hello World"
    print(x:len)
    => 11
    print(#x)
    => 11