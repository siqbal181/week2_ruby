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
