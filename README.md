# Scope & Control Flow


In __Variables & Types__ you learned how to track the state of your application step-by-step.  In __Scope & Control Flow__ you will learn how to read and manipulate program state in order to make decisions within your code's run-time execution. Code is not smart, but the people who make it can be.  

At this stage you want to think of the code you write as simply an automation of the decisions you would make yourself if you had to do a task by hand. The basic units of __strategy__ in JavaScript are:
* _Conditional Branching_ - Performing different actions depending on some condition (if, else, else if, switch/case).
* _Repetition_ - Performing small, repetitive tasks until a larger goal has been accomplished (loops: while, for, do while).

You are now learning more complex code constructs, but the heart of your program is still variables and the values that they store. In order to successfully use either of these strategies you must be comfortable interpreting and tracking your application's state as your code grows more complex.   

With the introduction of Control Flow, you will have to think about how and when you access variables.  This is a complex topic that you will continue to explore through the rest of this course, especially when you begin to explore __separation of concerns__ and __functional vs Object Oriented__ programming.  But for now you will only need to think about these three aspects of variable access:
1. _Reading_ - What is the purpose of reading this variable?  You will typically find there are two reasons to read from a variable: to make a decision based on it's contents (conditionals, loops), or to use it's value to generate a new value.
2. _Modifying_ -  What is the purpose of modifying this variable?  Variable modifications store information generated during the program's runtime for later use.  figure out something else to say here.
3. _Scope_ - In which scope is a variable accessed?  Was it accessed in the same scope it was created?  

