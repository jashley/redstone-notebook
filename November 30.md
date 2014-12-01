# Design notebook for week ending November 30, 2014

## Description

Oh man, so much progress! I went from having a vague idea of what programs I would use to a working program!
I just put the code up, which includes a few shell scripts, the python code that does everything, and a python package
to handle placing blocks in minecraft.

## Questions

**What is the most pressing issue for your project? What design decision do
you need to make, what implementation issue are you trying to solve, or how
are you evaluating your design and implementation?**

As of now, the most pressing issue is that, if the circuits are too big, the signal dies. to fix this, I
need to programmatically add repeaters to strengthen the signal along the way, which shouldn't be too bad.
Aside from that, I would like to make it so inputs with the same variable name are connected. This, however,
is not easy, as it requires making sure that wires bridge to each other without interfering with other bridges.
I think I have an idea of how to do this, but it will be challenging. This will probably get done, but no
promises there.

**What questions do you have for your critique partners? How can they best help
you?**

The core of the project is there, I just need to add the repeaters and it will work. The above link leads to an image
of what a circuit looks like so far. It is just massive, which I also have plans to tweak. Aside from shrinking the whole
circuit, are there any design ideas you have? What would make this more appealing for the user? Also, the user currently must
specify the path to the python package, a name for the file which stores the minecraft commands, the name of their world,
and the logic function to evaluate. Does this seem reasonable or like it is too much?

**How much time did you spend on the project this week? If you're working in a
team, how did you share the labor?**

Oh, man. I spent a good 4 hours on Friday, 7 Saturday, and 6 today, so 17 hours. Break was fun!

## Post-critique summary

## Post-critique reflection
