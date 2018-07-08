https://goo.gl/AGJdUi
```js
let result = '';

{
  let stepper_1 = 0;
  {
    let stepper_2 = stepper_1;
    while (stepper_2 < 2) {
      result += stepper_2;
      stepper_2++;
    };
  };
};

console.log(result);
```

https://goo.gl/mmZ8jY
```js
let result = '';

for (let stepper = 0; stepper < 2; stepper++) {
    result += stepper;
};

console.log(result);
```