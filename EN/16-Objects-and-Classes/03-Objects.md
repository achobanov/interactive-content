[slide]
# Objects

An object is **basic unit** and an **instance of a class**.
Classes define templates for objects: fields, constructors, methods.

Example:
- Sample class: LocalDate
- Sample objects: birthdayPeter, birthdayMaria


An object represents **real-life subjects**. 

If you compare the software object with a real-world object, they have very similar characteristics.
You can find many objects around us: cars, dogs, humans, etc.

[/slide]


[slide]
# Definition of Object

An object has:

- State is represented by **fields**.

- Behavior is represented by **methods**. An object interacts with another object by invoking methods. 

- Identity gives an **unique name** to an object.


Real-life example: A dog has states - color, name, breed; and behaviors – barking, eating, wagging the tail. 


An object holds a set of named values.
Example: birthday object holds day, month and year.

```java live
LocalDate birthday = LocalDate.of(2018,5,5);
System.out.println(birthday);
```
[/slide]


[slide]
# Create an Object

Creating an object of a defined class is called **instantiation**.
The **instance** is the object itself, which is created runtime.
All instances have common **behavior**. 
s

To create an object, specify the **class name**, followed by the **object name**, and use the **keyword** `new`:
```java
public class MyClass {
    public static void main(String[] args) {
        MyClass myObject = new MyClass();
    }
}
```

You can create multiple objects of one class.
```java
public class MyClass {
    public static void main(String[] args) {
        MyClass myObj1 = new MyClass();
        MyClass myObj2 = new MyClass();
    }
}
```

[/slide]

[slide]
# Problem: Songs
[code-task title="Songs" taskId="8e0847be-8955-427d-b47b-3a8a915cb610" executionType="tests-execution" executionStrategy="java-code" requiresInput]
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
## Description

Define a class **Song**, which holds the following information about songs: **Type List**, **Name** and **Time**.

On the first line you will receive the **number of songs - N**.

On the next N-lines you will be receiving data in the following format: **"{typeList}_{name}_{time}"**.

On the last line you will receive **Type List / "all"**.

Print only the **Names of the songs** which are from that **Type List / All songs**.

## Examples

| **Input** | **Output** |
| --- | --- |
| 3 | DownTown |
| favourite_DownTown_3:14 | Kiss |
| favourite_Kiss_4:16 | Smooth Criminal |
| favourite_Smooth Criminal_4:01 |  |
| favourite |  |

| **Input** | **Output** |
| --- | --- |
| 4 | Andalouse |
| favourite_DownTown_3:14 |  |
| listenLater_Andalouse_3:24 |  |
| favourite_In To The Night_3:58 |  |
| favourite_Live It Up_3:48 |  |
| listenLater |  |

| **Input** | **Output** |
| --- | --- |
| 2 | Replay |
| like_Replay_3:15 | Photoshop |
| ban_Photoshop_3:48 |  |
| all |  |



[/task-description]
[code-io /]
[tests]
[test open]
[input]
3
favourite_DownTown_3:14
favourite_Kiss_4:16
favourite_Smooth Criminal_4:01
favourite
[/input]
[output]
DownTown
Kiss
Smooth Criminal
[/output]
[/test]
[test open]
[input]
4
favourite_DownTown_3:14
listenLater_Andalouse_3:24
favourite_In To The Night_3:58
favourite_Live It Up_3:48
listenLater
[/input]
[output]
Andalouse
[/output]
[/test]
[test open]
[input]
2
like_Replay_3:15
ban_Photoshop_3:48
all
[/input]
[output]
Replay
Photoshop
[/output]
[/test]
[test]
[input]
4
v_rrr_3:14
listenLater_rr_3:24
v_r_3:58
v_rp_3:48
v
[/input]
[output]
rrr
r
rp
[/output]
[/test]
[test]
[input]
6
v_rrr_3:14
listenLater_rr_3:24
v_r_3:58
v_rp_3:48
b_wqeq_3:58
b_tre_3:48
b
[/input]
[output]
wqeq
tre
[/output]
[/test]
[test]
[input]
5
a_opsa_2:51
like_Replay_3:15
c_tigre_4:21
Ceca_Trepni_3:58
ban_Photoshop_3:48
all
[/input]
[output]
opsa
Replay
tigre
Trepni
Photoshop
[/output]
[/test]
[/tests]
[/code-task]
[/slide]

