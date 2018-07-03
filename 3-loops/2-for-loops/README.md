For loops in JavaScript are [__syntactic sugar__](https://www.quora.com/What-is-syntactic-sugar-in-programming-languages). 

[For loops](https://www.w3schools.com/js/js_loop_for.asp) do not handle __var__ and __let__ as you would expect.  So we have an example for each:
* [Lexical Scope in For Loops](./for-loop-var) - using __var__ 

### [From StackOverflow](https://stackoverflow.com/questions/8109509/in-which-situations-should-i-use-while-loops-instead-for-loops-in-javascript#)
> (This will soon get closed as too subjective, or moved to another forum, but anyway...)

> Obviously any for loop can easily be rewritten using "while". But given the syntax of:

> for ([initialization]; [condition]; [final-expression])
that is used by the for loop it is obviously very well suited to situations where there is some simple initialisation and a simple end-of-iteration update or counter increment. Putting all of the loop control logic right there in the loop's opening statement makes it easy to see at a glance what makes the loop tick.

> With a while loop the end-of-iteration processing generally has to happen at the bottom of the loop's body, so it's harder to see at a glance how the loop works, but also that is much more suited to the situation where you have to perform a number of calculations to decide whether to keep the loop going.

> Of course you can shove multiple statements in a for loop initialisation or final-expression by separating them with commas, but if that is anything more complicated than i++, j++, k-- it quickly gets too messy for my taste and a while loop would be a better choice.

### [From w3schools](https://www.w3schools.com/js/js_loop_for.asp):

> The for loop has the following syntax:

```js
for (statement 1; statement 2; statement 3) {
    code block to be executed
}
```

> Statement 1 is executed (one time) before the execution of the code block.

> Statement 2 defines the condition for executing the code block.

> Statement 3 is executed (every time) after the code block has been executed.

simulate while loop with for loop