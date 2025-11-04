# STATS506HW5
Homework 5 due Nov 14, 2025


Problem 1 - OOP Programming
Create a class to represent Wald-style normal approximation Confidence Intervals. Do this using S4.

For the waldCI class, define the following:

A constructor, which takes in either a mean and standard deviation, or a lower and upper bound along with a confidence level. This should be a custom constructor, not new() or waldCI().
A validator.
A show method, which takes as arguments level and digits.
Accessors: lb, ub, mean, sterr. lb and ub should take in level.
Setters: lb, ub, mean, sterr. Be sure to validate the resulting waldCI. lb and ub should take in a level.
A contains method, returning a logical of whether a value is within a CI of a certain level.
An overlap method, that takes in two waldCI’s and a level, and returns a logical of whether the two confidence intervals overlap.
as.numeric to return c(lb, ub) for a given level.
transform which takes in a monotonic function and a waldCI, and returns the transformed confidence interval.
All level arguments should have a reasonable default value. digits as well.

Use your waldCI class to create three objects:

ci1: 
, 95%
ci2: mean: 13, standard error: 2.5
ci3: 
, 75%
Evaluate the following code:

ci1
ci2
ci3
as.numeric(ci1)
as.numeric(ci2, .8)
as.numeric(ci3)
show(ci1, .9)
show(ci2, .8)
show(ci3, .75)
lb(ci2)
ub(ci2, .99)
mean(ci1)
sterr(ci3)
lb(ci2) <- 10.5
lb(ci2, .9) <- 10
mean(ci3) <- 34
contains(ci1, 17)
contains(ci2, 11, .9)
contains(ci3, 44)
overlap(ci1, ci2)
overlap(ci1, ci2, .99)
eci1 <- transform(ci1, exp)
eci1
show(eci1, .75)
mean(transform(ci2, sqrt))

Show that your validator does not allow the creation of invalid confidence intervals:

negative standard error
lb > ub
Infinite bounds
invalid use of the setters
Note that there are a lot of choices to be made here. What are you going to store in the class? How are you going to store them (what object types)? How are you going to enforce the function in transform being monotonic?

There is no right answer to those questions. Make the best decision you can, and don’t be afraid to change it if your decision causes unforeseen difficulties.

You may not use any existing R functions or packages that would trivialize this assignment. (E.g. if you found an existing package that does this, or found a function that checks for overlap between two CIs, that is not able to be used.)

Hint: It may be useful to define other functions that I don’t explicitly ask for.

Problem 2 - data.table
Repeat problem set 4, question 2, using data.table.

You can make the same or different decision as you did last time. You can also use or ignore the decisions I made in the solutions. As before, there is no “correct” answer (including those in the problem set 4 solutions).

Problem 3 - plotly
Repeat problem set 4, question 3 using plotly.

There is no expectation that you produce the exact same plots as last time. You may of course use your plots as last time, or the ones from the problem set 4 solutions, as inspiration for these plots.

These will be graded similar to last time:

Is the type of graph & choice of variables appropriate to answer the question?
Is the graph clear and easy to interpret?
Is the graph publication ready?