[slide]
# Solution: Songs
[code-task title="Songs" executionType="tests-execution" executionStrategy="java-code" requiresInput]
[code-editor language=java]
```
import java.util.ArrayList;
import java.util.List;
import java.util.Scanner;
import java.util.stream.Collectors;

public class Songs {

    public static class Song{
        private String typeList;
        private String name;
        private String time;

        public String getTypeList(){
            return typeList;
        }

        public String getName(){
            return name;
        }

        public void setTypeList(String typeList){
            this.typeList = typeList;
        }

        public void setName(String name){
            this.name = name;
        }

        public void setTime(String time){
            this.time = time;
        }
    }

    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);

        int n = Integer.parseInt(scanner.nextLine());
        List<Song> songs = new ArrayList<>();

        for (int i = 0; i < n; i++) {
            String [] data = scanner.nextLine().split("_");
            String type = data[0];
            String name = data[1];
            String time = data[2];

            Song song = new Song();

            song.setTypeList(type);
            song.setName(name);
            song.setTime(time);

            songs.add(song);
        }
        String typeList = scanner.nextLine();

        if(typeList.equals("all")){
            for (Song song : songs) {
                System.out.println(song.getName());
            }
        } else {
            for (Song song : songs) {
                if(song.getTypeList().equals(typeList)){
                    System.out.println(song.getName());
                }
            }
        }
    }
}
```
[/code-editor]
[task-description]
## Description

Define a class **Song**, which holds the following information about songs: **Type List**, **Name** and **Time**.

On the first line you will receive the **number of songs - N**.

On the next N-lines you will be receiving data in the following format: **"{typeList}_{name}_{time}"**.

On the last line you will receive **Type List / "all"**.

Print only the **Names of the songs** which are from that **Type List / All songs**.

## Examples

| **Input** | **Output** |
| --- | --- |
| 3 | DownTown |
| favourite_DownTown_3:14 | Kiss |
| favourite_Kiss_4:16 | Smooth Criminal |
| favourite_Smooth Criminal_4:01 |  |
| favourite |  |

| **Input** | **Output** |
| --- | --- |
| 4 | Andalouse |
| favourite_DownTown_3:14 |  |
| listenLater_Andalouse_3:24 |  |
| favourite_In To The Night_3:58 |  |
| favourite_Live It Up_3:48 |  |
| listenLater |  |

| **Input** | **Output** |
| --- | --- |
| 2 | Replay |
| like_Replay_3:15 | Photoshop |
| ban_Photoshop_3:48 |  |
| all |  |



[/task-description]
[code-io /]
[tests]
[test open]
[input]
3
favourite_DownTown_3:14
favourite_Kiss_4:16
favourite_Smooth Criminal_4:01
favourite
[/input]
[output]
DownTown
Kiss
Smooth Criminal
[/output]
[/test]
[test open]
[input]
4
favourite_DownTown_3:14
listenLater_Andalouse_3:24
favourite_In To The Night_3:58
favourite_Live It Up_3:48
listenLater
[/input]
[output]
Andalouse
[/output]
[/test]
[test open]
[input]
2
like_Replay_3:15
ban_Photoshop_3:48
all
[/input]
[output]
Replay
Photoshop
[/output]
[/test]
[test]
[input]
4
v_rrr_3:14
listenLater_rr_3:24
v_r_3:58
v_rp_3:48
v
[/input]
[output]
rrr
r
rp
[/output]
[/test]
[test]
[input]
6
v_rrr_3:14
listenLater_rr_3:24
v_r_3:58
v_rp_3:48
b_wqeq_3:58
b_tre_3:48
b
[/input]
[output]
wqeq
tre
[/output]
[/test]
[test]
[input]
5
a_opsa_2:51
like_Replay_3:15
c_tigre_4:21
Ceca_Trepni_3:58
ban_Photoshop_3:48
all
[/input]
[output]
opsa
Replay
tigre
Trepni
Photoshop
[/output]
[/test]
[/tests]
[/code-task]
[/slide]


[slide]
# Problem: Students
[code-task title="Students" taskId="2a4c6916-905f-4143-b6e2-d275a309221b" executionType="tests-execution" executionStrategy="java-code" requiresInput]
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
## Description
Define a class **Student**, which holds the following information about students: first name, last name, age and hometown.

Read list of students until you receive **"end"** command.

After that, you will receive a city name.

Print only students which are from the given city, in the following format: **"{firstName} {lastName} is {age} years old."**.

## Examples
| **Input** | **Output** |
| --- | --- |
| John Smith 15 Sofia | John Smith is 15 years old. |
| Peter Ivanov 14 Plovdiv | Linda Bridge is 16 years old. |
| Linda Bridge 16 Sofia |  |
| Simon Stone 12 Varna |  |
| end |  |
| Sofia |  |

