[COEN174] week01

## CLASSICAL PHASES OF ENGINEERING
- **requirement**:
    - define the problem
    - determine what must be done
- **design**:
    - define the solution
    - determine how the work will be done
- **implemenation**:
    - build the system according to established principles and guidelines
- **test**:
    - verify that the work was done correctly

## REQUIREMENTS
- these define and qualify what the system needs to do
- typically defined by the client (marketers, customers, users, etc.)
- in English, a requirement is something that absolutely must happen
- in engineering, it is negotiable and can be prioritized

## FUNCTIONAL REQUIREMENTS
- define what must be done
- usually be answered as true / false
- usually stated as "*the system will …* "

## NON-FUNCTIONAL REQUIREMENTS <a id="nfr"></a>
- define the manner in which the functional requirements need to be achieved
- usually assumed by a degree of satisfaction
- usually stated as "*the system will be …* “

## DESIGN CONSTRAINTS
- a lot like [NFR](#nfr)
- constraints the solution:
> e.g.  "must be written in Java" -> DC
> e.g.  "must be web-based"       -> DC 
> e.g.  "system msb be portable"  -> NFR

## HOW IS A SYSTEM DIFFERENT FROM A PROGRAM?
- complexity of actual code
- non-engineering aspects

## COMPLEXITY OF ACTUAL CODE
- “**breadth**" refers to number and variety of components
    - more major functionality
        - i.e.    browse webpages
        - i.e.    used e-mails
        - i.e.    edit webpates
    - more features with each function
        - i.e.    spam filtering
        - i.e.    spelling correction
    - more interfaces to features
        - i.e.    fetch mail from a different place
        - i.e.    export mail
    - more users
        - i.e.    novice users
        - i.e.    expert users
- “**depth**” refers to complexity and relationship among components
    - more layers of abstraction
    - more links between layers
    - more libraries & frameworks

## TECHNICAL CONCERNS
- What platform(s) will be used?
- What language(s) will be used?
- Is the DB required?
- Is it networked?
- Is a [configureation management system](https://en.m.wikipedia.org/wiki/Configuration_management) required?

## NON-ENGINEERING ASPECTS
- more people and resources to coordinate
- have people with different skills
- need to impose a team structure

## CH. 6: MAIN POINTS
- What are requirements?
- What are the steps in requirements engineering?
- What are informal and formal methods of gathering, describing and evaluating requirements?

## WHAT ARE REQUIREMENTS?
- Statements that describe what the system “should"/“must" do.
- They do not describe how the software is to be constructed. 
- Top reason for project failure: POORLY DEFINED REQUIREMENTS
- Top reason for project success: WELL-DEFINED REQUIREMENT
- If some requirements are missing, they are incomplete.
- If they are conflicting, they are ambiguous.
- The process of determining requirements is called “REQUIREMENT ENGINEERING”.

## REQUIREMENT ENGINEERING
- Talk to the customer about what they want
- End up with a formal document they can sign off.
- How do we get from one to the other: we use a PROCESS.

## (SOFTWARE) PROCESS
- A framework used to guide system development
- it includes…
    - tasks to be performed
    - sequencing of tasks
    - I / O
    - pre-conditions / post-conditions
- i.e. **classical phase of engineering**
![classical phase of engineering](img/[COEN174]week1b-diagram1.png)

- i.e. **requirements process**
![requirements process](img/[COEN174]week1b-diagram2.png)
    - **elicitation**: talk to the customers about what they want
    - **analysis**: go back and tabulate, sort, prioritise (i.e. analyse)
    - **definition**: write it up informally
    - **prototyping**: build a mock-up to get feedback
    - **review**: check it over

## WHY DO WE NEED REQUIREMENTS?
- for acceptance testing
- limit scope creep
- planning for training and support
- scheduling the project

## REQUIREMENT ELICITATION
- customers involved? **YES**
- talk to the customers about what they want
- focus on what (requirement), not how (design)

## HIGH-LEVEL REQUIREMENT
- deal with business concerns
- **communication skills** are important; many {RE} have business background
- **business opportunity**: need for s/w
- **justification**: how well s/w save/make money?
- **scope**: how much s/w will do?
- **constraints**: schedule/cost 
- **user characteristics**: who is using the system?

## LOW-LEVEL REQUIREMENT
- more technical than HIGH-LEVEL REQUIREMENT

![low-level requirement](img/[COEN174]week1c-diagram1.png)
> DIFFERENT SYSTEM = DIFFERENT REQUIREMENTS

- **physical environment**
    - Where will system run?: One location? / Several?
- **interfaces**
    - Where is the input going?: One system? / Several?
    - Where is the output going?: One system? / Several?
- **user**
    - Who will use the system?: Different type? Different skills?
- **Functionality**
    - What will it do? Constraints on time / space
- **Documentation**
    - What kind? How detailed?
- **Data**
    - Format? Persistent? Accuracy?
- **Resources**
    - What equipment and personnel are necessary?
- **Security**
    - Must access be controlled? data backed up?
- **Quality Assurance**
    - Will the system detect errors? Mean Time to Failure?

## REQUIREMENT ANALYSIS
- customers involved? **NO**
- organizing and prioritizing the data gathered during ELICITATION
- We will find that we are missing some information and other information is contradictory
- **Make assumptions** (based on experience), **document** them, and then **validate** them through prototypes.
