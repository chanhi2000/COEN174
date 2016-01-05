[COEN174] week03

## ENTITY-RELATIONSHIP DIAGRAM
- **ex**. *senior deign projects *

![ex-sendes](img/[COEN174]week3a-diagram1.png)


## BEHAVIOR-BASED MODELS
- [ERD](#entity-relationship-diagram) describes objects and their relationships
- [DFD](#data-flow-diagram) describes how data is transformed
- neither of these describes the **behavior**
- **two examples**:
    - state transition diagrams [STD]
    - sequence diagrams [UML]
- **ex** STD: COPIER

![copier](img/[COEN174]week3a-diagram2.png)


## CH.7 MAINPOINTS
- high-level vs. low-level design
- architectural styles
- UML class diagrams


## WHAT IS DESIGN?
- requirements are the “what”; design is the “how”
- design is the process of **taking a problem** and **coming up with a solution** that meets established professional practices.
> **engineering** = putting science into practice paying attention to efficiency, economy, and safety. 

 

## LEVELS OF DESIGN
- **architectural design**
    - high-level design
    - describing the major components
- **detailed design**
    - low-level design
    - describing modules, clauses, functions, etc.
- in theory, each design decision should relate to one module and/or one requirement
- in practice, this does not happen, so we will use TRACEABILITY TABLES
- **ex**: TRACEABILITY TABLE

![ex-traceability-table](img/[COEN174]week3a-diagram3.png)


## SOFTWARE ARCHITECTURES
- describes how the s/w is put together or structured
- high-level view of the system
- may not show all components or connections for simplicity
- allows a complex system to be viewed as a whole


## ARCHITECTURAL STYLES
- each style conjures up mentally a picture of what the structure of the system is
- three C’s of architectural styles
    - **components**: things that do the work
    - **connectors**: transport between components 
    - **constraints**: limits on the number and/or type of connectors or components to achieve the style.


## DATA-CENTRIC ARCHITECTURES

![ex-dca1](img/[COEN174]week3b-diagram1.png)
> **repository**: CLIENTs are active; DATA are passive
> **blackboard**: CLIENTs are passive; DATA are active

- **COMPONENTS**: clients & data store
- **CONNECTORS**: need/writes to data store
- **CONSTRAINTS**: clients are independent
- **GOOD**: easy for clients to come and go
- **BAD**: single point of failure

![ex-dca2](img/[COEN174]week3b-diagram2.png)￼

## DATA-FLOW ARCHITECTURE 
- **test ex**. UNIX SHELL

![ex-unix](img/[COEN174]week3b-diagram3.png)￼

```bash
$  grep pattern file |grep pattern | sort| l less &
```

- **COMPONENTS**: filters
- **CONNECTORS**: pipe
- **CONSTRAINTS**: filters are independent
- **GOOD**: 
    - reusability / flexibility
    - concurrency is easy   
    - is this needle?
- **BAD**:
    - translator filter needed if filters do not speak same language
    - NOT GOOD for incremental updates  (why? this style takes a transformational view/approach to date


## LAYERED ARCHITECTURES
- each layer provides services to the layer above
- **lower layers** are closer to the machine
- **higher layers** provide more abstraction

![ex-os](img/[COEN174]week3c-diagram1.png)￼￼￼

- **ex**. OS

![ex-os](img/[COEN174]week3c-diagram2.png)￼￼


- **ex**. ISO/OSI 


![ex-iso](img/[COEN174]week3c-diagram3.png)￼


- **COMPONENTS**: LAYERS
- **CONNECTORS**: layer transitional calls between layers
- **CONSTRAINTS**: communicable with layers below you
- **GOOD**: naturally supports abstraction reusability
- **BAD**: performance penalty when crossing layers

## CALL AND RETURN

![ex-call-and-return](img/[COEN174]week3c-diagram4.png)￼

- **COMPONENTS**: functions
- **CONNECTORS**: function calls
- **CONSTRAINTS**: stack-board


## OBJECT-ORIENTED ARCHITECTURE
- **COMPONENTS**: objects/methods
- **CONNECTORS**: messages

- OBJECT-ORIENTED TERMINOLOGY
    - **object**: an instance of a class
    - **class**: a data type that provides both attributes and operations on those attributes
    - **e.g.**

    ![ex-tt](img/[COEN174]week3c-diagram5.png)￼

    
    > **objects** communicate by sending messages; a message consists of the name of the operation to invoke (i.e., the method), the destination object, any `parameters  w.resize(2)` “messages invoke methods”


## INHERITANCE
- an ability of a subclass to reuse or have access to all attributes and operations of its parent(s)
- under the idea of subclassing, classes fall into a hierarchical relationship
- **ex.**

![ex-inherit1](img/[COEN174]week3c-diagram6.png)￼


- A SUBCLASS MAY 
    - **keep** existing behavior
    - **add** behavior
    - override behavior
- BUT MAY NOT 
    - **remove** behavior
- **ex.**:

![ex-inherit2](img/[COEN174]week3c-diagram7.png)￼

￼
- **ex.**: *binomial class*

![ex-inherit2](img/[COEN174]week3c-diagram8.png)￼


- **BAD**: objects must know the identity of another object in order to communicate with it (HIGH / TIGHT COUPLING)
- **CONSTRAINT**: objects are responsible for maintaining the integrity of its representation through encapsulation.





