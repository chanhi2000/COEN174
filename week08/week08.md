# week08

## BRANCH COVERAGE
- also called DECISION COVERAGE or EDGE COVERAGE
- ensure that each branch will be taken and not taken if we look across all tests.


## STATEMENT COVERAGE
- also known as NODE COVERAGE
- ensure all statements will be executed at least once 

## FUNCTION COVERAGE
- each function (executed) covered at least once.
￼

OTHER WAYS OF FINDING ERRORS

## INSPECTIONS / REVIEWS
* A REVIEW is simply any process that uses humans to examine a software artifact for the purpose of finding errors
* A INSPECTION is just a more detailed review
* A WALKTHROUGH is just an explanation of the artifact


## TESTING VS. REVIEWS / INSPECTIONS
- finding errors is CHEAPER using TESTING, but fixing them is EXPENSIVE.
- TESTING works only on code, but REVIEWS work on any artifact
- TESTING catch errors “LATE”, whereas INSPECTIONS / REVIEWS catch errors “EARLY”
- TESTING is more “OBJECTIVE”, whereas REVIEWS are more “SUBJECTIVE”


## FORMAL METHODS
- prove the program correct
- usually only practical for small portions of the code


## STATIC ANALYSIS TOOLS
- examine the source good looking for errors
- results must be examined by hand
- ex. LINT, gcc -wall

