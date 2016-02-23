# week06

## OBJECT-ORIENTED METRICS
- object oriented metrics typically differ from traditional metrics
- rather than just focusing on complexity, they rather try to measure characteristics such as abstraction and reuse
- We will discuss one set of metrics: CHIDAMBER AND KEMERER {CK}


## WEIGHTED METHODS PER CLASS
- Take your favorite complexity metric, apply it to each method in a class, and add them up
- The higher the number, the more complex your class is (and therefore harder to understand, modify, …)


## DEPTH OF INHERITANCE TREE
- length of the longest path from root to a leaf.
- **HIGH NUMBER**:
	- [+] more reuse
	- [–] more complexity
- **LOW NUMBER**:
	- [–] less reuse
	- [+] less complexity


## NUMBER OF CHILDREN
- number of subclasses of a parent class
- HIGHER NUMBER:
	- [+] greater reuse
	- [–] dilution in abstraction


## LACK OF COHESION OF METHODS
- Consider a class with methods $$m_1,\cdots,m_n$$ and instance variable uses $$I_1,\cdots,I_n$$
- $$P$$: set of ALL method that have non common instance variable
- $$Q$$: set of all method that have

$$
\text{LCOM}=\begin{cases}|P|-|Q|,&|P|>|Q|\\Q,&\text{otherwise}\end{cases}
$$

- EX.
    - $$I_1=\{a,\:b,\:c,\:s\}$$
    > (i.e. method $$m_1$$ uses variables $$a$$, $$b$$, $$c$$, $$s$$)

    - $$I_2=\{d,\:b,\:z\}$$
    - $$I_3=\{f,\:h,\:w\}$$
    - Consider each pair
        - $$(I_1,\:I_2)\to{Q}$$
        - $$(I_1,\:I_3)\to{P}$$
        - $$(I_1,\:I_3)\to{P}$$
    - $$\text{LCOM}=|P|-|Q|=(2)-(1)=1$$
    - **SIDENOTES**: DISTANCE METRIC
    $$
    1-\frac{A\cap{B}}{|A\cup{B}|}
    $$
￼
**EXAM: identify name one or two metrics and their jobs, traditional metrics and what they try to measure**


## SKIPPING CH9. BECAUSE
- coding style, commenting, debugging…


## CH10. MAINPOINTS
- what is the point of testing?
- how can we “test” the program?
- what are validation and verification?
- code coverage for testing?


## DIFFERENCE BETWEEN TEST AND QUALITY ASSURANCE:
there is none.


## QUALITY
- CLEARLY, we want our software to be high quality.
- **QUALITY ASSURANCE** refers to activities to measure and improve quality
- **QUALITY CONTROL** refers to activities to verify the quality


## WHAT IS QUALITY?
- **QUALITY** can be defined as conformance to specifications and serving a purpose
	- conformance to specifications: **VERIFICATION**
	- serving a purpose: **VALIDATION**


## V PROCESS MODEL
- EX (classical phase of software engineering)
![fig01](week05/[COEN174]week6b-fig01.png)￼
- **VERIFICATION** *ANSWERS THE QUESTION*
    - “did we build the **product right**?
- **VALIDATION** *ANSWERS THE QUESTION*
    - “did we build the **right product**?


## LACK OF QUALITY
- Quality is lacking due to errors
- A **fault** or **defect** is a condition that may cause a failure
- A **failure** is the inability of a system to perform according to specifications
- note that a fault does not have to be in code
- faults can also exist in requirements and design documents
- The later an error is found, there expensive it is to fix.


## FINDING ERRORS
- we can find faults in many ways, only one which is **testing**
- Testing involves **running the program within the purpose of finding errors**
- It is the most common, easiest, and “cheapest” way.
- It is also the only dynamic way (i.e. running the program)
- There are also many static ways to find errors, but these are typically harder and more “expensive”
- We can do **inspections**, **reviews**, or even use formal methods to prove code correct
- We can also do a static analysis of the code.


## TESTING
- What is testing?
	- **definition #1**: to find defects / errors / faults
    - Testing can only show the presence of defects not their absence
    - In other words, testing cannot be used to prove a program correct.
    - **WHY?** exhaustive testing is simply not possible.
    - **EX**: Program to find quadratic $$ax^2+bx+c$$. We have three inputs: $$A$$, $$B$$, and $$C$$. Let’s assume each input is a 32-bit quantity Also assume that we can one test in $$1\:\text{ns}$$. We would need 2.5 trillion years to test all possible inputs
    - **definition #2**: to provide a general assessment of quality.
    - The better the test cases, the better the assessment.

- who does the testing?
	- **programmers** do unit testing
	- **testers** do system and integration testing.
	- **users** do alpha and beta testing
		- **alpha**: in-house
		- **beta**: not in-house
		- both types of acceptance testing
- what is tested?
    - **unit testing**: test an individual unit (a handful of functions or classes that ideally exhibit **high cohesion**)
	- **integration / system testing**: all components to test a complete system
- when to stop testing?
	- NEVER
	- slightly more practical answer: WHEN ALL BUGS ARE FOUND
	- more practical answer: WHEN WE EXECUTE ALL THE TESTING
	- Problem Discovery
￼	![fig02](week05/[COEN174]week6c-fig01.png)
    > A better approach: FAULT SEEDING
￼	![fig03](week05/[COEN174]week6c-fig02.png)
    - **ASSUMPTION**: distribution across code /functionality of seeded faults matches closely that of actual faults
        - **Q**:  How might we know the latter.
        - **A**:  Metrics to infer which modules are more complex and therefore prone to errors
            - INTUITION INEXPERIENCE
            - HISTORICAL KNOWLEDGE OF THE CODE (including that of off -the-shelf code)
