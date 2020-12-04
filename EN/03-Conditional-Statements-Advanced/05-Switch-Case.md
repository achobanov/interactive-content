[slide]
# The Switch-Case Statement

The switch-case condition works as a sequence of if-else blocks. 

Whenever the work of our program depends on the value of one variable, instead of making consecutive conditions with `if-else` blocks, we can **use** the conditional `switch` statement. 

It is being used for **choosing between a list of possibilities**. 

The statement compares a given value with defined constants and depending on the result, it takes an action.

- We put **the variable** that we want to **compare**, inside the **brackets after the operator** `switch` and it is called a **"selector"**. 
- The type must be **comparable** (numbers, strings,etc) 
- **Consecutively**, the program starts comparing each value which is found after the case labels.  
- Upon a match, the execution of the code from the respective place begins and continues until it reaches the operator `break`. 

`break` might be skipped, in order to execute a code from other `case` construction, until it reaches another operator. 

When **no matches** are **found**, the `default` construction is being executed, **if** such **exists**.

```js
switch (selector) {
  case value1:
    statements;
    break;
  case value2:
    statements;
    break;
}
```

# The default case
The default case specifies the `switch` section to execute **if the match expression doesn't match any other case label**.

If a default case is not present and the match expression doesn't match any other case label, program flow **falls** through the switch statement.

The default case can appear in any order in the switch statement, but regardless of its order in the source code it's always evaluated **last**, after all case labels have been evaluated.

```js
switch (selector) {
  case value1:
    statements;
    break;
  case value2:
    statements;
    break;
  default:
    statements;
    break;
}
```

# Example: Day of the Week
Let's write a program that prints **the day of the week** (in English) depending on the **given number** (1 … 7) or **"Error!"** if an invalid input is given.

```js
let day = Number(input);
switch (day) {
    case 1:
      console.log("Monday");
      break;
    case 2:
      console.log("Tuesday");
      break;
    case 3:
      console.log("Wednesday");
      break;
    case 4:
      console.log("Thursday");
      break;
    case 5:
      console.log("Friday");
      break;
    case 6:
      console.log("Saturday");
      break;
    case 7:
      console.log("Sunday");
      break;
    default:
      console.log("Error!");
      break;
}
```
[/slide]

[slide]
# Multiple Labels
In **JS** we have the possibility to use **multiple** `case` labels in the `switch-case` coonstruction, when they have to execute **the same code**. 

This way, when our **program** finds a **match**, it will execute the **next** code, because **after** the respective `case` label **there is no code** for execution and a `break` operator. 

```js
switch (selector) {
    case value1:
    case value2:
    case value3:
        construction;
        break;
    case value4:
    case value5:
        construction;
        break;
    default:
        construction;
        break;
}
```

# Example: Animal Type
Write a program that prints the type of the animal depending on its name:
-  dog -> **mammal**
-  crocodile, tortoise, snake -> **reptile**
-  others -> **unknown**

We can solve the task with `switch-case` conditions with multiple labels in the following way:
```js live
let animal = "snake";
switch (animal) {
    case "dog":
    case "cat":
      console.log("mammal");
      break;
    case "crocodile":
    case "tortoise":
    case "snake":
      console.log("reptile");
      break;
    default:
      console.log("unknown");
      break;
}
```
[/slide]