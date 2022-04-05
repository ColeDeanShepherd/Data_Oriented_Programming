# Software Engineering Advice

## Getting an interview
* Open-source projects
* Networking
* Applying for jobs
* Practicing interview questions
  * Leetcode

## Being Interviewed
* Communicate your thought process
* Start with simple brute-force solution, then refine.
* Don't forget edge cases
* Have questions for the interviewers

## Working on a team professionally
* Workflow
  * Come up with goals
  * Break down goals into hierarchical tasks
  * Prioritize tasks
  * Schedule tasks
    * Sprints/agile
  * Pick a task
    * Highest-priority
    * Maybe also pick a backup task to help avoid task fatigue
    * Assign to yourself & set in progress
  * Plan the task
    * Technical design docs (TDDs)
      * Background
      * Goals & non-goals
        * KPIs
      * Functional & non-functional requirements
      * Possible solutions
        * Design "ideal" solution, irrespective of current state of application
        * Determine where to draw the line in terms of how close to get to the "ideal" solution given the current state of the application.
        * Tradeoffs
      * Test plan
      * Metrics/logging/alerts/dashboards
      * Deployment/migration plan
      * Estimated timeline
      * FAQ
      * Open questions
      * Future work
      * Resources
  * Do the task
    1. Create branch
    2. Create failing tests verifying requirements & calling into skeleton implementation
      * Arrange/Act/Assert
    3. Write simplest possible implementation to make tests pass. If test is too simple, implementation will be too simple - improve test.
    4. Refactor
    5. Review your own code
    6. Create PR
    7. Get code reviews & address feedback
      * Anticipate comments others might have on your PR, and add explanations as comments to your source code.
      * There will almost always be feedback. Don't take it personally. Gently push back if you disagree.
      * Don't get too personally attached to your code - it might be re-written or removed in the future.
      * Re-test code!
    8. Update branch with changes from production if necessary
      * Resolving merge conflicts
    9. Merge PR
  * Document the task
  * Deploy the task
    * Update task in project management software & mark as completed
  * Fix bugs
    * Bugs are inevitable
    * Add a failing regression test
    * Fix bug, make sure test succeeds.
    * If adding a regression test takes a lot of effort & you're confident in your fix, ship the fix before the regression test.
* Reviewing others' code
  * set aside time to review code every day
  * put 100% effort into reviewing code as well
  * Look more for high-level issues than nitpicks. If you have nitpicks, preface them as nitpicks.
  * Don't take it personally if the PR author doesn't implement your suggestions.
* Code conventions
  * Just adopt the team's code conventions. Hopefully you have an automatic linter so you don't need to think about it.
* Other
  * Recommend daily journaling
    * Of tasks completed (unless your project management software suffices)
    * Things you did well
    * Things to improve on

## Mental/physical health
* Take breaks (during a work day, also vacation time)
  * Pomodoro technique
* Get enough sleep
* Don't skip meals
* Don't sit all day - get up from time to time, or use a standing desk.
* Exercise is great for both physical & mental health
* You may not want to do every task, but try to find something to motivate you in every task, like:
  * The end result
  * Applying a new technique
  * Trying to write really high quality code
  * Doing something quickly
* Software engineering is HARD. You will make mistakes. Strive to do your best & learn from your mistakes.
* Don't take code reviews personally.
* Don't lash out at co-workers - be pleasant to work with.
* You will have ups and downs.
* Step away and cool down if you get frustrated.

## Data-oriented Programming
* Programming is all about transforming data.
  * Computers simply transform & move around data.
  * Everything a computer stores is data
  * Code is data.
  * Code specifies algorithms which transform data.
  * The same data can be represented in many ways.
  * Each representation can have different strengths and weaknesses regarding storage space, performance for certain queries, etc.
  * The same data may be represented in multiple ways in a program to service different use-cases.
* Data
  * Bits & bytes
  * Integers
  * Floating-point numbers
  * Characters & strings
  * Enumerations
  * Arrays
  * Tuples
  * Records
  * Sum types
  * Structs
  * Classes
* Data Structures
  * Arrays
  * Linked Lists
  * Stacks
  * Queues
  * Hash Tables/Sets
  * Trees
    * Binary search tree
  * Heaps
  * Graphs
  * Enums
  * Tuples
* Databases
  * Relational
  * Non-relational
  * Why use them?
* Compression & decompression
* Serialization & deserialization
  * Binary
    * Protobuf
  * JSON

