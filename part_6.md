# Part 6

## An Introduction To Programming with Ruby

### What is programming?

Programming is the art of writing computer programs, but what is a program? To understand what a program is, we must first understand a little about how computers work. Your computer, the one you are reading this prework on, is a machine consisting of various parts. One of the most important parts is the [CPU][cpu] or "Central Processing Unit". Many think of the CPU as the brain of the computer, but its job is to carry out the [instructions][instructions] given to it.

An instruction when sent to the CPU is interpreted and handled according to what the CPU has been designed to do. For instance we can tell the CPU to add two numbers together. For the most part the CPU is relatively "dumb" as it can only do the things we explicitely tell it to do; however it is very fast at performing those tasks. This is the main reason we write computer programs, because the CPU will be multitudes faster than a human at performing tasks. In order for a CPU to understand the instruction we have given it, we must speak its language. What might an instruction look like to a CPU? Well an instruction to a CPU would look like this "00100000001000100000000101011110". If you were a 32-bit MIPS processor this would tell you add 350 to a value and store the result. Luckily for us programming has come a long way and we no longer have to keep track of the zeros and ones required to make a computer perform tasks.

### A brief history of programming

Early electronic computers abtracted the instructions passed to computers into a format known as assembly. Assembly abstracted out each instruction into words. That means our previous instruction "00100000001000100000000101011110" might look like "addi $r1, $r2, 350" in an assembly language. While this is a bit easier than the zeros and ones, it is still quite a bit difficult to understand and requires a lot of knowledge about a specific processor due to the fact that each processor has its own version of assembly.

In 1953, John W. Backus proposed to others at IBM that they develop a more practical alternative to assembly language. In 1957 the first Fortran compiler was delivered. A compiler is a computer program that transforms code written in one language to another. In this case the Fortran compiler transformed Fortran code into instructions for the IBM 704 mainframe. While this was not the first compiler written it was one of the first to gain widespread acceptance.

Over time computer programming evolved, each new language adding in additional features to make the job of the programmer easier. In the early days a programmer would have to understand a lot of information about the processor their code would run on, how to solve problems with very strict memory restrictions, and lots of hardware quirks they could exploit. Nowadays, most of these problems have already been solved for you allowing you to focus on the important parts of programming.

### A brief history of Ruby

Ruby is an [interpreted language][interpreted_language]. An interpreted language is one that runs its programs through an interpreter. An interpreter executes instructions immediately rather than compiling them. This is in contrast to compiled languages that we talked about before which require the instructions to be transformed before the program can be run. Interpreted programs tend to be easier to write and evolve, however, they tend to be much slower when compaired to compiled languages. Luckily for us, computers are extremely fast nowadays and we do not have to worry a great deal about the microseconds we will lose using an interpreted language over a compiled language.

Ruby is also an [object-oriented programming language][oo]. The goal of an object oriented programming language is to allow us to express the concepts we are trying to program as objects. We will go into more detail about this later, but you will frequently hear "Everything in Ruby is an object" from other Ruby developers. As we go into more details about Ruby keep this expression in mind.

Ruby was conceived by developer [Yukihiro Matsumoto][matsumotosan] in the early 1990s and its expressiveness and simplicty are admired by developers all around the world. Ruby was not extremely popular in the United States until [David Heinemeier Hansson][dhh] used Ruby to write a web framework known as Ruby on Rails. After the release of Ruby on Rails, Ruby grew dramatically in popularity in the United States. These days Ruby is used with Ruby on Rails to build some of the largest websites on the internet such as GitHub, Yammer, Shopify, and Basecamp. There are currently over 200,000 websites running Ruby on Rails, with that number growing steadily.

### Enough talk, onward to programming

To learn Ruby, we suggest working through the [Learn to Program Book][learn_to_program] by Chris Pine. We highly suggest following through and participating by completing all of the example programs. It is worth noting that this book was originally written around 2002 and references an older version of Ruby. No worries though as the current version of Ruby is backwards compatible and you will be able to use your modern version of Ruby and follow along with the book.

As you work through the [Learn to Program Book][learn_to_program] please commit your work to GitHub as well as ask questions in Campfire if you run into any problems.

[cpu]: http://en.wikipedia.org/wiki/Central_processing_unit
[instructions]: http://en.wikipedia.org/wiki/Instruction_(computer_science)
[interpreted_language]: http://en.wikipedia.org/wiki/Interpreted_language
[oo]: http://en.wikipedia.org/wiki/Object-oriented_programming
[matsumotosan]: http://en.wikipedia.org/wiki/Yukihiro_Matsumoto
[dhh]: http://david.heinemeierhansson.com/
[hello_world_program]: http://en.wikipedia.org/wiki/Hello_world_program
[string]: http://en.wikipedia.org/wiki/String_(computer_science)
[learn_to_program]: https://pine.fm/LearnToProgram/
