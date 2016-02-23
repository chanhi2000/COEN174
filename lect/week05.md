# week05

## CLASS-BASED MODELING
- EX.
![fig01](/[COEN174]week5a-fig01.png)

we want to add a new class, $$x5$$, with methods $$m1$$, $$m2$$, $$m3$$, $$m4$$, and a new method $$m8$$. How should we do this?
- **solution #1**:
![fig02](week05/[COEN174]week5a-fig02.png)
- **issue #1**: two copies of *m4*
- **solution #2**:
![fig03](week05/[COEN174]week5a-fig03.png)
- **issue #2**: turns a compile-time into a run-time error
- **solution #3**
![fig04](week05/[COEN174]week5a-fig04.png)
￼

## DESIGN CONCEPTS
- #### modularity
- #### abstraction
- #### refinement


## MODULARITY
- **what is it?**:

    dividing a system into independent components that can be independently managed/thought about
- **why?**:

    a monolithic system is two difficult to reason about as a whole
- **how does it work?**:

    consider two problems, $$P_1$$ and $$P_2$$. Let $$C$$ represent the complexity of each problem. What’s interesting is that. $$C(P_1+P_2)>C(P_1)+C(P_2)$$
- **TOO MANY MODULES** however leads to too much linkage between modules
- **TOO FEW MODULES** leads to too much complexity within each module.


## ABSTRACTION
- **what is it?**:

    the hiding of details to facilitate understanding
- **different types of abstraction**
    - **procedural**
    - **date**
        - control (i.e. event)


## REFINEMENT
- **what is it?**:

    method of design that uses a top-down strategy that successively reveals levels of detail
- also called *elaboration*
- **refinement** and **abstraction** are complementary in that refinement reveals levels of detail but steps at some point, where abstraction takes over.


## COHESION {CH}
- The degree of RELATEDNESS WITHIN a model, unit, or component
- A cohesion model should do one thing and do it well.
- cohesion helps us to understand and maintain software

> BECAUSE ALL RELEVANT COLD IS IN ONE LOCATION AND THERE IS NO NON-RELEVANT CODE TO CONFUSE THE DEVELOPER


## DIFFERENT TYPE OF COHESION
- #### COINCIDENTAL COHESION:
    - Two tasks (or ideas or pieces of functionality) are in the same module for no good or apparent reason
- #### LOGICAL COHESION:
    - Two tasks that related logically (do the same thing like CONVERSIONS or OUTPUT) are in the same module
- #### TEMPORAL COHESION:
    - Two tasks that occur near one another in time are in the same module
- #### PROCEDURAL COHESION:
    - occurs when two tasks that are always executed in the same order are in the same module
- #### COMMUNICATIONAL COHESION:
    - two tasks that rely on the same data structure are in the same module


## COUPLING:
- The degree of **LEVEL OF INTERCONNECTIVITY** (or **INTERDEPENDENCE**) among modules
- **LESS COUPLING** (or **LOWER** or **LOOSER COUPLING**) also helps software maintenance—how?
- **LESS COUPLING** means that changes are less likely to ripple through the system.

**BEST**: low COUPLING and high COHESION


## DIFFERENT LEVELS OF COUPLING
- #### DATA COUPLING
    - simple argument list of atomic values
- #### STAMP COUPLING
    * portions of data structures are passed as arguments
- #### CONTROL COUPLING:
    * a control flag is passed as an argument
- #### EXTERNAL COUPLING:
    * ties to input, output, other external device
- #### COMMON COUPLING:
    * access to a common, global data structure or variable
- #### CONTENT COUPLING:
    * one module just goes in and violates access control to access access data in another module


## METRICS
- we want our software to have certain quantities, whether explicitly specified or    not:
    - *maintainable*
    - *usable*
    - *reusable*
    - *flexible*
    - *adaptable*
    - *etc.*
- ALL OF THESE QUALITIES of software are hard to measure
- METRICS are a way of quantifying the qualitative
- To be useful, a metric should be:
    - simple to compute
    - intuitive
    - simple to understand
- Early metrics tend to be more low-level and code-oriented, whereas more recent metrics are more HIGH-LEVEL and DESIGN-ORIENTED


##TRADITION METRIC #1: Lines of Code
- **rationale**: more lines of code means more complexity or functionality
- It’s simple to compute and intuitive
- problem:
    - MORE LINES DOES NOT NECESSARILY IMPLY MORE COMPLEXITY
    - what exactly is a line of code?
        - comments?
        - blank lines?
- remember: developed in 60s for ASM language.


## TRADITIONAL METRIC #2: [ALSTEAD’S COMPLEXITY METRIC](https://en.m.wikipedia.org/wiki/Halstead_complexity_measures)
- developed in 1970s
- definitively code oriented
- **RATIONALE**:

    more operators and operands mean more complexity
- *operators* include:
	- $$+$$, $$–$$, $$/$$, $$*$$, $$\text{if}$$, $$\text{while}$$, $$\text{for}$$, $$\text{FUNCTION CALL}$$, …
- *operands* incldue:
	- variables, constants, strings, …
- **4 quantities**:
	- $$n_1$$: # of distinct operators
	- $$n_2$$: # of distinct operands
	- $$n_3$$: # total of operators
	- $$n_4$$: # total of operands
- **basic properties**:
	- $$n=n_1+n_2$$: *program vocabulary*
	- $$N=N_1+N_2$$: *program length*
	- V = N (log n)    program volume
- **REALITY**:

    measures lexical (textual) complexity, not structural complexity


## ## TRADITIONAL METRIC #3: [MCCABE’S CYCLOMATIC COMPLEXITY](https://en.m.wikipedia.org/wiki/Cyclomatic_complexity)
- **RATIONALE**:

    complexity is more related to the structure of a program than to its text
- we need to use **FLOW GRAPHS**:
- EX.
![fig05](week05/[COEN174]week5c-fig01.png)
- TWO QUANTITIES
    - $$N$$: # of NODES (7 in ex.)
    - $$E$$: # of EDGES (8 in ex.)
- **FORMULA**:
    - $$C=E-N+2$$ (3 in ex.)
    - If $$P$$ represents # of binary predicate (decision) nodes, then $$C=P+1$$
    - From *Graph Theory*
        - $$C$$: # of REGION
    - **IDEA**:
        - more complicated control-flow means more COMPLEXITY
    - **GUIDELINES**:
        - $$1\sim10$$:	low-risk
        - $$11\sim50$$: indeterminate
        - $$>50$$: high risk


## ## TRADITIONAL METRIC #4: HENRY-KAFURA INFORMATION FLOW
- measures inter-module flow
- **RATIONALE**:

    It’s the connections between modules that result in complexity
- **RELEVENT QUANTITIES**:
    - $$\text{fan}_{\text{in}}$$: # of incoming piece of info
    - $$\text{fan}_{\text{out}}$$: # of outgoing piece of info
- $$C=(\text{fan}_{\text{in}}\cdot\text{fan}_{\text{out}})^2$$ of a module
- $$C_{\text{total}}$$: sum of individual complexity.

