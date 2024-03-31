# 21. Design by Contract
- technique that focuses on documenting and verifying the responsibilities of software routines (i.e. methods, functions)

## Documenting
1. Preconditions
- what must be true in order for the routine to be called

2. Postconditions
- what must be true after the routine is called

3. Invariants

## Verifying
- when any of the conditions are not met, we can raise exceptions or terminate the program

## Implementating DBC
1. Inheritance in OOP
- to ensure that the subclass is really "a-kind-of" the base class, the contract can be specified in the base class
- the sub class may accept a wider range of inputs, BUT must at the very least, accept the same inputs as the base class

2. Polymorphism in OOP

3. Use comments for languages that do not support DBC

# 23. Assertive Programming
- assertions check for things that should never happen

# 25. Resource Allocation
- whichever routine is responsible for allocating a resource should be responsible for deallocating it