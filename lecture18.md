# Lecture 18 Black Box
__what is black box, key characteristics,  general process for blackbox testing, two specific instantiations, category partition method, systems as finite state machines, use FSM to automate testing of software__
## Black Box Testing is
based on functional specification of software
scales because we can use different techniques at different granularity
## Characteristics
- Does not consider implementation structure
- Focus on domain of input data
## General Approach to BB Testing
1. __Equivalence Partitioning__
    - take all possible inputs and partition into groups
2. Identification of __boundary values__
    - identify specific values in the groups to test
3. Generation of test cases
    - combine values for all inputs
### Example
- Identify EP and BV for a program that inputs an integer and prints its value
    - EP: non-integers, negative integers, positive integers
    - BV: max_int, min_int, max_int+1, max_int-1, min_int-1, min_int+1, -1, 0, 1

## Category Partition Method
1. Identify independent testable features
2. Identify categories for parameters
3. Partitioning the categories into choices
4. Identify constraints among choices
5. Produce and evaluate test case specs
    - choices are elemental cases to be combined by picking a choice per category
    - a combination identifies a partition of the input space
6. generate test cases from specs
    - generation of test scripts from specs can b e semi automated
    - degree of automation depends on how formal the description is