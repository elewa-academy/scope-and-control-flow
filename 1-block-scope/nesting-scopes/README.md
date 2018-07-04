## Nesting Block Scopes





### Index:
* [Sample Step-Through](#sample-step-through)
* [More examples to study](#more-examples-to-study)

___

### Sample Step-Through

```js
let global_let = 'global let';
console.log('leaving global scope');
{
    console.log('entering block scope');
    var inner_var = 'global var';
    let inner_let = 'inner let';
    console.log('leaving block scope');
};
console.log('re-entering global scope');
inner_var = 'modified globally';
console.log('final state');
```

[PythonTutor link](https://goo.gl/TMzZRs)

___




___

### More examples to study


Very thorough example. ([PythonTutor link](https://goo.gl/qC9ppR)):
```js
let global_let = 'global_let';
var global_var = 'global_var';
{
    let b_1_let = 'b_1_let';
    var b_1_var = 'b_1_var';
    {
        let b_2_let = 'b_2_let';
        var b_2_var = 'b_2_var';

        global_let;
        global_var;
        b_1_let;
        b_1_var;
        b_2_let;  
        b_2_var;
    };

    global_let;
    global_var;
    b_1_let;
    b_1_var;
    // b_2_let;  // -> ReferenceError: b_2_let is not defined
    b_2_var;
};

global_let;
global_var;
// b_1_let;  // -> ReferenceError: b_1_let is not defined
b_1_var;
// b_2_let;  // -> ReferenceError: b_2_let is not defined
b_2_var;
```

___
___
### <a href="http://elewa.education/blog" target="_blank"><img src="https://user-images.githubusercontent.com/18554853/34921062-506450ae-f97d-11e7-875f-6feeb26ad72d.png" width="100" height="40"/></a>