## Algorithms
  * Performance
    * Big O notation (runtime, storage)
  * Sorting
    * Bubble sort (just as an example)
    * Quick sort
    * Merge sort
  * Search
    * Binary search
    * Depth-first search
    * Breadth-first search
  * Algorithm Techniques
    * Brute-force
    * Divide-and-conquer
    * Search
    * Recursion
    * Dynamic Programming

## Performance
  * Caches
  * Bottlenecks
  * Death by 1000 cuts
  * Profiling
  * Choosing algorithms
  * Avoid premature optimization

## How computers work
* Physical components
  * CPUs
    * Caches
    * Multi-core
    * Better at branching than GPUs
  * GPUs
    * Massively parallel
    * Not great at branching
  * RAM
  * Storage
* Operating system concepts
  * Threads
  * Processes
  * Sockets
  * Files
  * Containers

## Programming paradigms
* Object-oriented programming (OOP)
  * Classes
  * Public/protected/private
  * Inheritance
  * Polymorphism
* Functional programming
  * Lambdas
  * Pure functions
  * Side-effects
* Declarative programming

## Parallelism and concurrency
* Parallelism
  * CPU cores, threads, processes
* Concurrency
* Asynchronous tasks
* Synchronization primitives
  * Mutex
  * Reader/writer locks
* Deadlocks
* Shared memory vs message passing
* Actor model
* Optimistic & pessimistic locking

## Automated testing
* Unit tests
* Dependency injection
* Mocks
* Regression tests
* Refactoring code without introducing bugs
  * Add extensive tests for existing code
  * Refactor
  * Fix tests if necessary
  * Ensure tests still succeed

## C#
* LINQ
* Generics
* Enumerables
* Tasks & async/await
  * Task vs ValueTask
    * ValueTask is more efficient if the task completes asynchronously most of the time, and you don't need to await the task more than once.
* Interfaces
* Classes
* Structs
* Records
* Nullable types
* Static classes
* Attributes
* Reflection
* Garbage collection
* Gotchas
  * Don't pass exception to `throw` when re-throwing - it changes the call stack.

## Error handling
* Exceptions
  * try/catch/finally
* Return values
* Optional type
* Result type
* Logging

## Clean code
* Write high-level comments
* Use consistent naming conventions
* Keep functions small
* Optimize for readability, not writability.
* Give each piece of code a single responsibility.
* Dependency injection
* Avoid magic literals
* Think with separate levels of abstractions
* DRY
* Should be testable

## Using source control
  * Commits
  * Branching
  * Pulling & pushing
  * Merging
  * Pull requests
  * stashing

## Security
* Don't trust the client
* Any program users have access to can be hacked
* Hashing
* SQL Injection

## Software Engineering Process
1. Define goals
2. Create work items
3. Prioritize work items
4. Pick a work item to work on
5. Draw line for MVP
6. Write tests for requirements

## Requesting data
* Flexible query language would be nice

## Databases
* Make automatic backups!
* Delete rows in batches from live OLTP tables.
* Before running a `DELETE`, do a `SELECT` to preview the changes you're going to make.

## Project management
* You will probably always have more work in the backlog than you can realistically handle. Prioritize!
* Ship early, ship often.

## When adding a feature, keep in mind.
* Implementation in an ideal world.
* Current state of application and how big of a bridge you'd need to build to reach the ideal implementation.
* Automated/manual testing
* Where to draw the line for the MVP
* Logging & metrics & alerts & dashboards
* Limiting unbounded growth
* Dynamic configuration

## Clean Code
* Optimize for code readability, not necessarily writability.
* Try to keep code reading like English

## Other topics
* Finite state machine
* String interpolation
* Regex
* Machine learning
  * Neural networks
* Parsing
  * Lexing
    * Tokens
  * Parsing
    * Syntax trees
  * Context-free grammars
* REST APIs
* Cloud computing
* Debugging
  * Logging & telemetry & metrics
  * Debugger

## Other
* Keep main branch working, only update main branch through PRs, only allow PRs to merge if all tests pass.
* Use CI with automated test runs.
* Save ad-hoc queries into a repository if they're non-trivial.
* Use logging & telemetry to get an insight into production systems without using a debugger.
* No one is perfect. You are going to make mistakes. It's OK, just learn from them.
* Get enough sleep.
* Recognize burnout ahead of time.
* Invest in automation.
* When investigating a live issue, first try to mitigate the issue, then try to understand and fix the cause.
* Always assume server can die at any point during a request. You have to handle that.
* Prefer idempotent requests.

## Resources
* https://github.com/mtdvio/every-programmer-should-know
* https://www.cs.usfca.edu/~galles/visualization/Algorithms.html
* https://fsharpforfunandprofit.com/posts/13-ways-of-looking-at-a-turtle-3/