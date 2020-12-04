[slide]

# Problem 5: TV Series Budget

## Description
You were hired by a TV company to write a program that calculates whether it is possible for their customers to purchase some of their TV series. You will receive a number, representing the budget of the customer, the total number of TV series titles, that the user will want to purchase, and afterward the title and price for each of the entries.
Some of the series have a discount:
- Thrones – 50\%
- Lucifer – 40\%	
- Protector – 30\%
- TotalDrama – 20\%
- Area – 10\%

## Input
You receive from the console:
- Budget - real number in the range \[10.0… 100.0\]
- Count series - n – whole number in the range \[1… 10\]

For each series you receive two lines:
- Name of the series - string
- Price for a series - real number in the range \[1.0… 15.0\]

## Output
Print one line on the console:

- If your budget is greater than or equal to the price of the series: `You bought all the series and have {money left}$ left.`

- If your budget is less than the price of the series: `You need {money needed}$ more to buy the series!`

The result must be formatted to two digits after the decimal point.
[code-task title="TV Series Budget" executionType="tests-execution" executionStrategy="javascript-code" requiresInput]
[code-editor language=javascript]
```
function solve(input) {
	// Write your code here
}
```
[/code-editor]
[task-description]
## Input
Budget - 10

Total number of TV series - 3

First title - Thrones

Price for the first one - 5

Second title - Riverdale

Price for the second one - 5

Third title - Gotham

Price for the third one - 2

## Output
You bought all the series and have 0.50$ left.

## Comments
You receive budget – 10$ and count of series - 3.

The first series is Thrones with price 5$, which has 50\% discount from the price `5 - 50% = 2.50$`. 

The second series is Riverdale, which does not have a discount on the price. 

The third series also does not have a discount. 

Price of series is `2.50 + 5 + 2 = 9.50$`. 

Your budget is bigger than the price of series, so you can buy them.
[/task-description]
[code-io /]
[tests]
[test]
[input]
25
2
Thrones
6
Lucifer
5
[/input]
[output]
You bought all the series and have 19.00$ left.
[/output]
[/test]
[test]
[input]
15
3
Protector
8
TotalDrama
6
Area
5
[/input]
[output]
You bought all the series and have 0.10$ left.
[/output]
[/test]
[test]
[input]
50
2
Lord of the rings
40
Gotham
10
[/input]
[output]
You bought all the series and have 0.00$ left.
[/output]
[/test]
[test]
[input]
24
4
Gotham
11
Thrones
5
Lucifer
9
Unkown
4
[/input]
[output]
You bought all the series and have 1.10$ left.
[/output]
[/test]
[test]
[input]
5
2
Area
12
Legendarie
48
[/input]
[output]
You need 53.80$ more to buy the series!
[/output]
[/test]
[test]
[input]
10
4
Thrones
8
Lucifer
5
Stoned
4
MK
12
[/input]
[output]
You need 13.00$ more to buy the series!
[/output]
[/test]
[test]
[input]
5
4
Legends
5
Gotham
4
Lucifer
12
Thrones
4
[/input]
[output]
You need 13.20$ more to buy the series!
[/output]
[/test]
[test]
[input]
5
2
Thrones
5
Scooby-Doo
2.50
[/input]
[output]
You bought all the series and have 0.00$ left.
[/output]
[/test]
[test]
[input]
14.67
3
Golden age
2.47
Rush hours series
15
Unknown
1.45
[/input]
[output]
You need 4.25$ more to buy the series!
[/output]
[/test]
[test]
[input]
100
4
Area
15
Legendary
10
Teen wolf
10
Breaking bad
15
[/input]
[output]
You bought all the series and have 51.50$ left.
[/output]
[/test]
[/tests]
[/code-task]
[/slide]