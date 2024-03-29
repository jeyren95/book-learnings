# 7. The Evils of Duplication
## DRY Principle - Don't repeat yourself
- every piece of knowledge should have a single representation within the system

## Preventing duplication
1. Multiple representations of information
- e.g. a class whose attributes mirrors the schema in the DB
- use a filter or code generator whereby the class is automatically generated from the DB schema

2. Code comments
- comments should represent the highest level of explanation
- code should represent the low level explanation
- avoids the problem where changing the code leads to the need to change the comments

3. Documentation
- code and documentation contain the representations of the same knowledge
- requirements change --> update documentation --> update code
- generate tests programmatically from the documentation itself

4. Common functionality needed across teams, but doesn't fall into an obvious area of responsibility
- can lead to such functionality being implemented many times
- active communication should be facilitated between developers

# 8. Orthogonality
## Benefits of independent components
1. Increased productivity
- changes are more localized, meaning development and testing time is reduced
- ability to combine components in ways that were not envisioned originally

2. Reduce risk
- isolation of broken code prevents other components from being affected
- less likely for a change to break other components

## Achieving decoupling
1. Each major infrastructure component should get a subteam
- e.g. DB, API, middlewares, UI
- for each change requested, how many people are required to be in the meeting?

2. Modular/Component-based/Layered system
- if a change in requirements is needed for a particular function, how many other modules are affected?

3. Write shy modules
- modules that do not reveal anything unnecessary to other modules
- e.g. if a change is needed in a object's state, get the object do it for you

4. Avoid global data
- referencing global data will tie your code to other parts that also share the data
- pass around context instead, by using the <b>singleton design pattern</b>

5. Avoid similar functions
- e.g. if you find that a group of functions are doing something similar, use the <b>strategy design pattern</b>

6. Testing + Bug fixing
- do you have to drag in a large percentage of the rest of the system to test this component?
- how localized is the bug fix?

# 9. Reversibility
- whatever mechanism is implemented, make it reversible

# 10. Tracer code
- applies to new projects, particularly when building something that has not been built before

## Benefits
1. Feedback is immediate

2. Users get to see something working early

3. Availability of an integration platform
- ability to add new pieces of code everyday, rather than a big bang integration

## Tracer code vs Prototyping
Tracer code                         
- trivial implementation of the final system    
- need to know how the application as a whole, hangs together
- lean, but complete and forms part of the skeletion of the final system

Prototyping
- explores a specific aspect of the final system
- throw away whatever you used to try out the concept, and recode it properly using lessons learnt
- generates disposable code


