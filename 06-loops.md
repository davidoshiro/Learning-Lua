Loops
=====

Loops are another necessary type of statement in programming. Loops execute blocks of code for a predefined or undefined number of times. There are three types of loops in Lua:

* `for`
* `while`
* `repeat`

For example, let's print `Hello World` 10 times:

    for i=1, 10 do
      print('Hello World')
    end
    
    x = 1
    while x <= 10 do
      print('Hello World')
      x = x + 1
    end
    
    y = 1
    repeat
      print('Hello World')
      y = y + 1
    until y > 10

All of the above examples will output `Hello World` 10 times. Why are there different types of loops? As far as I can tell it has to do with what are trying to do. If you know that you want to do something for a specific number of times, you may prefer to use a for loop because the counting is done for you. If you want to evaluate a condition at the beginning of each block of code, then you would use the `while` loop. If you want to evaluate a condition at the end of a block then you would use the `repeat` loop.

Iterating Through Arrays
------------------------

Sometimes you will know how many items you have in your array and sometimes you will not. Lua makes it easy to iterate through arrays using the `for` loop.

If you have an array of 5 fruits, it is simple to print out each fruit.

    fruit = {"apple", "banana", "pear", "grape", "lemon"}
    for i=1, 5 do 
      print(fruit[i])
    end
    => apple
       banana
       pear
       grape
       lemon

Let's say you do not know the contents of your array, it is still simple to print out each item.

    for i,v in ipairs(fruit) do
      print(v)
    end
    => apple
       banana
       pear
       grape
       lemon

The example above shows the use of the `ipairs` function. This function allows you to iterate through all the items in an indexed array. the `i` and `v` variables contain the current array index and it's associated value. This is simple enough since the indexes start at 1 and gets incremented up to whatever `#fruit` may be.

But what about key/value tables? Remember that tables may use indexes and/or keys to reference values. Lua makes iterating through these tables simple as well.

    fruits = {apples="red", banana="yellow", orange="orange", grape="purple"}
    for k in pairs(fruits) do
      print(k .. " is " .. fruits[k])
    end
    => grape is purple
       orange is orange
       apples is red
       banana is yellow

The example above shows the use of the `pairs` function. While `ipairs` is used for indexed arrays, `pairs` is used for key/value tables as well as indexed arrays. You should notice that the `k` variable contains the current key and we are able to get its associated value via `fruits[k]`. But you'll notice that the order of the output is not how we initialized the `fruits` table. This is because the table is not indexed and therefore has no order. Ordering our list is easy enough, though.

    fruits = {{apples="red"}, {banana="yellow"}, {orange="orange"}, {grape="purple"}}
    for i,v in ipairs(fruits) do
      for k in pairs(v) do
        print(k .. " is " .. v[k])
      end
    end
    => apples is red
       banana is yellow
       orange is orange
       grape is purple

The example above shows that I created an index array of 4 items. Each item is a key/value table. This is sort of like a database where each indexed item is a row of data. Each row contains a fruit and its color. If we step through the `for` loops we will get the following:

* i=1 and v={apples="red"}
* k="apples" and v[k]="red"
* i=2 and v={banana="yellow"}
* k="banana" and v[k]="yellow"
etc...


