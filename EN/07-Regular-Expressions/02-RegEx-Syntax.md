
# RegEx Syntax

[slide]

 # Character Classes

  In the **context of regular expressions**, a character class is a **set of characters enclosed within square brackets**. 

  It specifies the **characters** that will **successfully match** a **single character** from a given **input string**.

- Simple Class - a set of characters side-by-side within square brackets:
 [image assetsSrc="regex-example(2).png" /]
 In the example above, the class `[abc]` matches any character that is either **a**, **b**, or **c**

- Negation - the "^" metacharacter at the beginning of the character class matches all characters except the listed
[image assetsSrc="regex-example(3).png" /]
`[^abc]` - matches any character that is **not** **a**,**b** or **c**

- Ranges - insert a "-" between the first and last character to set the range
[image assetsSrc="regex-example(4).png" /]
`[0-9]` - character **range** matches any digit from 0 to 9:
  



[/slide]

[slide]

 # Predefined Classes

 - `\w` - matches any word character [a-z, A-Z, 0-9, _]
[image assetsSrc="regex-example(5).png" /]

[/slide]

[slide]

# Character Escapes

[/slide]

[slide]

# Anchors

[/slide]