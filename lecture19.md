# Lecture 19 Whitebox testing
__what are definitions of different white box criteria, pros and cons, identify pros and cons what are test requirements for different test criteria, “tell me what are the branch testing requirements”, figuring out which testing criteria are weaker or stronger than others__
# Statement Coverage
C = executed statements / statements
# Branch Coverage
Tests branches in program
C = number of traversed branches / number of edges
# Basic Condition Coverage
Tests truth values assumed by basic conditions
C = number of boolean values assumed by all basic conditions / number of boolean values of all basic conditions
- does not reveal faults in branches 
# Branch and Condition Coverage
Test requirements: Branches and truth values assumed by basic conditions
# Compound Condition Coverage
All possible combinations of basic conditions
## Example
((((a || b ) && c ) || d ) && e)
2^5 test requirements
# Short Circuit operators
adv: less tests needed
dis: lots of analysis and pre processing
# Modified Condition/Decision Coverage (MC/DC) 
- MC/DC criterion requires that each basic
condition be shown to independently affect
the outcome of each decision.
- For each basic condition C, there are two
test cases in which the truth values of all
conditions except C are the same, and the
compound condition as a whole evaluates
to True for one of those test cases and
False for the other
# Path Coverage
__path adequacy__ requires each path in program to be
exercised by at least one test case
- basis path coverage
    - find paths that do not overlap
    - build test cases that cause each independent edge to overlap
    - want to cover every edge
    - aren't covering all combinations, save time
- loop coverage
    - all test cases must execute the loop from 0 to n times
# Data flow Coverage Criteria
- test definitions (d) and uses (u) of variables
Test requirements: sets of du pairs with respect to variable v  
- def of v is a reference to v where value of v is cahnged (assignement, input)
- a use v is a reference to v where value of v is fetched but not changed
- a def-clear subpath for a definition of v and a use of v is a subpath in the CFG between d and u on which v is not redefined
1. All defs
    - Test requirements: For each definition of each variable, at least
a du pair containing that definition
2. All uses
    - Test requirements: For each definition, a def-clear path from the
definition to all uses
3. All du paths
    - Test requirements: For each definition and each use of each
variable, all def-clear paths from the definition to the use