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
access to *V* and *E* is not allowed; accesses  must go through *G*
    - [–] adding *C* requires modifying *G*
    - [+] modifying *G* to *G’* 
    - [+] reuse of *V* and *E*
- ###### * SOLUTION#2: Hardwiring
    - [–] adding C requires modifying V
    - [–] extending G to G’ is hard
    - [–] reuse of V and E is poor