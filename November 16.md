# Design notebook for week ending November 16, 2014

## Description

So far, I have the conversion between boolean logic and executable functions nearly done. There are a few
thigns I want to check with Prof Ben about, but it is looking good so far.

## Questions

**What is the most pressing issue for your project? What design decision do
you need to make, what implementation issue are you trying to solve, or how
are you evaluating your design and implementation?**

At the moment, the most pressing issue is order of precedence. I need to make sure my code will
evaluate statements such as xvy^z correctly (btw, it is xv(y^z) ). Also, I need to think of a 
way to allow grouping by parens as a form of precedence to allow for (xvy)^z.

**What questions do you have for your critique partners? How can they best help
you?**

If you have any advice on the above, great, but no specific questions.

**How much time did you spend on the project this week? If you're working in a
team, how did you share the labor?**

This week, I spent a total of 3 hours outside of class working on the DSL. About 1 hour was getting Eclipse to be happy, the other two was spent actually coding.

## Post-critique summary
Those are some really good ideas. I know that this will become a tree, it is just coming up with how to tree-ify programmatically that will be difficult.

## Post-critique reflection
At this point, I have ideas using a program called pymclevel for constructing the stuff in Minecraft. The parsing problem
should be easy to figure out in Scala.
