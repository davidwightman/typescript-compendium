# null coalescing operator

The nullish coalescing operator (??) is a logical operator that returns its right-hand side operand when its lef-handside operand is null or undefined, and otherwise returns its left-hand side operand

```
const foo = null ?? 'default string';
console.log(foo);
// expected output: "default string"

const baz = 0 ?? 42;
console.log(baz);
// expected output: 0
```
