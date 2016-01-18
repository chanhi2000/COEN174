# **week02**
## PRIORITIZING REQUIREMENTS
- **ex**:
    - absolutely necessary: **critical**
    - highly desirable: **recommended**
    - possible: **suggested**

## ANALYTICAL HIERARCHICAL PROCESS
- more rigorous approach
- **key idea**: compare components / requirements parallels


#### EXAMPLE: [AHP](#analytical-hierarchical-process)
- 3 major requirements (R1, R2, R3)
- R1 is 4x as important as R2
- R1 is 2x as important as R3
- R3 is 2x as important as R2
- **Q**: *What is the overall importance of each?* [on MIDTERM]
![ahp-example](img/[COEN174]week2a-diagram1.png)


## REQUIREMENT: DEFINITIONS, PROTOTYPING, REVIEWS
- customer involved? **YES**
- definition involves writing up the requirements
- if we need clarification, we can prototype
- prototypes are common for user interface
    - **low-fidelity**: papers/cards
    - **high-fidelity**: mockup in a browser / Visual Basic
- results go through a review


## REQUIREMENT SPECIFICATION
- customer involved? **NO**
- this is what customer will sign OFF on
- in some organizations
    - **requirement documentation [HI]**: written more for **customers**
    - **requirement specification [LO]**: written more for **technical folks**
    - some specification languages are even executable


## REQUIREMENT AGREEMENT
- customer involved? **YES**
- customer signs, marking end of requirement engineering


## ANALYSIS MODELS
- "formal model" is used to write up the results of analysis
- #### structured analysis (1960s)
- #### unified modeling language (1990s)
- **difference**:
    - **structured analysis** considers data and operations separately whereas **object-oriented analysis** considers them together

#### SCENARIO-BASED MODEL
- user satisfaction is key to the success of a system
- therefore, models involving the user are usually constructed first
- **a user case** describes how a “user” interacts with the system to accomplish some goal or perform some action
- #### **example**: user case diagram
    
    ![user-case](img/[COEN174]week2a-diagram2.png)
    
    ![user-case](img/[COEN174]week2a-diagram3.png)
- The diagram itself is not enough
- we also need **narrative**
    - **name**
    - **actor(s)**
    - **pre-condition**
    - **post-condition**
    - **goal**
    - **steps** in a typical system
    - **exceptions**


- **example**:
    ```
    - name: login
    - pre-condition: none
    - post-condition: user authenticated
    - goal: authenticate user
    - steps:    
        1. enter username
        2. enter password
        3. information is submitted
        4. user taken to landing screen
    - exceptions: username/password incorrect -> retry
    ```

## ACTIVITY DIAGRAMS
- shows the dynamic behavior of the system (or part of the system)
- looks much like a flowchart, but also has notation for concurrency
- #### **example**: baking a cake
![baking-a-cake1](img/[COEN174]week2c-diagram1.png)
![baking-a-cake2](img/[COEN174]week2c-diagram2.png)
- ####**example**: login
![login](img/[COEN174]week2c-diagram3.png)

## SWIMLANE DIAGRAMS
- activity diagrams but with responsibilities assigned
- #### **example**: baking a cake (again)
![baking-a-cake3](img/[COEN174]week2c-diagram4.png)

## DATA-BASED MODEL
- identify data and their relationships
- a data object is simply composite information
- #### **example**:
    - **object** = person
    - **attribute** = first name, last name

## DATA-FLOW DIAGRAM (DFD)
- models how data is transformed as it flows through the system
- decomposed hierarchically
- #### **example:** a compiler
![dfd-compiler](img/[COEN174]week2c-diagram5.png)

## ENTITY-RELATIONSHIP DIAGRAM (ERD)
- entities = objects
- #### **example**: generic one
![erd1](img/[COEN174]week2c-diagram6.png)

- #### **example**: book
![erd2](img/[COEN174]week2c-diagram7.png)

- #### **example**: school
![erd3](img/[COEN174]week2c-diagram8.png)