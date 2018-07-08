# For Loops

For loops are very similar to while loops. Deciding when to use one or the other is a strategic question:  For loops can be simpler when you know how many times the loop will be executed, like when you have an array with x items. 


### Index:
* [For Loop Syntax](#for-loop-syntax)
* [For or While?](#for-or-while)
* [Block Scoping](#block-scoping)
* [Resources](#resources)

___

## For Loop Syntax

__[From w3schools](https://www.w3schools.com/js/js_loop_for.asp)__:
> The for loop has the following syntax:
```
for (statement 1; statement 2; statement 3) {
    code block to be executed
}
```
> Statement 1 is executed (one time) before the execution of the code block.  
> Statement 2 defines the condition for executing the code block.  
> Statement 3 is executed (every time) after the code block has been executed.  


___

## For or While?

__[From StackOverflow](https://stackoverflow.com/questions/8109509/in-which-situations-should-i-use-while-loops-instead-for-loops-in-javascript#)__
> (This will soon get closed as too subjective, or moved to another forum, but anyway...)  
> Obviously any for loop can easily be rewritten using "while". But given the syntax of:  

```
for ([initialization]; [condition]; [final-expression])
```
>that is used by the for loop it is obviously very well suited to situations where there is some simple initialisation and a simple end-of-iteration update or counter increment. Putting all of the loop control logic right there in the loop's opening statement makes it easy to see at a glance what makes the loop tick.  

> With a while loop the end-of-iteration processing generally has to happen at the bottom of the loop's body, so it's harder to see at a glance how the loop works, but also that is much more suited to the situation where you have to perform a number of calculations to decide whether to keep the loop going.  

> Of course you can shove multiple statements in a for loop initialisation or final-expression by separating them with commas, but if that is anything more complicated than i++, j++, k-- it quickly gets too messy for my taste and a while loop would be a better choice.  

> -- nnnnnn

___

## Block Scoping

A big Gotcha! is how JavaScript implements for loops when you use _let_ to declare the incrementing variable in your for loop definition.  

__For__ loops in JavaScript could be considered [syntactic sugar](https://www.quora.com/What-is-syntactic-sugar-in-programming-languages), meaning you can replicate their exact behavior using simpler language features.    Because it's always best to relate new knowledge to previous understanding let's demonstrate block scoping in __for__ loops by replicating it using _while_ loops and code blocks:
* [For loop with __var__](./for-loop-var)
* [For loop with __let__](./for-loop-let)

___

### Resources

* Example Step-Throughs:  [For loop with __var__](./for-loop-var), [For loop with __let__](./for-loop-let)
* [MDN on For Loops](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Statements/for)
* [Video + Article](https://www.kirupa.com/html5/loops_in_javascript.htm)
* [Same challenge, different loops](https://gist.github.com/colevandersWands/a25901206cf04f266afde7da8b7aa152)




___
___
### <a href="http://elewa.education/blog" target="_blank"><img src="https://user-images.githubusercontent.com/18554853/34921062-506450ae-f97d-11e7-875f-6feeb26ad72d.png" width="100" height="40"/></a>

