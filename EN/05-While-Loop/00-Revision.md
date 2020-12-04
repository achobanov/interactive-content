[slide]
# Revision

## For-Loop
We can repeat a code block using a `for` loop:
```js live
for (let i = 65; i <= 90; i++) {
  let letter = String.fromCharCode(i);
  console.log(letter);
}
```

We can read a sequence of `n` numbers from the console this way:
```js
let n = Number(input.shift());
for (let i = 1; i <= n; i += 1) {
   let num = Number(input.shift());
}
```

## Increment and Decrement Operators
Increments or decrements its operand by 1.

Both operators are supported in two forms: the postfix increment operator, `x++`, `x--`, and the prefix increment operator, `++x`, `--x`.

Prefix operator means increment / decrement the value before using it, while the postfix operator means increment / decremenet the value after using it.

```js live
let i = 3;
console.log(i);
console.log(i++);
console.log(i);
```

```js live
let i = 3;
console.log(i);
console.log(++i);
console.log(i);
```
[/slide]