```js
let condition = false;
let result = '';

switch (condition && true) {
  case true:
    result = 'condition is true';
    break;
  case false:
    result = 'condition is false';
  default:
    result = 'condition is not boolean';
}

console.log(result);
```
this code has a logic error

illustrates the perils of switch/casing

https://javascript.info/switch

https://goo.gl/gZYg9y