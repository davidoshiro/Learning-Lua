Lua Data Types
==============

Tutorial on the different data types in Lua.

Nil
---

All undeclared or empty variables have a value of `nil`. 

    print(x) 
    => nil
    local y
    print(y) 
    => nil
  
Booleans
--------

Boolean values are `true` and `false`. Anything other than `false` or `nil` is considered `true`. `nil` is the same as `false`.

    x = true
    print(x) 
    => true
    y = false
    print(y) 
    => false
    if(z) then
      print("Yes")
    else
      print("No")
    end
    => No
    
Numbers
-------

In Lua all numbers are floating-point numbers. There is no integer.

    x = 1
    print(x) 
    => 1
    y = 1.00
    print(y) 
    => 1
    z = 1.25
    print(z) 
    => 1.25
    print(x + z) 
    => 2.25

Strings
-------

Strings can be of any length. Strings must be enclosed by double quotes, single quotes or double brackets.

    x = "Hello World."
    print(x) 
    => Hello World
    y = "Halley's Comet"
    print(y) 
    => Halley's Comet
    z = ""This isn't mine!" said Johnny."
    print(z) 
    => error
    z = [["This isn't mine!" said Johnny."
    print(z) 
    => "This isn't mine!", said Johnny.
    
Escape sequences can also be used in strings

    x = "The ghost said, \"Boo!\""
    print(x) 
    => The ghost said, "Boo!"
    y = "This is line 1\nThis is line 2\nThis is line 3"
    print(y) 
    => This is line 1
    This is line 2
    This is line 3
    
Strings can be concatenated using `..`.

    x = "Hello"
    y = "World"
    print(x .. y) 
    => HelloWorld
    print(x .. " " .. y) 
    => Hello World
    
The length of a string can be determined by using the prefix `#`.

    x = "Hello World"
    print(#x)
    => 11
    
Tables
------

Tables are like associative arrays. Array indexes may be numbers or strings.

    x = {'a', 'b', 'c'}
    print(x[1])
    => a
    y = {name="John", age=21, is_male=true}
    print(y.name)
    => John
    print(y["name"])
    => John
    
Note you may specify the index via the bracket notation `y["name"]` or dot-notation `y.name`. If the index name is stored in a variable use the bracket-notation.

    i = "name"
    x = {}
    x.name = "John"
    print(x.i)
    => nil
    print(x[i])
    => John

The length of the table can be determined by using the `#` prefix.

    x = {'a', 'b', 'c'}
    print(#x)
    => 3
    
Querying Data Types
-------------------

You can query a variable for its data type by using the `type()` function.

    a = nil
    b = true
    c = 10
    d = "Hello World"
    e = {one=1, two=2, three=3}
    print(type(a))
    => nil
    print(type(b))
    => boolean
    print(type(c))
    => number
    print(type(d))
    => string
    print(type(e))
    => table