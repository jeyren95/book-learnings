# Summary
This chapter talks about being proactive while coding - always thinking critically about the code, and seeking ways to improve it

# 31. Programming by Coincidence
- refers to the act of relying on luck and accidental successes, instead of programming deliberately

## How to program deliberately
1. Document your assumptions
- people operate with many assumptions in mind, but such assumptions are rarely documented
- this can cause conflicts to occur between different developers

2. Rely only on reliable things
- do not depend on assumptions or accidents

3. Don't just test your code, test your assumptions as well
- write assertions to test your assumption that certain edge cases will never happen

4. Don't be a slave to history
- don't let existing code dictate the state of future code

# 32. Algorithm Speed
## Estimating using Big-O notation
- O() notation refers to asymptotic time complexity --> how the runtime of an algo grows as the input size grows 

1. Simple loops = O(n)
2. Nested loops = O(m * n)
3. Binary search = O(log n)
4. Divide and conquer = O(n log n)
5. Combinatoric

## Testing estimates
- run the program with varying input record counts
- plot the results 
- deduce the running time with the shape of the curve

## Factors that affect the need to optimize
1. Size of input sets
- it is possible that an insertion sort may perform as well as quicksort for a small input set

2. Setup cost

3. Be wary of pre-optimization
- make sure that algorithm is really the bottleneck before actually going ahead to optimize it

# 33. Refactoring
- refers to the act of rewriting, reworking, and re-architecting code

## When to refactor
1. Violation of DRY principle
2. Non-orthological code design
3. Outdated knowledge
4. Performance

## How to refactor
1. Don't refactor while adding new functionality at the same time
2. Ensure the presence of good tests before refactoring, and run the tests often
3. Take short, deliberate steps 

# 34. Code That's Easy to Test
## Unit testing by testing against contract
- write test cases that ensure the code meets the contract, and promises its functionality over a wide range of test cases and boundary conditions

## Testing in production
1. Log files containing trace messages

2. Hot-key sequence
- when a combination of keys is pressed, a diagnostic control window pops up, displaying status messages etc

3. Include a built-in web server
- allow users to see internal status, log entries, and maybe even have a debug control panel

