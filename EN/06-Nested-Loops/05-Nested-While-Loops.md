[slide hideTitle]
# Nested while Loops

interactive-programming-basics-with-java-nested-loops-28-30-nested-while-loops

The use of nested `while` loops is very similar to the one of the `for`.

Here is the syntax in Java:
```java
while (condition) {
  // Outer Loop 
  while (condition) {
    // Inner Loop
    
    // Statements
  }
}
```

# Example:

```java live
int i = 0;
int n = 5;
while (i < n) {
  System.out.printf("Value of i: %d%n", i);
  int j = 1;
  i++;

  while (j < n) {
    System.out.printf("  Value of j: %d%n", j);
    j++;
  }
}
```
[/slide]

[slide hideTitle]
# Problem: Triangle of Stars with While

interactive-programming-basics-with-java-nested-loops-31-problem-triangle-of-stars

[code-task title="Triangle of Stars with While" taskId="java-basics-nested-loops-Triangle-of-Stars-with-While" executionType="tests-execution" executionStrategy="java-code" requiresInput]
[code-editor language=java]
```
import java.util.Scanner;

public class Main {
    public static void main(String[] args) {
        // Write your code here
    }
}
```
[/code-editor]
[task-description]
# Description
Write a program, which:

* Reads the **height** of a triangle from the console
* Prints a **triangle of stars**
# Example

| **Input** |**Output**|
| ----- | ----- |
| 5 | \* |
|| \*\* |
|| \*\*\* |
|| \*\*\*\* |
|| \*\*\*\*\* |

[/task-description]
[tests]
[test]
[input]
4
[/input]
[output]
\*
\*\*
\*\*\*
\*\*\*\*
[/output]
[/test]
[/tests]
[code-io/]
[/code-task]

[/slide]

[slide hideTitle]
# Solution: Triangle of Stars with While

interactive-programming-basics-with-java-nested-loops-31-problem-triangle-of-stars-solution

[code-task title="Triangle of Stars with While" executionType="tests-execution" executionStrategy="java-code" requiresInput]
[code-editor language=java]
```
import java.util.Scanner;

public class Main {
    public static void main(String[] args) {
      // Write code here
    }
}
```
[/code-editor]
[task-description]
# Description
Write a program, which:

* Reads the **height** of a triangle from the console
* Prints a **triangle of stars**
# Example

| **Input** |**Output**|
| ----- | ----- |
| 5 | \* |
|| \*\* |
|| \*\*\* |
|| \*\*\*\* |
|| \*\*\*\*\* |

[/task-description]
[tests]
[test]
[input]
4
[/input]
[output]
\*
\*\*
\*\*\*
\*\*\*\*
[/output]
[/test]
[/tests]
[code-io/]
[/code-task]

[/slide]

[slide hideTitle]

# Example: Combining while and for Loops

interactive-programming-basics-with-java-nested-loops-33-nesting-while-and-for-loops + 

interactive-programming-basics-with-java-nested-loops-34-problem-and-solution-sum-digits-calcuulator


[/slide]