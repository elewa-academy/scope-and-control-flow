simulated for loop with "let":
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

[pytut link](https://goo.gl/AGJdUi)

[parsons practice](https://elewa-academy.github.io/parsons/examples-to-study/scope-and-control-flow.html#sim-for-loop-let)

___

for loop with "let":
```js
let result = '';

for (let stepper = 0; stepper < 2; stepper++) {
    result += stepper;
};

console.log(result);
```

[parsons practice](https://elewa-academy.github.io/parsons/examples-to-study/scope-and-control-flow.html#for-loop-let)

[pytut link](https://goo.gl/mmZ8jY)