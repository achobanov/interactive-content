# The Switch-Case Statement
[slide hideTitle]
# The Switch-Case Statement

interactive-programming-basics-with-java-conditional-statements-advanced-24-25-switch-case

The switch-case condition works as a sequence of **if-else** blocks. 

Whenever the work of our program depends on the value of one variable, instead of making consecutive conditions with `if-else` blocks, we can **use** the conditional `switch` statement. 

It is being used for **choosing between a list of possibilities**. 

The statement compares a given value with defined constants and depending on the result, it takes an action.

- We put **the variable** that we want to **compare**, inside the **brackets after the operator** `switch` and it is called a **"selector"**. 
- Here **the type must be comparable** (numbers, strings). 
- **Consecutively**, the program starts **comparing** each **value** that is **found** after the `case` **labels**. 
- Upon a match, the execution of the code from the respective place begins and continues until it reaches the operator `break`. 

In some programming languages (like C and C++) `break` might be skipped, in order to execute a code from other `case` construction, until it reaches another operator. 

In Java though, the presence of `break` is **mandatory** for **every** `case` that contains a program logic. 

When **no matches** are **found**, the `default` construction is being executed, **if** such **exists**.

```java
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

```java
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
[/slide]

[slide hideTitle]
# Example: "Yes" or "No"

interactive-programming-basics-with-java-conditional-statements-advanced-26-switch-case-example + 

interactive-programming-basics-with-java-conditional-statements-advanced-26-switch-case-example-demo

Let's write a program that prints **"Yes" or "No"** (in English) depending on the **given command** (Y, N) or **"Invalid response"** if an invalid input is given.

```java
Scanner scanner = new Scanner(System.in);
String choice = scanner.nextLine();
switch (choice) {
  case "Y":
    System.out.println("Yes");
    break;
  case "N":
    System.out.println("No");
    break;
  default:
    System.out.println("Invalid response");
    break;
}
```
[/slide]

[slide hideTitle]
# Multiple Labels

interactive-programming-basics-with-java-conditional-statements-advanced-27-29-multiple-labels-in-switch-case

In **Java** we have the possibility to use **multiple** `case` labels in the `switch-case` coonstruction, when they have to execute **the same code**. 

This way, when our **program** finds a **match**, it will execute the **next** code, because **after** the respective `case` label **there is no code** for execution and a `break` operator. 

```java
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
```java
Scanner scanner = new Scanner(System.in);
String animal = scanner.nextLine();
switch (animal) {
    case "dog":
    case "cat":
      System.out.println("mammal");
      break;
    case "crocodile":
    case "tortoise":
    case "snake":
      System.out.println("reptile");
      break;
    default:
      System.out.println("unknown");
      break;
}
```
[/slide]