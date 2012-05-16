If Then Else
============

Now that we know how to write expressions using relational and logical operators, we can use them to add logic to
our programs. The most simple and commonly used way to add logic to a program is by using `if` statements. 

Let's look at some basic `if` statements.

    if(1+2 == 3) then print("Correct!") end
    => Correct!
    if(false) then print("Correct!") else print("Incorrect!") end
    => Incorrect!
    x = "Hello World"
    if(string.lower(x) == "hello world") then
      print(string.upper(x))
    else
      print("Sorry")
    end
    => HELLO WORLD
    
The `if` statement evaluates an expression and performs the following code block if the expression is `true`.
If the expression is `false` then the optional `else` block is executed.

Sometimes doing many `if` statements is required and can be tedious. Lua allows you to add `elseif` 
blocks in addition to the `else` block.

    x = {
      {fruit="apple", taste="sweet", is_juicy=true},
      {fruit="banana", taste="sweet", is_juicy=false},
      {fruit="lemon", taste="sour", is_juicy=true}
    }
    if(x[2].taste == "sweet" and x[2].is_juicy) then
      print("This is an apple")
    elseif(x[2].taste == "sweet" and not x[2].is_juicy) then
      print("This is a banana")
    elseif(x[2].taste == "sour" and x[2].is_juicy)
      print("This is a lemon")
    else
      print("Fruit is unknown")
    end
    => This is a banana

Even though code blocks consist of a single `print()` statement, you are not limited to any number of statements.
You can even nest other `if` statements as code blocks in an `if` statement.
  