[slide hideTitle]
# Console App in IntelliJ IDEA

[video src="https://videos.softuni.org/hls/Java/Java-Programming-Basics/00-intro-programming/EN/Java-basics-introduction-to-programming-26-27-28-Console-app-in-IntelliJ-IDEA-,1080p,720p,480p,360p,240p,.mp4/urlset/master.m3u8" poster="" /]

We already have IntelliJ IDEA and we can start it.

Create new Console Application in IntelliJ IDEA: `[New Project]` -> `[Java]` -> `[Template Command Line App]` -> `[Finish]`

We set **a meaningful name** to our program, for example `HelloJava`:

[image assetsSrc="intro-to-programming-name-hellojava.png" /]

IntelliJ IDEA is going to create for us **an empty Java program**, which we have to finish writing.

# Configuring JDK in IntelliJ IDEA
If no JDK is still configured, you should configure it:

[image assetsSrc="intro-to-programming-4.png" /]

Click [New] and locate your JDK installation:

[image assetsSrc="intro-to-programming-5.png" /]
[/slide]

[slide hideTitle]
# Writing the Program Code

[video src="https://videos.softuni.org/hls/Java/Java-Programming-Basics/00-intro-programming/EN/Java-basics-introduction-to-programming-29-writing-programming-code-in-intelliJ-IDEA-,1080p,720p,480p,360p,240p,.mp4/urlset/master.m3u8" poster="" /]

The commands of the program are written in `main(String[] args)`, between the opening and the closing parentheses `{ }`.

This is the main method (action), that is being executed with the start of a Java program.

Press `[Enter]` after **the opening parentheses** `{` and **start writing**.

The code of the program is written **inwards**, as this is a part of shaping up the text for convenience during a review and/or debugging.

[image assetsSrc="intro-to-programming-inwards-example.png" /]

Write the following command:
```java
System.out.println("Hello Java");
```

Here is how our program should look like in IntelliJ IDEA:

[image assetsSrc="intro-to-programming-code-in-intellij.png" /]

The command `System.out.println("Hello Java")` in the Java language means to execute printing (`System.out.println(…)`) on the console and to print the text message `Hello Java`, which we should surround by quotation marks, in order to clarify that this is a text.

In the end of each command in the Java language the symbol `;` is being put and it says that the command ends in that place (it doesn't continue on the next line).

This command is very typical in programming: we say a given **object** should be found (in this case the console) and some **action** should be executed upon it (in this case it is printing something that is given inside the brackets). 

More technically explained, `out` is a static member in the `System` class, being an instance of PrintStream. And println is a normal (overloaded) method of the PrintStream class and we give as a parameter to it a text literal `"Hello Java"`.
[/slide]

[slide hideTitle]
# Starting the Program

[video src="https://videos.softuni.org/hls/Java/Java-Programming-Basics/00-intro-programming/EN/Java-basics-introduction-to-programming-30-Starting-the-program-,1080p,720p,480p,360p,240p,.mp4/urlset/master.m3u8" poster="" /]

To start the program, press `[Ctrl + Shift + F10]`. If there aren't any errors, the program will be executed. 

The result will appear in the console (terminal window):

[image assetsSrc="intro-to-programming-console.png" /]

Another way to start your program is by clicking the right mouse button and selecting **Run 'Main'**

[image assetsSrc="run-intellij-right-click.png" /]

Actually, the output from the program is the following text message:
```
Hello Java
```
[/slide]

[slide hideTitle]
# Example: Creating Console App in IntelliJ IDEA

Java-basics-introduction-to-programming-26-30-Console-app-in-inteliJ-IDEA-demo

[/slide]