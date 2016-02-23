# week07

## TYPES OF TESTING
- #### ACCEPTANCE TESTING:

    done before official acceptance by the customer (white / black) (validation / verification / both?)
- #### CONFORMANCE TESTING:

    meeting standard requirements
- #### CONFIGURATION TESTING:

    testing across different platform.
- #### PERFORMANCE TESTING:

    testing the non-functional requirements
- #### STRESS TESTING:

    testing for gradual degradation under increasing workload


## GENERATING TEST CASES
- #### FROM INTUITION:

    no guidance, just experience
- #### FROM SPECIFICATION:

    [black box testing](https://en.m.wikipedia.org/wiki/Black-box_testing). (validation / verification / both?)
- #### FROM CODE:

    [(white / glass) box testing](https://en.m.wikipedia.org/wiki/White-box_testing)  (validation / verification / both?)
- #### FROM EXISTING CASES:

    regression testing.

    > **MIDTERM**: what’s the difference between white box testing and glass box testing?  => NONE


## BLACK BOX TESTING
- **what is it?**:
    - testing done without knowledge of the implementation.
    - testing done at the level of the specification
    - **key idea**: generate equivalent test cases by considering which test cases are equivalent
- #### EQUIVALENCE CLASS PARTITIONING:
    - **motivation**: eliminate redundant test cases
    - **reason**: save time and compute effort
    - **idea**: partition the input into equivalence classes and use a representative of each class for test.
    - each class is equivalent as far as test is concerned
    - a representative of each class is used for testing
    - **ex**: Application that makes recommendation based on age
￼
- #### BOUNDARY VALUE ANALYSIS
    - **goal**: improve EQUIVALENCE CLASS PARTITIONING by selecting the most appropriate test inputs.
    - **rationale**: In reality, if we look at historical data, many errors occur when checking the endpoints of a range.
    - **idea**: pick as test cases the boundary, boundary+1, and boundary–1.
    - **EX**: Application that makes recommendation based on age (again)
￼
    - **EX**: Application requires a user name of only letters and at most eight characters.
        - **Q**: What are some good test cases using EQUIVALENCE CLASS PARTITIONING and BOUNDARY VALUE ANALYSIS
        - **A1**: consider first the length of the string.
        ![]()
        - we should strings of length 0,1,2,7,8,9 to isolate behavior, we should check just legal strings.
        - **A2**: now, we can consider the content of the string.
        ![]()

## WHITE BOX TESTING
- #### CODE COVERAGE
    - in white box testing, we have knowledge of the code, so let’s USE it!
    - We want **good code coverage** from our test suite.
    - THE BETTER the code coverage, THE MORE TEST CASES required, but THE BETTER our perception of quality.
- #### LOGICAL PATH
    - Ideally, we want all possible paths through the code to be executed.
    - for programs with loops, the number of paths is ∞.
    - we can deal with this problem by limiting loops to at most one iteration
    - for each binary decision, there are 2 POSSIBLE PATHS
    - IN THE WORST CASE, a program with a decisions has 2n possible paths.
    - **ex#1**.
    ![]()
    - **ex#2**.
    ![]()
￼

- #### LINEAR INDEPENDENT PATHS
    - not all paths are linearly independent in that some are combinations of other paths
    - ex
    ![]()

    - **Q**: What is the number of linearly independent paths?
    - **A**: It’s the **cyclomatic complexity**.
￼
<diagram11>


