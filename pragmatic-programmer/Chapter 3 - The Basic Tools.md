# 16. Power Editing
## Useful editor features
1. Configurable
- e.g. fonts, colors, window sizes, key-stroke bindings
- using key-stroke bindings for common editing operations is more efficient than using mouse

2. Extensible
- should be able to integrate new programming languages that come out

3. Programmable
- you should be able to program the editor to perform complex, multistep tasks

4. Programming language specific
- e.g. syntax highlighting, auto complete, auto indent, code boilerplate

# 17. Debugging
## Mindset
- try to discover the root cause of the problem, rather than just fixing the symptoms causing the problem

## Debugging strategies
1. Data visualization
- e.g. using a debugger that allows to visualize the state of program, and the relationships that exist between data

2. Tracing
- e.g. using print statements
- use tracing when time is a factor (e.g. in concurrent processes, real-time systems, and event-based applications)

3. Rubber ducking
- process of explaining the bug to someone else

# 20. Code generators
## Passive
- parameterized templates that generate a given output from a set of inputs
- helps to save typing

### Use cases
1. Create new source files
- e.g. producing templates, standard comment blocks etc

2. Performing one-off conversions among programming languages

3. Produce lookup tables and other resources that are expensive to compute at run time

## Active
- helps to follow the DRY principle

## Use cases
1. Generating struct code from the DB schema used

2. Communicating between different programming languages used in the same application
- each code base requires some info in common (e.g. data structures, message formats, field names etc)
- express such info in a language-neutral representation (e.g. JSON, XML), and generate the code for both languages 





