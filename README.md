# Software Engineering Advice

## Topics for getting a Software Engineering Job
* Getting an interview
  * Open-source projects
  * Networking
  * Applying for jobs
  * Practicing interview questions
    * Leetcode
* Interviewing
  * Communicate your thought process
  * Start with simple brute-force solution, then refine.
  * Don't forget edge cases
  * Have questions for the interviewers
* Programming is all about transforming data.
  * Computers simply transform & move around data.
  * Everything a computer stores is data.
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
* How computers work
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
* Algorithms
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
* Compression & decompression
* Performance
  * Caches
  * Bottlenecks
  * Death by 1000 cuts
  * Profiling
  * Choosing algorithms
  * Avoid premature optimization
* Machine learning
  * Neural networks
* Databases
  * Relational
  * Non-relational
  * Why use them?
* Garbage collection
* Regex
* Serialization & deserialization
  * JSON
* Programming paradigms
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
* Finite state machine
* String interpolation
* Parallelism and concurrency
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
* Parsing
  * Lexing
    * Tokens
  * Parsing
    * Syntax trees
  * Context-free grammars
* Automated testing
  * Unit tests
  * Dependency injection
  * Writing testable code
  * Regression tests
  * Refactoring code without introducing bugs
* REST APIs
* C#
  * LINQ
  * Generics
  * Enumerables
  * Tasks & async/await
  * Interfaces
  * Classes
  * Structs
  * Records
  * Nullable types
  * Static classes
  * Attributes
  * Reflection
* Error handling
  * Exceptions
    * try/catch/finally
  * Return values
  * Optional type
  * Result type
  * Logging
* Working on a team
  * Coming up with goals
  * Breaking down goals into tasks
  * Prioritizing tasks
  * Sprints/agile
  * Writing technical design docs
  * Using source control
    * Branching
    * Pulling & pushing
    * Merging
      * Resolving merge conflicts
    * Pull requests
  * Code reviews
    * Don't take it personally
    * Look more for high-level issues than nitpicks
  * Code conventions
    * Just adopt the team's code conventions. Hopefully you have an automatic linter so you don't need to think about it.
* Clean code
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
* Cloud computing
* Debugging
  * Logging & telemetry & metrics
  * Debugger
* Mental/physical health
  * Take breaks (during a work day, also vacation time)
    * Pomodoro technique
  * Get enough sleep
  * Don't skip meals
  * Don't sit all day - get up from time to time, or use a standing desk.
  * Exercise is great for both physical & mental health
  * Find something to motivate you in every task
    * The end result
    * Applying a new technique
    * Improving your code quality
    * Doing something quickly
  * Software engineering is HARD. You will make mistakes. Strive to do your best & learn from your mistakes.
  * Don't take code reviews personally.
  * Don't lash out at co-workers - be pleasant to work with.
  * You will have ups and downs.
  * Step away and cool down if you get frustrated.
* Resources
  * https://github.com/mtdvio/every-programmer-should-know
  * https://www.cs.usfca.edu/~galles/visualization/Algorithms.html
  https://fsharpforfunandprofit.com/posts/13-ways-of-looking-at-a-turtle-3/
* Security
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

## TDD Process
1. Define requirements
3. Create failing tests verifying requirements & calling into skeleton implementation
4. Write simplest possible implementation to make tests pass. If test is too simple, implementation will be too simple - improve test.
5. Refactor

## C#
* Don't pass exception to `throw` when re-throwing - it changes the call stack.

## SQL
* Delete rows in batches from live OLTP tables.
* Before running a `DELETE`, do a `SELECT` to preview the changes you're going to make.

## Databases
* Make automatic backups!

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

## Helpful Tools
* Timer system app
* VS Extensions
    * Create instance & set all fields