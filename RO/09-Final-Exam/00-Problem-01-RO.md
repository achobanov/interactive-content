# Problem 1: Study Materials

[slide]

# Description
The school year has already started and Annie has to buy a certain number of **packets of pencils**, **packets of markers**, and a **detergent** for cleaning the board. 

She is a regular customer of a bookstore, and there is a **discount** for her, which represents a **percentage** of the total.

Write a program that calculates how much money Annie will have to **save** to pay the bill, keeping in mind the following price list:

- **Package of pencils:** $5.80

- **Markers:** $7.20

- A **liter of detergent**: $1.20 

# Input
Four numbers are read from the console:

- Count pencil packages. Integer in the interval \[0 ... 100\]

- Count marker packages. Integer in the interval \[0 ... 100\]

- Liters of detergent for cleaning the board. Real number in the interval \[0.00… 50.00\]

- The percentage discount. Integer in the interval \[0 ... 100\]

# Output

Print on the console how much money Annie will need to pay her bill. The result should be **formatted** to the third decimal place.

[code-task title="Study materials" taskId="js-pb-final-exam-Study-Materials" executionType="tests-execution" executionStrategy="javascript-code" requiresInput]
[code-editor language=javascript]
```
function solve(input) {
	// Write your code here
}
```
[/code-editor]
[task-description]

# Example

| **Input** | **Output** |
| --- | --- |
|`["2", "3", "2.5", "25"]` | 27.150 |

# Comments

- Price for the **pencils**: `2 * 5.80 = 11.60`

- Price for the **markers**: `3 * 7.20 = 21.60`

- Price for the **detergent**: `2.5 * 1.20 = 3.00`

- **Total price:** `11.60 + 21.60 + 3.00 = 36.20`

- **Price with discount:** `36.20 – ((36.20 * 25) / 100) = 27.150`

# More Examples

| **Input** | **Output** |
| --- | --- |
|`["4", "2", "5", "13"]` | 37.932 |
|`["7, "8", "0.5", "45"]` | 54.340 |
 
[/task-description]
[code-io /]
[tests]
[test]
[input]
1
8
5.5
40
[/input]
[output]
42.000
[/output]
[/test]
[test]
[input]
9
9
4
15
[/input]
[output]
103.530
[/output]
[/test]
[test]
[input]
11
2
4.5
16
[/input]
[output]
70.224
[/output]
[/test]
[test]
[input]
12
12
10
5
[/input]
[output]
159.600
[/output]
[/test]
[test]
[input]
1
1
1
1
[/input]
[output]
14.058
[/output]
[/test]
[test]
[input]
3
11
8
50
[/input]
[output]
53.100
[/output]
[/test]
[test]
[input]
17
19
35.6
45
[/input]
[output]
152.966
[/output]
[/test]
[test]
[input]
48
62
32.54
18
[/input]
[output]
626.355
[/output]
[/test]
[test]
[input]
73
84
50.0
65
[/input]
[output]
380.870
[/output]
[/test]
[test]
[input]
100
100
50
100
[/input]
[output]
0.000
[/output]
[/test]
[/tests]
[/code-task]
[/slide]