# week2_ruby
Going through Ruby basics

## Hello world

REPL - Read-Evaluate-Print Loop
When we run a REPL program we:
* set up the Ruby world, and
* we get the ability to write Ruby code to moifty that world on the fly.

Destroying & loading pre-written worlds
* in irb you can exist and close the programme but the world disappears and then the next time you run REPL program in irb, you'll get a brand new world
* you can use a file to store the instructions which we would have to type into the REPL
* when we require (import) the file into the program, it'll be executed automatically
* the result of the execution will be pre-written instructions and can provide an interactive window into the world

1. Create a Ruby file. Call the file `hello_world.rb`
2. Open the file in VSCode and `puts 1 + 1`
3. Save the file
4. Launch IRB
5. Require the file using `require ./hello_world.rb` and it will print out 2
6. Run the file directly using `ruby ./hello_world.rb`

The main difference between running the file through IRB and running it directly with Ruby is that running it through IRB loads the code into IRB's runtime environment, while running it directly executes the code as a standalone program.

## Variables & Statements

* Giving names to things which need to be sensible
* Variables are names for things - and the process of attachment is called assignment

`one = 1`
`two = 2`
`puts one + two` 
`3`

* An expression like `1 + 2` is a statement, same as `one = 1` is a statement

* You can also assign results of statements with names for example 
`fifteen = 10 + 5`

Constants 
* These are never changing objects that we assign
* Special rule for constants in that they are all capitals

`CONSTANT = object`

* When we start the program world, some constants come into existence automatically. One of these is `RUBY_VERSION` (I used ruby -v)
* In order to load all the names for our calculator from a file and into the REPL, the names need to be written as constants
* This is because variables can't be read outside the file they're written in, but constants can be

## Messages & Interfaces

* In response to our messages, objects return something
* If we do `one + 1` we send the `+` a message, telling it to add another number onto itself and return the result

` 1 + 2`
` 1.integer?`
* In both cases we're sending a message to an object, but in the first case, we've got a space before the message +, making the statement look like a regular sum.
* In the second case, the `.` between object & message

Dot syntax
* Dot is the only way to send messages to objective in Ruby
* Dot means "send this object a message" 
* `1.integer?` means send the object referenced by 1 a message asking if it's an integer or not
* `1 + 2` is actually translated to `1.+(2)`. We say and see "one plus two" and Ruby translates this to "send the object referenced by `1` a message to add itself to the object referenced by `2`.

Arguments
* 1.integer? is answerable on it's own and doesn't need another object
* When you do need another object to fulfil a message, you call the second object an argument

`# 2 is the argument`
`1.+(2)`
`3`

* The above is optional, but Ruby wants it to be simple

Making Random Numbers
`rand`


* Each time run, you get a random float between zero and one
* If you give rand an integer argument, you'll get a random number between zero and integer -1

`integer = 6`
`rand(integer)`
`2`

Floats
`> nine./(two)
`=> 4`

* On the above, integer objects don't understand decimal points, so they round them DOWN 
* 9/2 is 4.5 which the integer referenced by 'nine' rounds down to 4
* We need to use `to_f` to do floats

`4.to_f./(5)`
`0.8`
