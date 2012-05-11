Lua Data Types
==============

Tutorial on the different data types in Lua.

Nil
---

All undeclared or empty variables have a value of `nil`. 

  print(x) => nil
  local y
  print(y) => nil
  
Booleans
--------

Boolean values are `true` and `false`. Anything other than `false` or `nil` is considered `true`. `nil` is the same as `false`.

    x = true
    print(x) => true
    y = false
    print(y) => false
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
    print(x) => 1
    y = 1.00
    print(y) => 1
    z = 1.25
    print(z) => 1.25
    print(x + z) => 2.25

Strings
-------

Strings can be of any length. Strings must be enclosed by double quotes, single quotes or double brackets.

    x = "Hello World."
    print(x) => Hello World
    y = "Halley's Comet"
    print(y) => Halley's Comet
    z = ""This isn't mine!" said Johnny."
    print(z) => error
    z = [["This isn't mine!" said Johnny."
    print(z) => "This isn't mine!", said Johnny.
    
Escape sequences can also be used in strings

    x = "The ghost said, \"Boo!\""
    print(x) => The ghost said, "Boo!"
    y = "This is line 1\nThis is line 2\nThis is line 3"
    print(y) => This is line 1
    This is line 2
    This is line 3
    
Strings can be concatenated using `..`.

    x = "Hello"
    y = "World"
    print(x .. y) => HelloWorld
    print(x .. " " .. y) => Hello World