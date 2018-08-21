simulated for loop with "let":
```js
let result = '';

for_let: {
  let stepper_1 = 0;
  {
    let stepper_2a;
    {
      stepper_2a = stepper_1;
      if (stepper_2a < 2) {
        result += stepper_2;
        stepper_2a++;
      } else {
        break for_let;
      };
    };
    let stepper_2b;
    {
      stepper_2b = stepper_2a;
      if (stepper_2b < 2) {
        result += stepper_2;
        stepper_2b++;
      } else {
        break for_let;
      };
    };
  };
};

console.log(result);
```

[pytut link]()

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