After understanding these different access cases, you will be prepared to start thinking about [the __roles__](http://saja.kapsi.fi/var_roles/stud_vers/stud_Pascal_eng.html) that variables can play in program execution.  While there are 10+ distinct roles a variable can play in your code (depending on who you ask), we will be focusing on only 2 for now:
1. _Meaningful Variables_ - These are variables that store values related to the purpose of your code.  These values will show up directly in the final result of your code and may be mapped onto the real-world. A variable is probably a __meaningful variable__ if it is mentioned in the prompt, console.logged'd at the end of your program, or is used as part of the final result. 
2. _Utility Variables_ - These are variables that store information necessary for successful execution, but that will not show up anywhere in the final result. Examples include: "i" in for loops, arrays or objects containing pieces of the final result, or booleans used for decision making.



### Index
* [Learning Objectives](#learning-objectives)
* [Specifications](#specifications)
* [Resources](#resources)

---

## Learning Objectives

__Study Techniques:__
* Stepping through run-time behavior
* Diagramming flow control


__JavaScript:__
* Block Scope:
  * let & const
  * (we'll see lexical scope in the next chapter)
* Truthy & Falsey
* Conditionals:
  * if, else, else if
  * switch/case
* Loops:
  * while
  * for
  * do while
  * "for ... of" (objects)
  * "for ... in" (arrays)
* Error Handling:
  * throw
  * try/catch/finally




__Programming Skillzz:__
* Stepping Through Execution:
  * Predicting & indicating changes in scope
  * Evaluating expressions by hand
  * Predicting which line will execute next
* Variable Roles:
  * Meaningful variables
  * Utility variables
* Strategy before Code:
  * Understanding the differences between control flow structures
  * Choosing the right control flow structure for your use case
  * Creative incrementing in for loops
* Using nested flow control:
  * Conditionals in conditionals
  * Loops in loops
  * Conditionals in loops
* Using nested data structures:
  * Arrays in Arrays
  * Objects in Objects
  * Arrays in Objects
  * Objects in Arrays
* Errors:
  * Syntax errors 
  * Logic errors
  * Runtime errors


  
[TOP](#scope--control-flow)

---

## Specifications

Continue working your way through your preferred on-line tutorial, regularly tying what you learn there back to these step-through examples. Not all of the examples will have complete step-through diagrams provided, moving forward we'll just be filling in the tricky bits. Stay engaged with these examples like you did in __Variables & Types__, it's not enough to understand them!  You'll know you've got them down when you can predict PythonTutor's next steps:
1. [Block Scope](./1-bloc-scope)
2. [Conditionals](./2-conditionals)
  * if/else/if else
  * switch case
3. [Loops](./3-loops)
  1. while
  2. for
  3. do while
4. [Error Handling](./error-handling)
  1. Throw
  2. Try/Catch

_Sketching execution:_
Nothing that you learned in __Variables & Types__ about sketching run-time behavior has changed, but there will be 2 new things to be aware of:
1. __Block Scope__: You will now need to indicate in your sketch when a new scope has been opened or closed and illustrate which scope a variable belongs to.  There are examples for how to do this in [Block Scope](./1-block-scope).
2. Keeping track of the previous, current and next lines to execute will become much more involved.  With conditional checks and loops you will need to think a little harder to trace JavaScript's journey through your code.
3. You will now be expected to indicate a variable's __role__ and why it is accessed.  It is enough to mention this in the text above your sketch, there is no need to include this info in the diagram itself.



[TOP](#scope--control-flow)

---

## Resources

__Tutorials and the Like:__
* [JavaScipt.info](https://javascript.info): 
  * 2.10 -> 2.13 
  * 4.1 -> 4.2 
  * 5.6 -> 5.9 ()
  * 8.1 -> 8.2 (error handling)
* Practical JavaScript:
  * [Controlling Logical Flow](https://shawnr.gitbooks.io/practical-introduction-to-javascript/content/controlling-logical-flow/)
* MDN: 
  * [Conditionals](https://developer.mozilla.org/en-US/docs/Learn/JavaScript/Building_blocks/conditionals) 
  * [Looping Code](https://developer.mozilla.org/en-US/docs/Learn/JavaScript/Building_blocks/Looping_code)
  * [Error Handling](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Control_flow_and_error_handling)
* learn-js.org: 
  * [Operators](http://www.learn-js.org/en/Operators)
  * [Conditions](http://www.learn-js.org/en/Conditions)
  * [Loops](http://www.learn-js.org/en/Loops)



  

#### Tools:
* [Realtime flow-chart generator](https://bogdan-lyashenko.github.io/js-code-to-svg-flowchart/docs/live-editor/index.html):
  * For visualizing flow control, the logical structure & progression of your code.
  * Copy paste code into this site to automatically generate flow control visualizations.
* [PythonTutor for JavaScript](http://www.pythontutor.com/javascript.html#mode=edit):
  * For building your Notional Machine: visualizes how the JavaScript engine steps through code, deals with variables, and handles function execution. 
  * Copy your code into the text area and click "visualize execution".  Step through line by line with the "forward" button.  
* [Parsonizer](https://elewa-academy.github.io/parsons/):
  * Randomizes the lines in your code, you have to put them back in order (tabs count!).  This will help you learn syntactic structures & develop your logical problem solving skills by studying quality examples.
  * Copy paste your code into the text box and click the magic button.  Click "get feedback" to grade your answer.


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
* __let__ in a for loop:
  * [Step-through example](./3-loops/2-for-loops)
  * [Noraesae](https://noraesae.net/2017/09/14/lexical-scope-in-js-for-loop/)
* Truthy & Falsey:
  * [A video](https://www.youtube.com/watch?v=J4N6ETFpdkA)
  * [Deep dive](https://www.sitepoint.com/javascript-truthy-falsy/)
  * [All things truthy](https://developer.mozilla.org/en-US/docs/Glossary/Truthy)
  * [All things falsey](https://developer.mozilla.org/en-US/docs/Glossary/Falsy)
  * [Some Gotchas](https://codeburst.io/javascript-truthy-values-dont-always-equal-true-8afaf071a4a6)
* Syntax vs Runtime vs Logic errors:
  * [Syntax vs Logic - in cinema](https://www.youtube.com/watch?v=tV0tQisuxPo)
  * [MDN - What went wrong?](https://developer.mozilla.org/en-US/docs/Learn/JavaScript/First_steps/What_went_wrong)
  * [TutorialsPoint](https://www.tutorialspoint.com/javascript/javascript_error_handling.htm)
  * [On Quora](https://www.quora.com/What-is-the-difference-between-a-logical-error-and-a-semantic-error)



[TOP](#scope--control-flow)

___
___
### <a href="http://elewa.education/blog" target="_blank"><img src="https://user-images.githubusercontent.com/18554853/34921062-506450ae-f97d-11e7-875f-6feeb26ad72d.png" width="100" height="40"/></a>

