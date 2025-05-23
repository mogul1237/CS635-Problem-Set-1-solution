# CS635-Problem-Set-1-solution

Download Here: [CS635 – Problem Set #1 solution](https://jarviscodinghub.com/assignment/cs635-problem-set-1-solution/)

For Custom/Original Work email jarviscodinghub@gmail.com/whatsapp +1(541)423-7793

1 Warm-Up Problem
1.1 Problem
Enter and solve the following linear program in GAMS
minx1,x2,x3
3×1 + 2×2 − 33×3
subject to x1 − 4×2 + x3 ≤ 15
9×1 + 6×3 = 12
−5×1 + 9×2 ≥ 3
x1, x2, x3 ≥ 0
Use the statement “option limrow=0, limcol=0;” to suppress some of the compiler output
(not needed in this exercise) from the “lst” file. Also use the expression “positive variables”
to get the lower bounds on the variables instead on setting the lower bounds with “lo”. You
should have your gams file display the solution. You should create parameters objval,
x1val, x2val, and x3val to do this as follows.
Assuming that you call your (GAMS) decision variables x1, x2, and x3, and your objective
variable is obj, your code will look like:
parameter x1val, x2val, x3val, objval;
objval = obj.l ;
x1val = x1.l ;
x2val = x2.l ;
x3val = x3.l ;
display objval, x1val, x2val, x3val ;
Problem 2 Page 1
CS635 Problem Set #1 Prof Michael Ferris
2 Index sets and bounds
2.1 Problem
Use an appropriate set J and declare variables x(J) along with upper and lower bound
statements to formulate and solve:
maxx1,x2,x3
5(x1 + 2×2) − 11(x2 − x3)
subject to 3×1 ≥ x1 + x2 + x3
0 ≤ xj ≤ 3, j = 1, . . . , 3
You should enter the problem as written above – there is no need to do arithmetic to
simplify the objective or constraints. Ensure the model is called prob2.
Look through the solution report in the listing file to ensure that you understand where
all the relevant pieces of information are stored. Use a display statement to print out the
level values of the variables, their lower and upper bounds, and the value of the objective
function:
display x.l, x.lo, x.up, prob2.objval;
3 Soft Suds
The Soft Suds Brewing and Bottling Company, because of faulty planning, was not prepared
for the UW Comp Sci Department. There was to be a big party in Madison and Gus Guzzler,
the manager, knew that Soft Suds would be called upon to supply the refreshments. However
the raw materials required had not been ordered and could not be obtained before the party.
Gus took an inventory of the available supplies and found the following:
Malt 90 units
Hops 40 units
Yeast 80 units
Soft Suds produces two types of pick-me-ups: light beer and dark beer, with the following
specifications:
Malt Hops Yeast
Light Beer 2 3 2
Dark Beer 3 1 5/3
Note that fractions (such as 5/3) may not be entered directly but must be approximated,
or calculated in an assignment. The light beer brings $2.00/gallon profit, the dark beer
$1.00/gallon profit.
3.1 Problem
Assuming that Comp Sci students will buy whatever is made, formulate the linear program
Gus must solve to maximize profits, and solve it using GAMS.
Problem 3 Page 2
