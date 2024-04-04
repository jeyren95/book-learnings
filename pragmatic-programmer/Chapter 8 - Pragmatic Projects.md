# 41. Pragmatic Teams
- include automation
  - assign a team member to be a tool builder (e.g. writing makefiles, shell scripts, editor templates, utility programs etc)
  - ensures consistency and accuracy since everyone will be using the same templates and tools

# 42. Ubiquitous Automation
1. Shell scripts

2. Cron jobs

3. Makefiles to compile projects
- can add in hooks to generate code for us
- able to run regression tests automatically

4. Maintaining internal websites for documentation
- documentation generated from code should be published on the website without any human interaction

# 43. Ruthless Testing
## What to test
1. Unit testing
- ensures that the individual modules are working properly

2. Integrated testing
- ensures that major subsystems of the application are working properly

3. Performance/stress testing
- e.g. CPU usage, RAM usage etc

4. Usability testing

## How to test
1. Regression testing
- compares the output from the current test with previous values
- ensures that bugs fixed today did not break things that were fixed yesterday

2. Test the tests
- deliberately insert bugs that break the system to see if these bugs are caught by the tests

3. Testing thoroughly
- high test coverage does not mean that the tests are comprehensive
- ensure that the tests written covers the different states of the component

## When to test
- test as soon as production code exists
- however, for tests the require special setup (e.g. performance testing), can test weekly/monthly

## Rule of thumb
- if a bug exists, make sure to write tests to account for it

