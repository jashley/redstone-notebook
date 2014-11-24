# Design notebook for week ending November 23, 2014

## Description

This week, I finished up the parsing and internal representation portions of the project.
I have a way to translate text input of the form "x^yvz" and transform it into an AST.
The semantics portion of this is in the works, but is the most significant part, as it
involves taking the AST and transforming it into a form that can be read by Minecraft or
some external program to generate the expression as logic gates. In order to get the
semantics, I must understand what program I will be using to build the logic gates.

The core of my work this week has been looking into just that. There are a variety of ways
that will work, but some are impractical in different ways. The first I looked into was a 
program called MCEdit, which is a popular program for spawning custom mobs, building giant
structures, and generally altering the world in a way that is infeasible to do in-game. 
There are "filters" that are written in Python and allow users to build pre-coded structures,
which is exactly what I want to do. This is by far the easiest option for me. However, this
method requires the user to download MCEdit, navigate a confusing UI for first-time users,
and select a region large enough to fit the machinery. I have deemed this too complex for
the average user.

The second was an in-game item called a Command Block. These allow map makers to specify that
certain regions should be filled, or emptied, or have a zombie with a flaming bow, etc... This
means that I can have an external program generate the necessary code and all the user has to
do is copy-paste the code into the block. This is the easiest method for the user. However, 
because I do not want the user to have to place down multiple command blocks, and because each
command block only accepts one command, I really need a way to do this all in a single command.
Though it is <a href="https://www.youtube.com/watch?v=mGtGmmcdQZU">possible</a> to do this,
it is incredibly complex and I have deemed this too complex even with the benefit of usability.

What I have actually decided to go with is a Python package called pymclevel (there's a Python
package for everything). Essentially, this is a way to execute commands without needing to
use command blocks in-game. This is a nice middle-ground between ease of use for the user (no
need to use MCEdit) and ease of programming for me (click the link above). However, this does
require the user to download and install this code, which means a README.txt with the project
describing how to download and install the appropriate packages.

## Questions

**What is the most pressing issue for your project? What design decision do
you need to make, what implementation issue are you trying to solve, or how
are you evaluating your design and implementation?**

Currently, the biggest issue is figuring out how to take Scala ASTs and move
them into Python, where I will be coding the placing of blocks in Minecraft.
I am planning on having Scala write to a file that Python reads, but there
is probably a nicer way.

**What questions do you have for your critique partners? How can they best help
you?**

I expect to run into an issue as follows: If a user inputs (xvy)^(xvz), I will have two
OR gates ANDed together, where each OR gate has the same input x. I would like to have a
single lever controlling x, but that will involve wires crossing (the first x needs to
cross over the y). If you have any ideas for how to decide how to cross the wires, that
would be great. Alternatively, I may decide to place a lever for every input, meaning the
user would have to manually flip both levers if they wanted to change x. Is this reasonable,
or would this be too difficult for larger Boolean expressions?

**How much time did you spend on the project this week? If you're working in a
team, how did you share the labor?**

I spent about 2 hours in class and 7 hours outside of class finishing up the parsing and IR
and looking into the various ways to place blocks in Minecraft programmatically. I have also
been thinking off and on about how to deal with large Boolean expressions, but probably no
more than an hour of that kind of sheer brainstorming.

## Post-critique summary

## Post-critique reflection
