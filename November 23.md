# Design notebook for week ending November 23, 2014

## Description

**TODO:** Fill in this part with information about your work this week:
important design decisions, changes to previous decisions, open questions,
exciting milestones, preliminary results, etc. Feel free to include images
(e.g., a sketch of the design or a screenshot of a running program), links to
code, and any other resources that you think will help clearly convey your
design process.

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



## Questions

**What is the most pressing issue for your project? What design decision do
you need to make, what implementation issue are you trying to solve, or how
are you evaluating your design and implementation?**

**What questions do you have for your critique partners? How can they best help
you?**

**How much time did you spend on the project this week? If you're working in a
team, how did you share the labor?**

## Post-critique summary

## Post-critique reflection
