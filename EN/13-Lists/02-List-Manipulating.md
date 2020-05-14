[slide]
# List Manipulating
**List manipulation** is easier than an array because of its **methods**.


# Lists methods
There are a lot of useful **methods** in a List:

`add(element)` method - **appends** the element at the **end** of the **list**:

```java live
List<String> names = new ArrayList<>();

names.add("Peter");
names.add("Maria");
names.add("George");

for (String name : names){
  System.out.println(name);
}
```

`add(index, element)` - inserts an element to given position:

```java live
List<Integer> nums = new ArrayList<>();
        nums.add(10);
        nums.add(20);
        nums.add(30);
        nums.add(40);
        nums.add(50);

        nums.add(0, -100); // insert the number -100 at index 0

        for (Integer num : nums) {
            System.out.print(num + " ");
        }
}

```

`remove(element)` - **removes** the **first occurrence** of the **specified element** (returns **true** / **false**)

```java live
 List<String> names = new ArrayList<>();

 names.add("Peter");
 names.add("Maria");
 names.add("George");

 System.out.println(names.remove("Maria")); // return true because "Maria" is in the List
 System.out.println(names.remove("John"));  // return false because "John" is not in the List

 for (String name : names){
     System.out.println(name);
 }

```

`remove(index)` - **removes** the **element** at the **specified index**

```java live
List<String> names = new ArrayList<>();

names.add("Peter");
names.add("Maria");
names.add("George")
names.remove(1); // remove element at index 1

for (String name : names){
  System.out.println(name);
}
```

`set(index, item)` - replaces element at a given index

```java live
 Integer [] numbers = new Integer[] {10, 20, 30, 40, 50};

List<Integer> nums = Arrays.asList(numbers); // convert the numbers array into List

nums.set(4, -100); // replace the element at index 4 (50) with -100

for (Integer num : nums) {
    System.out.print(num + " ");
}
```
Let's explain what does the code do above:
- On the first line we initialize an array `numbers` not with primitive type `int []` but with its wrapper class `Integer []`, because the List can store only objects.
- After that we **convert** the **array** numbers into **List** using  `Arrays.asList()` - method
- On the next row we **replace** the element at **index 4** with **-100**.

`get()` - access an element to the given index

```java live
List<Integer> nums = new ArrayList<>(Arrays.asList(10, 20, 30, 40, 50));
        
int numberAtIndex4 = nums.get(4);
        
System.out.println(numberAtIndex4);
```

`contains(element)` - checks if an element is in the List

```java live
List<String> names = new ArrayList<>(Arrays.asList("Maria", "Peter", "George"));

if (names.contains("Maria")){ 
     System.out.println("Yes, the name is in the List.");
}
```

`size()` - number of elements in the List

```java live
List<String> names = new ArrayList<>(Arrays.asList("Maria", "Peter", "George"));

int numberOfNames = names.size();

System.out.println(numberOfNames);
```
[/slide]