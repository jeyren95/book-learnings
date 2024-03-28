# Chapter 2 - A Pragmatic Approach
## 7. The Evils of Duplication
### DRY Principle - Don't repeat yourself
- every piece of knowledge should have a single representation within the system

#### Preventing duplication
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

## 8. Orthogonality