| **Input** | **Output** |
| --- | --- |
| Anthony Taylor 15 Chicago | Anthony Taylor is 15 years old. |
| David Anderson 16 Washington | Jack Lewis is 14 years old. |
| Jack Lewis 14 Chicago | David Lee is 14 years old. |
| David Lee 14 Chicago |  |
| end |  |
| Chicago |  |



[/task-description]
[code-io /]
[tests]
[test open]
[input]
John Smith 15 Sofia
Peter Ivanov 14 Plovdiv
Linda Bridge 16 Sofia
Simon Stone 12 Varna
end
Sofia
[/input]
[output]
John Smith is 15 years old
Linda Bridge is 16 years old
[/output]
[/test]
[test open]
[input]
Anthony Taylor 15 Chicago
David Anderson 16 Washington
Jack Lewis 14 Chicago
David Lee 14 Chicago
end
Chicago
[/input]
[output]
Anthony Taylor is 15 years old
Jack Lewis is 14 years old
David Lee is 14 years old
[/output]
[/test]
[test]
[input]
Anthony Taylor 13 varna
David A 14 b
Jack L 16 varna
David Lee 17 varna
end
varna
[/input]
[output]
Anthony Taylor is 13 years old
Jack L is 16 years old
David Lee is 17 years old
[/output]
[/test]
[test]
[input]
Thony Taylor 13 varna
David A 14 b
Jack L 16 varna
David Lee 17 b
end
b
[/input]
[output]
David A is 14 years old
David Lee is 17 years old
[/output]
[/test]
[test]
[input]
T T 13 varna
b Aa 14 b
N m 21 c
Jack L 16 varna
David Lee 17 b
end
c
[/input]
[output]
N m is 21 years old
[/output]
[/test]
[test]
[input]
T T 13 v
b Aa 14 v
N m 21 v
Jack L 16 v
David Lee 17 v
end
v
[/input]
[output]
T T is 13 years old
b Aa is 14 years old
N m is 21 years old
Jack L is 16 years old
David Lee is 17 years old
[/output]
[/test]
[test]
[input]
T T 22 a
b Aa 14 e
N m 30 c
Jack L 18 e
Port Lee 14 e
end
e
[/input]
[output]
b Aa is 14 years old
Jack L is 18 years old
Port Lee is 14 years old
[/output]
[/test]
[/tests]
[/code-task]
[/slide]

[slide]
# Solution: Students
[code-task title="Students" executionType="tests-execution" executionStrategy="java-code" requiresInput]
[code-editor language=java]
```
import java.util.ArrayList;
import java.util.List;
import java.util.Scanner;

public class Students {

    static class  Student {
        private String firstName;
        private String lastName;
        private int age;
        private String city;

        public Student (String firstName, String lastName, int age, String city){
            this.firstName = firstName;
            this.lastName = lastName;
            this.age = age;
            this.city = city;
        }

        public String getFirstName() {
            return firstName;
        }

        public String getLastName() {
            return lastName;
        }

        public String getCity() {
            return city;
        }

        public int getAge() {
            return age;
        }

        public void setAge(int age) {
            this.age = age;
        }

        public void setCity(String city) {
            this.city = city;
        }
    }

    private static Student findStudent(String firstName, String lastName, List <Student> students ){
        for (Student student : students) {
            if(student.getFirstName().equals(firstName) &&
            student.getLastName().equals(lastName)){
                return student;
            }
        }
        return null;
    }

    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);

        List<Student> students = new ArrayList<>();

        String input = scanner.next();
        while (!input.equals("end")){
            String firstName = input;
            String lastName = scanner.next();
            int age = scanner.nextInt();
            String city = scanner.next();

            Student existingStudent = findStudent(firstName, lastName, students);
            if(existingStudent != null){
                existingStudent.setAge(age);
                existingStudent.setCity(city);
            }else{
                Student student = new Student(firstName, lastName, age, city);
                students.add(student);
            }


            input = scanner.next();

        }

        String cityName = scanner.next();

        for (Student student : students) {
            if(student.getCity().equals(cityName)){
                System.out.printf("%s %s is %d years old%n", student.getFirstName(),
                        student.getLastName(), student.getAge());
            }
        }

    }
}
```
[/code-editor]
[task-description]
## Description
Define a class **Student**, which holds the following information about students: first name, last name, age and hometown.

Read list of students until you receive **"end"** command.

After that, you will receive a city name.

Print only students which are from the given city, in the following format: **"{firstName} {lastName} is {age} years old."**.

