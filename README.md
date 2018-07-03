# Scope & Control Flow


In __Variables & Types__ you learned how to track the state of your application step-by-step.  In __Scope & Control Flow__ you will learn how to read and manipulate program state in order to make decisions with your code. Code is not smart, but the people who make it can be.  

At this stage you want to think of the code you write as simply an automation of the decisions you would make yourself if you had to do a task by hand. The basic units of __strategy__ in JavaScript are:
* _Conditional Branching:_ Performing different actions depending on some condition (if, else, else if, switch/case).
* _Repetition:_ Performing small, repetitive tasks until a larger goal has been accomplished (loops: while, for, do while).

In order to successfully use either of these strategies you must be comfortable interpreting and using your application's state to make things happen.   

Now you will begin to use primitives and objects quite differently:
* objects (arrays, objects) will be used as data structures.  their purpose is to store and organize primitives
* primitives will be the main pieces in your program.  You will read them and operate on them to make decisions, and modify them to store information. 

Reading vs Writing to variables will serve different purposes.

### Index
* [Learning Objectives](#learning-objectives)
* [Specifications](#specifications)
* [Resources](#resources)

---

## Learning Objectives

__Study Techniques:__
* Stepping through run-time behavior
* Diagramming flow control
* Evaluating expressions by hand

__JavaScript:__
* Block Scope:
  * let & const
  * (we'll see var in the next step)
* Objects: "for ... of" loops
* Arrays: "for ... in" loops
* For loops:
  * (Used when you know how many times you'll want to repeat)
  * Incrementing counters
  * Decrementing counters
  * Creative counters
* While loops:
  * (Used when you know why you'll want to stop repeating)
* Truthy & Falsey



__Programming Skillzz:__
* Strategy before Code:
  * choosing the right structures
  * knowing what each one is used for
* Variable Roles:
  * 
* Tracking data structures
* Nested flow control:
  * Conditionals in conditionals
  * Loops in loops
  * Conditionals in loops
* Nested data structures:
  * Arrays in Arrays
  * Objects in Objects
  * Arrays in Objects
  * Objects in Arrays

  
[TOP](#javascript-fundamentals)

---

## Specifications

Take a look through these examples. Not all of the examples will have step-through diagrams provided, only when there is something you haven't learned how to sketch before like __scope__. So stay engaged with these examples, it's not enough to understand them.  You'll know you've got them down when you can predict PythonTutor's next steps:
1. [Block Scope](./1-bloc-scope)
2. [Conditionals](./2-conditionals)
  * if/else/if else
  * switch case
3. [Loops](./3-loops)
  1. while
  2. for
  3. do while

- - - - 

** should this be called 'roles'?
  or should it be split to two - before/after chunk
  how to handle this 
  introduce roles up front
    then introduce the roles as they are relevant

diagram that focuses on values
  - column per variable & structure
    ala changelog
  - track structures
  - track contexts & scopes
    how to differentiate scopes & contexts?
    and to relate vars that share
  - indicate if two vars point to same object
  steps go down
  only steps that effect variables show up

concrete diagram takes shape
  - cases to capture in examples
    let vs var (jit declaration)
    scope
    context
    obj vs var
  for each variable a column
  for each step a variable is modified
    the old value
    the operation
    the new value
  white-space sensitive
    mark that you've tabbed in
  and context sensitive
  to track
    scope where created
    scope where modified
    contexts - can't keep them from using functions

roles for this time around
  - define classifying questions
  constants
    - it is never modified
      ie. only appears on the right hand side of assignments
    const key word
  utilities (infrastructural?)
    - is modified
    - is not on the right hand side of result
      except control flows
    - defined in/for a loop's condition
  grey zone
    is there really one more category?
  ephemeral
    - on the right hand side of result
    - will not matter in a post-chunk test
    fix this name
  result (output?)
    - leaves the chunk
      ie. on the right of a return statement
        or can be put in an assert to validate a chunk
    best practice
      only put it on the left hand side of equal signs
    https://elewa-academy.github.io/Solution-Design/07-place-constraints/
    often a data structure

info must have per var
  role
  scope & context 
    created
    read
    modified
    how it got there
  when used in assignment happens
    right or left side?
    what's on the other side?
      this helps determine it's role

abstract diagram

assert.md moves in here
  https://learn.freecodecamp.org/javascript-algorithms-and-data-structures/debugging
    
  try-catch + console.assert
  chromedev console
  console methods
    assert
    error
  tddbin
    does it have a save feature

*** sajaniemi 2002: from sorva pg 42
	https://pdfs.semanticscholar.org/735e/1f2eedf0b178d27073bffacf04a92e1d31c6.pdf

```js
// reading or writing twice
let a = 9;
let b = a;
let c = a;
let a = b;
```

tracing technologies
	pytut
	roles
		create examples of each in js
		perhaps copy from
			https://en.wikibooks.org/wiki/A-level_Computing/AQA/Problem_Solving,_Programming,_Data_Representation_and_Practical_Exercise/Fundamentals_of_Programming/The_Role_of_Variables
			http://www.cs.joensuu.fi/~saja/var_roles/role_intro.html
	diagram
		try to emulate roles guy's visualization
	instructions
	examples

** find this paper
	Using Tracing and Sketching to Solve Programming Problems: Replicating and Extending an Analysis of What Students Draw

*** https://faculty.washington.edu/ajko/papers/Xie2018TracingStrategies.pdf

works cited
  cunningham
  sketches from 2018
  roles guy

basic debugging
	or not here?
	only in pytut & fcc up to now?
	https://learn.freecodecamp.org/javascript-algorithms-and-data-structures/debugging

concrete tracing. sorva pg 63

[TOP](#javascript-fundamentals)

---

## Resources

js.info: 2.10-2.13, 4.1-4.2, 5.6-5.9 

https://shawnr.gitbooks.io/practical-introduction-to-javascript/content/controlling-logical-flow/

http://www.learn-js.org/en/Operators
http://www.learn-js.org/en/Conditions
http://www.learn-js.org/en/Loops


for loop details: https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Statements/for

https://developer.mozilla.org/en-US/docs/Learn/JavaScript/Building_blocks/Looping_code

scopes in for loops: https://noraesae.net/2017/09/14/lexical-scope-in-js-for-loop/

* [Mapping Conditional Checks](https://github.com/elewa-academy/mapping-conditional-checks/settings)

Loops
  [Video + Article](https://www.kirupa.com/html5/loops_in_javascript.htm)

#### Tools:
* [PythonTutor for JavaScript](http://www.pythontutor.com/javascript.html#mode=edit):
  * For building your Notional Machine: visualizes how the JavaScript engine steps through code, deals with variables, and handles function execution. 
  * Copy your code into the text area and click "visualize execution".  Step through line by line with the "forward" button.  
* [Parsonizer](https://elewa-academy.github.io/parsons/):
  * Randomizes the lines in your code, you have to put them back in order (tabs count!).  This will help you learn syntactic structures & develop your logical problem solving skills by studying quality examples.
  * Copy paste your code into the text box and click the magic button.  Click "get feedback" to grade your answer.
* [Realtime flow-chart generator](https://bogdan-lyashenko.github.io/js-code-to-svg-flowchart/docs/live-editor/index.html):
  * For visualizing flow control, the logical structure & progression of your code.
  * Copy paste code into this site to automatically generate flow control visualizations.

Tricky Bits:
* JavaScript Types:
  * [Primitives vs. Objects](https://codeburst.io/javascript-data-types-explained-347555cd2d4d)
  * [List of them](https://www.w3schools.com/js/js_datatypes.asp)
  * [Type Coersion](https://javascriptweblog.wordpress.com/2010/09/27/the-secret-life-of-javascript-primitives/)
* Expressions vs. Operators:
  * (This is a tricky concept, it will make more sense after __Scope & Flow Control__)
  * Over Views:[dev.to](https://dev.to/promhize/javascript-in-depth-all-you-need-to-know-about-expressions-statements-and-expression-statements-5k2), [flaviocopes](https://flaviocopes.com/javascript-expressions/), [lib.ru](http://lib.ru/%3E%3C/JAVA/javascr/expr.html)
  * In Depth: [MDN](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Expressions_and_Operators), [2ality](http://2ality.com/2012/09/expressions-vs-statements.html)
  * Assignment vs Comparison: [Overview (study with PyTut)](https://www.quirksmode.org/blog/archives/2008/01/using_the_assig.html#link1), [This isn't just a JS thing](http://wiki.c2.com/?AssignmentVsEqualityOperator)
* Which Loop to use?
  * [So many of them!](https://www.hackreactor.com/blog/javascript-loops-difference-between-types-while-for-in) - [interactive examples](http://www.dofactory.com/tutorial/javascript-loops)
  * For's vs While's: [StackOverflow](https://stackoverflow.com/questions/39969145/while-loops-vs-for-loops-in-javascript), [TeamTreeHouse](https://teamtreehouse.com/community/why-use-while-loop-instead-of-for)
  * [While vs Do While](https://www.digitalocean.com/community/tutorials/using-while-and-do-while-loops-in-javascript)
* Truthy & Falsey:
  * [A video](https://www.youtube.com/watch?v=J4N6ETFpdkA)
  * [Deep dive](https://www.sitepoint.com/javascript-truthy-falsy/)
  * [All things truthy](https://developer.mozilla.org/en-US/docs/Glossary/Truthy)
  * [All things falsey](https://developer.mozilla.org/en-US/docs/Glossary/Falsy)
  * [Some Gotchas](https://codeburst.io/javascript-truthy-values-dont-always-equal-true-8afaf071a4a6)
* Looping Arrays:
  * [Map vs ForEach]()


[TOP](#javascript-fundamentals)

___
___
### <a href="http://elewa.education/blog" target="_blank"><img src="https://user-images.githubusercontent.com/18554853/34921062-506450ae-f97d-11e7-875f-6feeb26ad72d.png" width="100" height="40"/></a>

