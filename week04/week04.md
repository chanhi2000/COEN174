# **week04**

## EVENT-BASED ARCHITECTURE
- **COMPONENTS**: whatever you like (objects, functions, layers, …)
- **CONNECTORS**: 
    - **Explicit Invocation**: whatever you had before 
    - **Implicit Invocation**: events
-  When a change occurs to a component, it  announces an event (broadcasts)
- other components that are listening for (registered for) an event have their event handlers invoked
- **CONSTRAINT**: the announcer does not know who receives the event or in what order multiple components receive it
    - **e.g.**: twitter, web browser (JavaScript), window system
- **BAD**: debugging of event based / asynchronous code is hard
- **GOOD**: A component does not have to know the identity of another component in order to communicate with it (LOW / LOOSE COUPLING)
 
#### EXAMPLE: EBA
- **problem**: a system  with 2 components:
    - *V*  represents a set of vertices
    - *E*  represents a set of edges 
- **requirements**: 
    - when an edge is added to *E*, its vertices must be added to *V*
    - when an vertex is deleted from *V*, the incident edges are deleted from *E*.
- Let’s call this relationship *G*.
- In the future, we might need to modify *G* to *G’*. Also, we might add a new component C that keeps track of the number of vertices in *V*.
- ###### SOLUTION #1: Encapsulation
![soln1](img/[COEN174]week4a-diagram1.png)
    - [–] access to *V* and *E* is not allowed; 
    - [–] accesses  must go through *G*
    - [–] adding *C* requires modifying *G*
    - [+] modifying *G* to *G’* 
    - [+] reuse of *V* and *E*

- ###### SOLUTION#2: Hardwiring
![soln2](img/[COEN174]week4a-diagram2.png)
    - [–] adding *C* requires modifying *V*
    - [–] extending *G* to *G’* is hard
    - [–] reuse of *V* and *E* is poor

- ###### SOLUTION#3 Events
![soln3](img/[COEN174]week4a-diagram3.png)
    - [+] reuse of *V* and *E* is good
    - [+] adding *C* is easy (no modification required)
    - [–] modifying *G* to *G’* is hard (it’s distributed still)

* ###### SOLUTION#4: Mediator
![soln4](img/[COEN174]week4a-diagram4.png)
    - [+] reuse of *V* and *E* is good
    - [+] easy to add *C*
    - [+] extending *G* to *G’* is easy (all-in-one place)

## CLASS-BASED MODELING
- XML has a class diagram 
- #### example#1:
![ex01](img/[COEN174]week4c-diagram1.png)
- #### example#2:
![ex02](img/[COEN174]week4c-diagram2.png)
- #### example#3:
![ex03](img/[COEN174]week4c-diagram3.png)
    - 0 = *zero*
    - 1 = *one*
    - 1..4 = *one, two, three, four*
    - \* = *0..*
    - \+ = *1..*
- #### example#4:
![ex04](img/[COEN174]week4c-diagram4.png)

- #### example#4: (layout improved)
![ex04b](img/[COEN174]week4c-diagram5.png)

- #### example#5: 
![ex05](img/[COEN174]week4c-diagram6.png)
- #### example#6:
A symbol table consists of symbols. Each symbol has a name. Example symbols include variables, types, functions, procedures, and literals. A function returns a value of a given type. Procedure are simply functions that do not return values. Each function also has variables. Example type include basic types such as integer and real, as well as, derived types such as arrays. Each array type has a base type and a length. Draw a UML class diagram to represent the symbol table and all of its symbols. 
![ex06](img/[COEN174]week4c-diagram7.png)