## Examples
| **Input** | **Output** |
| --- | --- |
| John Smith 15 Sofia | John Smith is 15 years old. |
| Peter Ivanov 14 Plovdiv | Linda Bridge is 16 years old. |
| Linda Bridge 16 Sofia |  |
| Simon Stone 12 Varna |  |
| end |  |
| Sofia |  |

| **Input** | **Output** |
| --- | --- |
| Anthony Taylor 15 Chicago | Anthony Taylor is 15 years old. |
| David Anderson 16 Washington | Jack Lewis is 14 years old. |
| Jack Lewis 14 Chicago | David Lee is 14 years old. |
| David Lee 14 Chicago |  |
| end |  |
| Chicago |  |



[/task-description]
[code-io /]
[tests]
[test open]
[input]
John Smith 15 Sofia
Peter Ivanov 14 Plovdiv
Linda Bridge 16 Sofia
Simon Stone 12 Varna
end
Sofia
[/input]
[output]
John Smith is 15 years old
Linda Bridge is 16 years old
[/output]
[/test]
[test open]
[input]
Anthony Taylor 15 Chicago
David Anderson 16 Washington
Jack Lewis 14 Chicago
David Lee 14 Chicago
end
Chicago
[/input]
[output]
Anthony Taylor is 15 years old
Jack Lewis is 14 years old
David Lee is 14 years old
[/output]
[/test]
[test]
[input]
Anthony Taylor 13 varna
David A 14 b
Jack L 16 varna
David Lee 17 varna
end
varna
[/input]
[output]
Anthony Taylor is 13 years old
Jack L is 16 years old
David Lee is 17 years old
[/output]
[/test]
[test]
[input]
Thony Taylor 13 varna
David A 14 b
Jack L 16 varna
David Lee 17 b
end
b
[/input]
[output]
David A is 14 years old
David Lee is 17 years old
[/output]
[/test]
[test]
[input]
T T 13 varna
b Aa 14 b
N m 21 c
Jack L 16 varna
David Lee 17 b
end
c
[/input]
[output]
N m is 21 years old
[/output]
[/test]
[test]
[input]
T T 13 v
b Aa 14 v
N m 21 v
Jack L 16 v
David Lee 17 v
end
v
[/input]
[output]
T T is 13 years old
b Aa is 14 years old
N m is 21 years old
Jack L is 16 years old
David Lee is 17 years old
[/output]
[/test]
[test]
[input]
T T 22 a
b Aa 14 e
N m 30 c
Jack L 18 e
Port Lee 14 e
end
e
[/input]
[output]
b Aa is 14 years old
Jack L is 18 years old
Port Lee is 14 years old
[/output]
[/test]
[/tests]
[/code-task]
[/slide]

[slide]
# Problem: Students 2.0
[code-task title="Students 2.0" taskId="a7df71f0-19c2-4666-a95d-70079df7f461" executionType="tests-execution" executionStrategy="java-code" requiresInput]
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
## Description
Use the class from the previous problem.

If you receive a student which already exists (first name and last name should be unique) overwrite the information.

## Examples
## Examples
| **Input** | **Output** |
| --- | --- |
| John Smith 15 Sofia | John Smith is 16 years old. |
| John Smith 16 Sofia | Linda Bridge is 17 years old. |
| Linda Bridge 17 Sofia |  |
| Simon Stone 12 Varna |  |
| end |  |
| Sofia |  |



[/task-description]
[code-io /]
[tests]
[test open]
[input]
John Smith 15 Sofia
John Smith 16 Sofia
Linda Bridge 17 Sofia
Simon Stone 12 Varna
end
Sofia
[/input]
[output]
John Smith is 16 years old
Linda Bridge is 17 years old
[/output]
[/test]
[test]
[input]
John Smith 15 Sofia
Peter Ivanov 14 Plovdiv
Peter Ivanov 14 Sofia
Linda Bridge 16 Sofia
Simon Stone 12 Varna
end
Sofia
[/input]
[output]
John Smith is 15 years old
Peter Ivanov is 14 years old
Linda Bridge is 16 years old
[/output]
[/test]
[test]
[input]
J S 3 S
Peter Ivanov 14 P
P J 104 S
J P 61 S
Simon Stone 12 Varna
Simon Sone 12 Varna
end
Varna
[/input]
[output]
Simon Stone is 12 years old
Simon Sone is 12 years old
[/output]
[/test]
[test]
[input]
J S 3 S
Peter Ivanov 14 P
P J 104 S
J P 61 S
Simon Stone 12 Varna
Simon Sone 12 Varna
end
S
[/input]
[output]
J S is 3 years old
P J is 104 years old
J P is 61 years old
[/output]
[/test]
[/tests]
[/code-task]
[/slide]

