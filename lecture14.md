# Lecture 14: Cleanroom
__Lecture 14: cleanroom software model, what was so different, what were properties, what made it unique, what things you do with coding and design, can run code, black,clear,whitebox testing, statistical based testing, tradeoffs of cleanroom, why, when, when not to__
## Two Principles
Software development based on mathematical principles
Testing based on statistical principles
1. Defect prevention rather than defect removal (any defects not prevented should be removed). This first priority is achieved by using human mathematical verification in place of program debugging to prepare software for system test. 
2. To provide valid, statistical certification of the software’s quality through representative-user testing at the system level. The certification takes into account the growth of reliability achieved during system testing before delivery.

## Characteristics
1. Spend time and money upfront to prevent defects
2. use statisitical methods to ensure quality
3. formally state requirements and prove compliance
4. specs, dev, certification may be done by separate teams
5. small teams
6. incremental dev under statistical quality control
7. software development based on mathematical principles
8. testing based on statistical principles
## Cleanroom methodology
1. Incremental development under statistical
process control
2. Function-Based Specification, Design,
and Verification
3. Correctness verification
4. Statistical testing and software
verification
### Three Box Models
1. Begin with external view (black box)
    - view of object that hides data implementation and process implementation
    - describes how a system responds to stimuli
2. transform into a state macine (state box)
    - show data implementation but hides process implementation
    - describes how state information is transformed, represented as FSM
3. fully develop into a procedure (clear box)
    - shows both data implementation and process implementation
    - may introduce new black boxes defining major operations
- Stepwise Refinement of Boxes to code
    - define black boxes
    - translate black to state
    - design set of clear boxes to match state boxes
    - expand clear boxes into lower level designs
    - expand low level designs into code
### Correctness Verification
- Code Reviews
- Formal inspection / Fagan Inspection
    - each activity has entry / exit criteria
    - perform inspection at each point
    - formal and structured meetings (author, reader, reviewers, moderator)
    - process: code is read out loud, defended by author, critiqued by reviewers
    - time consuming, but very effective
### Statistical testing and software verification
Each increment of compiled functionality is statistically tested to
- ensure that it meets the quality standards
- certify a level of reliability
- provide feedback
- Reliability Testing
    1. What are the features / states
    2. How will they be used and interact
    3. create formal model of this
    ![alt text](https://i.gyazo.com/20536a338634a503b0f22023dd8ebcd3.png)
    4. sample model to choose test cases
    5. run test cases
    6. measure passing versus total
Metric: __Mean Time To Failure (MTTF)__
calculated in (MR)^c where M = initial mttf, R = Observed Effectiveness Ratio for improving MTTF with software changes, c = releases
