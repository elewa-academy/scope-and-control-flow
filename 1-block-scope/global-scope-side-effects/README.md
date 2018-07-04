```js
// polution in the global space
{
    var lexical_1 = "lexical";
}
{
    var lexical_1 = "overwritten";
}

// no polution
{
    let block = "block";
    block
}

{
    let block = "kcolb";
    block
}
```