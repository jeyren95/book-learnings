# Summary
This chapter talks about how to make <b>reversible</b> decisions, so code can stay flexible.

# 26. Decoupling and the Law of Demeter
## Minimize coupling
1. Organize code into modules

2. Limit the number of module interaction, and beware of how the modules are interacted
- traversing relationships between objects can lead to highly dependent relationships

## Symptoms of highly dependent relationships
1. Simple changes to a module propagates through unrelated modules

2. Developers who are afraid to change code because they are afraid of what might be affected

## The Law of Demeter for Functions
Any method of an object should only access objects that are:
- defined within the current class
- arguments passed into the method
- created within the method
- globally available

# 27. Metaprogramming
- involves moving details out of code, so we don't run the risk of breaking the system every time we change code to accomodate a change in business logic

## Dynamic configuration
- make our systems highly configurable rather than highly integrated
- use metadata to describe the configuration options (e.g. screen colors, thread management, DB products, middleware technology etc)

## Benefits
1. Forces decoupling

2. Application is highly customizable
- since the application is built for the general case, and accepts metadata depending on the needs of the application

3. Able to implement different projects using the same application engine

# 28. Temporal Coupling
- when designing architecture or writing a program, things tend to be linear
- but this leads to temporal coupling (i.e. coupling in time)
- we need to allow for concurrency and think about decoupling any time or order dependencies

## Workflow
- use UML activity diagrams to capture workflows, and identify activities that can be done in parallel

# 29. It's Just a View
## Publish/Subscribe mechanism
- utilizes events to minimize coupling between components
- objects only register to receive events that they need, and should never be sent events that they don't need
- this mechanism serves as the basis for the MVC concept

## MVC 
- separates the model from both the GUI and the controller that manages the view

1. Model
- data itself

2. View 
- displays the model's data and sends new data to the controller to be forwarded to the model

3. Controller
- intermediary between the model and view
- forwards new data from the view to the model (i.e. publishes events to the model)
- forwards data from the model to the view to be displayed (i.e. publishes events to the view)

### Benefits
1. Support multiple views of the same model
2. Ability to use commmon controllers on different data models

### Limitations
- despite the decrease in decoupling between listeners and event generators, there is still some coupling involved
- both need to agree on common interface definitions and calling conventions when sending/receiving data