[slide]
# Solution: Students 2.0
[code-task title="Students 2.0" executionType="tests-execution" executionStrategy="java-code" requiresInput]
[code-editor language=java]
```
import java.util.ArrayList;
import java.util.List;
import java.util.Scanner;

public class Students2 {

    static class  Student {
        private String firstName;
        private String lastName;
        private int age;
        private String city;

        public Student (String firstName, String lastName, int age, String city){
            this.firstName = firstName;
            this.lastName = lastName;
            this.age = age;
            this.city = city;
        }

        public String getFirstName() {
            return firstName;
        }

        public String getLastName() {
            return lastName;
        }

        public String getCity() {
            return city;
        }

        public int getAge() {
            return age;
        }

        public void setAge(int age) {
            this.age = age;
        }

        public void setCity(String city) {
            this.city = city;
        }

        public void setFirstName(String firstName) {
            this.firstName = firstName;
        }

        public void setLastName(String lastName) {
            this.lastName = lastName;
        }
    }

    private static Student getStudent(List<Student> students, String firstName, String lastName) {
        Student existingStudent = null;
        for (Student student : students) {
            if(student.getFirstName().equals(firstName) &&
                    student.getLastName().equals(lastName)){
                existingStudent = student;
            }
        }
        return existingStudent;
    }

    private static boolean isStudentExisting(List<Student> students, String firstName, String lastName) {
        for (Student student : students) {
            if(student.getFirstName().equals(firstName) &&
                    student.getLastName().equals(lastName)){
                return true;
            }
        }
        return false;
    }

    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);

        List<Student> students = new ArrayList<>();

        String input = scanner.next();
        while (!input.equals("end")){
            String firstName = input;
            String lastName = scanner.next();
            int age = scanner.nextInt();
            String city = scanner.next();

            if(isStudentExisting(students, firstName, lastName)){
                Student student = getStudent(students,firstName,lastName);
                student.setFirstName(firstName);
                student.setLastName(lastName);
                student.setAge(age);
                student.setCity(city);
            } else {
                Student student = new Student(firstName,lastName,age,city);
                students.add(student);
            }

            Student existingStudent = getStudent(students, firstName, lastName);
            if (existingStudent != null){
                existingStudent.setAge(age);
                existingStudent.setCity(city);
            } else {
                Student student = new Student(firstName, lastName, age, city);
                students.add(student);
            }
 
            input = scanner.next();
        }

        String cityName = scanner.next();

        for (Student student : students) {
            if(student.getCity().equals(cityName)){
                System.out.printf("%s %s is %d years old%n", student.getFirstName(),
                        student.getLastName(), student.getAge());
            }
        }
    }
}
```
[/code-editor]
[task-description]
## Description
Use the class from the previous problem.

If you receive a student which already exists (first name and last name should be unique) overwrite the information.

## Examples
## Examples
| **Input** | **Output** |
| --- | --- |
| John Smith 15 Sofia | John Smith is 16 years old. |
| John Smith 16 Sofia | Linda Bridge is 17 years old. |
| Linda Bridge 17 Sofia |  |
| Simon Stone 12 Varna |  |
| end |  |
| Sofia |  |



[/task-description]
[code-io /]
[tests]
[test open]
[input]
John Smith 15 Sofia
John Smith 16 Sofia
Linda Bridge 17 Sofia
Simon Stone 12 Varna
end
Sofia
[/input]
[output]
John Smith is 16 years old
Linda Bridge is 17 years old
[/output]
[/test]
[test]
[input]
John Smith 15 Sofia
Peter Ivanov 14 Plovdiv
Peter Ivanov 14 Sofia
Linda Bridge 16 Sofia
Simon Stone 12 Varna
end
Sofia
[/input]
[output]
John Smith is 15 years old
Peter Ivanov is 14 years old
Linda Bridge is 16 years old
[/output]
[/test]
[test]
[input]
J S 3 S
Peter Ivanov 14 P
P J 104 S
J P 61 S
Simon Stone 12 Varna
Simon Sone 12 Varna
end
Varna
[/input]
[output]
Simon Stone is 12 years old
Simon Sone is 12 years old
[/output]
[/test]
[test]
[input]
J S 3 S
Peter Ivanov 14 P
P J 104 S
J P 61 S
Simon Stone 12 Varna
Simon Sone 12 Varna
end
S
[/input]
[output]
J S is 3 years old
P J is 104 years old
J P is 61 years old
[/output]
[/test]
[/tests]
[/code-task]
[/slide]