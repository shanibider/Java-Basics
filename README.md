# Java Basics Fundamentals <img align="center" height=40px src="https://skillicons.dev/icons?i=java">

<p><img align="center" src="https://github.com/shanibider/-Java-Basics/assets/72359805/00b8dc2c-00c6-4a8b-a9a8-d5c2921d1362"></p>

**Java** fundamental concepts and code examples covering various aspects of Java programming language.
Whether you're new to Java or seeking a refresher, this resource aims to provide a clear understanding
of essential Java concepts. 

# Essential Java fundamentals 🧱 -

## Variables and Data Types 🎖

Java supports various data types, including primitive types like `int`, `double`, `boolean`, and reference types like `String`. Understanding how to declare variables and manipulate data types is crucial.

```java
// Variable declaration and initialization
int age = 30;
double price = 19.99;
String name = "John Doe";
boolean isStudent = true;
```

## Control Flow 🎖

Control flow structures such as loops (`for`, `while`, `do-while`) and conditional statements (`if`, `else if`, `else`) dictate the flow of program execution. Mastering these constructs is fundamental for building robust Java applications.

```java
// Example of a for loop
for (int i = 0; i < 5; i++) {
    System.out.println("Iteration: " + i);
}

// Example of if-else statement
int num = 10;
if (num > 0) {
    System.out.println("Positive number");
} else {
    System.out.println("Negative number");
}
```

## Object-Oriented Programming 🎖

Java is an object-oriented programming language, emphasizing concepts like classes, objects, inheritance, polymorphism, and encapsulation. These concepts enable developers to organize and structure code effectively.

```java
// Example of class and object instantiation
class Person {
    String name;
    int age;

    void displayInfo() {
        System.out.println("Name: " + name + ", Age: " + age);
    }
}

// Creating an object of the Person class
Person person1 = new Person();
person1.name = "Alice";
person1.age = 25;
person1.displayInfo();
```

<p align="center">
<img src="https://github.com/shanibider/-Java-Basics/assets/72359805/5c6f65dc-3c11-4c42-a5ec-1559a724f7c7">
</p>


## Exception Handling 🎖

Java provides robust exception handling mechanisms to gracefully manage runtime errors. Understanding how to handle exceptions is essential for writing reliable and fault-tolerant Java applications.

```java
// Example of try-catch block
try {
    int result = 10 / 0; // Division by zero
} catch (ArithmeticException e) {
    System.out.println("Error: " + e.getMessage());
}
```

## Input/Output Operations 🎖

Input/output operations are fundamental for interacting with users and external systems. Java offers various classes and methods for performing input/output operations efficiently.

```java
// Example of reading user input
import java.util.Scanner;

Scanner scanner = new Scanner(System.in);
System.out.print("Enter your name: ");
String name = scanner.nextLine();
System.out.println("Hello, " + name + "!");
scanner.close();
```

## File Handling 🎖

Java provides classes like `File`, `FileReader`, `FileWriter`, etc., for working with files and directories. Understanding file handling is essential for reading from and writing to files in Java applications.

```java
// Example of file reading
import java.io.File;
import java.io.FileNotFoundException;
import java.util.Scanner;

try {
    File file = new File("example.txt");
    Scanner scanner = new Scanner(file);
    while (scanner.hasNextLine()) {
        System.out.println(scanner.nextLine());
    }
    scanner.close();
} catch (FileNotFoundException e) {
    System.out.println("File not found: " + e.getMessage());
}
```
<br>

---


# Brief overview and code examples from my code 🏆- 

### User Input 🖋️
User input allows interaction between the user and the program during runtime. This is typically achieved using the `Scanner` class.

```java
import java.util.Scanner;

Scanner scanner = new Scanner(System.in);
System.out.print("Enter your name: ");
String name = scanner.nextLine();
System.out.println("Hello, " + name + "!");
scanner.close();
```


### HashMap 🔑
A `HashMap` is a data structure that stores key-value pairs and allows rapid retrieval of values based on their keys.

```java
import java.util.HashMap;

HashMap<String, Integer> map = new HashMap<>();
map.put("apple", 10);
map.put("banana", 20);
int quantity = map.get("apple");
System.out.println("Quantity of apples: " + quantity);
```


### Setter and This 🔄
Setters are methods used to set the values of instance variables, often used in combination with the `this` keyword to refer to the current object.

```java
public class Person {
    private String name;

    public void setName(String name) {
        this.name = name;
    }
}
```

### Do-While Loop 🔁
A `do-while` loop is similar to a `while` loop, but it guarantees that the loop body executes at least once before the condition is checked.

```java
int i = 0;
do {
    System.out.println(i);
    i++;
} while (i < 5);
```


### Switch Statement 🔀
A `switch` statement allows you to execute different blocks of code based on the value of a variable or expression.

```java
int day = 2;
switch (day) {
    case 1:
        System.out.println("Sunday");
        break;
    case 2:
        System.out.println("Monday");
        break;
    // other cases...
    default:
        System.out.println("Invalid day");
}
```


### Arrays 📚
Arrays in Java allow you to store multiple values of the same type in a single variable.

```java
int[] numbers = {1, 2, 3, 4, 5};
System.out.println(numbers[0]); // Outputs: 1
```


### Multi-Dimensional Arrays 📊
Multi-dimensional arrays are arrays of arrays, allowing you to create tables or matrices.

```java
int[][] matrix = {
    {1, 2, 3},
    {4, 5, 6},
    {7, 8, 9}
};
System.out.println(matrix[1][1]); // Outputs: 5
```


### Classes and Objects 🏗️
Classes are blueprints for creating objects. Objects are instances of classes that encapsulate data and behavior.

```java
public class Car {
    private String model;

    public Car(String model) {
        this.model = model;
    }

    public void drive() {
        System.out.println("Driving a " + model);
    }
}

Car myCar = new Car("Toyota");
myCar.drive();
```

### Getters and Return Values 🔄
Getters are methods used to retrieve the values of instance variables.

```java
public class Person {
    private String name;

    public String getName() {
        return name;
    }
}
```

### Constructors 🚧
Constructors are special methods used for initializing objects. They have the same name as the class and no return type.

```java
public class Person {
    private String name;

    public Person(String name) {
        this.name = name;
    }
}
```

### StringBuilder 🛠️
`StringBuilder` is a class used to create mutable strings, allowing for efficient string manipulation.

```java
StringBuilder sb = new StringBuilder();
sb.append("Hello");
sb.append(" World");
System.out.println(sb.toString()); // Outputs: Hello World
```




### toString Method 🖨️
The `toString` method is used to return a string representation of an object.

```java
public class Person {
    private String name;

    @Override
    public String toString() {
        return "Person{name='" + name + "'}";
    }
}
```



### Inheritance 🧬
Inheritance allows a class to inherit properties and behavior from another class. This promotes code reuse and establishes a parent-child relationship between classes.

```java
class Animal {
    void eat() {
        System.out.println("Animal is eating...");
    }
}

class Dog extends Animal {
    void bark() {
        System.out.println("Dog is barking...");
    }
}

Dog dog = new Dog();
dog.eat();  // Output: Animal is eating...
dog.bark(); // Output: Dog is barking...
```

### Interfaces 🌐
Interfaces define a contract for classes to implement. They contain method signatures that participating classes must define.

```java
interface Animal {
    void eat();
    void sleep();
}

class Dog implements Animal {
    @Override
    public void eat() {
        System.out.println("Dog is eating...");
    }

    @Override
    public void sleep() {
        System.out.println("Dog is sleeping...");
    }
}

Dog dog = new Dog();
dog.eat();  // Output: Dog is eating...
dog.sleep(); // Output: Dog is sleeping...
```

### Access Modifiers 🔒
Access modifiers control the visibility and accessibility of classes, methods, and variables.

```java
public class Example {
    private int privateVar;
    protected int protectedVar;
    int defaultVar;
    public int publicVar;
}
```

### Polymorphism 🎭
Polymorphism allows objects to be treated as instances of their parent class or interfaces, enabling flexibility and code reusability.

```java
class Animal {
    void makeSound() {
        System.out.println("Animal makes a sound");
    }
}

class Dog extends Animal {
    @Override
    void makeSound() {
        System.out.println("Dog barks");
    }
}

Animal animal = new Dog();
animal.makeSound(); // Output: Dog barks
```

### Casting Numerical Values 🔢
Casting allows you to convert a value from one data type to another.

```java
double d = 10.5;
int i = (int) d; // Explicit casting
System.out.println(i); // Output: 10
```

### Upcasting and Downcasting ⬆️⬇️
Upcasting involves casting a subclass type to a superclass type, while downcasting involves casting a superclass type to a subclass type.

```java
class Animal {}
class Dog extends Animal {}

Animal animal = new Dog(); // Upcasting
Dog dog = (Dog) animal;    // Downcasting
```

### Generics 🎁
Generics allow you to create classes, interfaces, and methods that operate on types specified at compile time.

```java
class Box<T> {
    private T content;

    public void setContent(T content) {
        this.content = content;
    }

    public T getContent() {
        return content;
    }
}

Box<Integer> box = new Box<>();
box.setContent(10);
int value = box.getContent();
System.out.println(value); // Output: 10
```

### Generics and Wildcards 🃏
Wildcards in generics allow flexibility in working with unknown types.

```java
List<?> list = new ArrayList<>();
list.add("Hello");
list.add(10);
```

### Anonymous Classes 🕶️
Anonymous classes allow you to create a class instance without explicitly defining a class name.

```java
Runnable r = new Runnable() {
    @Override
    public void run() {
        System.out.println("Anonymous class implementation");
    }
};
```

### Reading Files using Scanner 📄
The `Scanner` class can be used to read input from various sources, including files.

```java
try {
    File file = new File("example.txt");
    Scanner scanner = new Scanner(file);
    while (scanner.hasNextLine()) {
        System.out.println(scanner.nextLine());
    }
    scanner.close();
} catch (FileNotFoundException e) {
    System.out.println("File not found: " + e.getMessage());
}
```

### Handling Exceptions 🚨
Exception handling allows for graceful error handling in Java programs.

```java
try {
    // Code that may throw an exception
} catch (ExceptionType e) {
    // Handle the exception
} finally {
    // Code that runs regardless of whether an exception occurred
}
```

### Multiple Exceptions 🚨🚨
Multiple exceptions can be caught and handled in separate catch blocks.

```java
try {
    // Code that may throw an exception
} catch (ExceptionType1 e) {
    // Handle exception type 1
} catch (ExceptionType2 e) {
    // Handle exception type 2
}
```

### Runtime vs. Checked Exceptions 🕒🚨
Runtime exceptions (unchecked exceptions) do not need to be declared in a method's throws clause, while checked exceptions must be declared.

```java
// Runtime exception (unchecked)
int result = 10 / 0;

// Checked exception
try {
    // Code that may throw a checked exception
} catch (CheckedException e) {
    // Handle the checked exception
}
```

### Abstract Classes 🎨
Abstract classes cannot be instantiated and are used to provide a blueprint for subclasses to implement.

```java
abstract class Animal {
    abstract void makeSound();
}

class Dog extends Animal {
    @Override
    void makeSound() {
        System.out.println("Dog barks");
    }
}
```

### Reading Files With File Reader 📖
The `FileReader` class can be used to read characters from a file.

```java
try (FileReader reader = new FileReader("example.txt")) {
    int character;
    while ((character = reader.read()) != -1) {
        System.out.print((char) character);
    }
} catch (IOException e) {
    System.out.println("Error reading file: " + e.getMessage());
}
```

### Try With Resources 🔄
The try-with-resources statement ensures that resources are closed after the execution of the try block.

```java
try (BufferedReader reader = new BufferedReader(new FileReader("example.txt"))) {
    String line;
    while ((line = reader.readLine()) != null) {
        System.out.println(line);
    }
} catch (IOException e) {
    System.out.println("Error reading file: " + e.getMessage());
}
```

### Creating and Writing Text Files ✍️📄
Text files can be created and written to using classes like `FileWriter`.

```java
try (FileWriter writer = new FileWriter("output.txt")) {
    writer.write("Hello, world!");
} catch (IOException e) {
    System.out.println("Error writing to file: " + e.getMessage());
}
```

### The equals() Method 🔄
The `equals()` method is used to compare the equality of objects.

```java
String str1 = "Hello";
String str2 = "Hello";
System.out.println(str1.equals(str2)); // Output: true
```

### Inner Classes 🏠
Inner classes are classes defined within another class.

```java
class Outer {
    class Inner {
        void display() {
            System.out.println("Inner class");
        }
    }
}
```

### Enum Types - Basic and Advanced Usage 🏷️
Enums are special data types used to define collections of constants.

```

java
enum Day {
    MONDAY, TUESDAY, WEDNESDAY, THURSDAY, FRIDAY, SATURDAY, SUNDAY
}
```

### Recursion - A useful trick up your sleeve 🔁
Recursion is a programming technique where a function calls itself.

```java
int factorial(int n) {
    if (n == 0) {
        return 1;
    }
    return n * factorial(n - 1);
}
```

### Serialization - Saving Objects to Files 📁
Serialization is the process of converting objects into a byte stream, which can be saved to a file or transmitted over a network.

```java
class Person implements Serializable {
    String name;
    int age;
    // Constructor, getters, and setters...
}

try (ObjectOutputStream oos = new ObjectOutputStream(new FileOutputStream("person.ser"))) {
    Person person = new Person("John", 30);
    oos.writeObject(person);
} catch (IOException e) {
    System.out.println("Error serializing object: " + e.getMessage());
}
```

### Serializing Arrays 📦
Arrays can also be serialized in Java.

```java
int[] numbers = {1, 2, 3, 4, 5};

try (ObjectOutputStream oos = new ObjectOutputStream(new FileOutputStream("array.ser"))) {
    oos.writeObject(numbers);
} catch (IOException e) {
    System.out.println("Error serializing array: " + e.getMessage());
}
```

### ArrayList - Arrays the Easy Way 📝
`ArrayList` is a resizable array implementation in Java's collections framework.

```java
ArrayList<String> list = new ArrayList<>();
list.add("Apple");
list.add("Banana");
System.out.println(list.get(0)); // Output: Apple
```

### Linked Lists 🔗
Linked lists are data structures consisting of a sequence of elements, where each element points to the next one.

```java
LinkedList<String> list = new LinkedList<>();
list.add("Apple");
list.add("Banana");
System.out.println(list.getFirst()); // Output: Apple
```

### HashMaps - Retrieving Objects via a Key 🗝️
`HashMap` is a data structure that maps keys to values.

```java
HashMap<String, Integer> map = new HashMap<>();
map.put("apple", 10);
map.put("banana", 20);
int quantity = map.get("apple");
System.out.println("Quantity of apples: " + quantity);
```

### Sorted Maps 🗺️🔍
Sorted maps maintain their elements in ascending order based on the keys.

```java
SortedMap<String, Integer> map = new TreeMap<>();
map.put("apple", 10);
map.put("banana", 20);
System.out.println(map.firstKey()); // Output: apple
```

### Sets 🔗
Sets are collections that do not allow duplicate elements.

```java
Set<String> set = new HashSet<>();
set.add("Apple");
set.add("Banana");
System.out.println(set.contains("Apple")); // Output: true
```

### Using Custom Objects in Sets and as Keys in Maps 🗝️
Custom objects can be used as elements in sets and as keys in maps.

```java
class Person {
    private String name;
    private int age;
    // Constructor, getters, and setters...
}

Set<Person> set = new HashSet<>();
Map<Person, Integer> map = new HashMap<>();
```

### Sorting Lists 🔍
Lists can be sorted using the `Collections.sort()` method.

```java
List<Integer> list = new ArrayList<>();
list.add(3);
list.add(1);
list.add(2);
Collections.sort(list);
System.out.println(list); // Output: [1, 2, 3]
```

### Natural Ordering 🔄
Natural ordering refers to the ordering imposed by the `Comparable` interface's `compareTo()` method.

```java
class Student implements Comparable<Student> {
    int id;
    String name;
    // Constructor, getters, and setters...

    @Override
    public int compareTo(Student other) {
        return Integer.compare(this.id, other.id);
    }
}
```

### Queues 🚶‍♂️
Queues represent a collection of elements with first-in-first-out (FIFO) ordering.

```java
Queue<String> queue = new LinkedList<>();
queue.add("Apple");
queue.add("Banana");
System.out.println(queue.poll()); // Output: Apple
```

### Using Iterators 🔄
Iterators provide a way to access the elements of a collection sequentially.

```java
List<String> list = new ArrayList<>();
list.add("Apple");
list.add("Banana");

Iterator<String> iterator = list.iterator();
while (iterator.hasNext()) {
    System.out.println(iterator.next());
}
```

### Implementing Iterable 🔄
The `Iterable` interface allows objects to be iterated over using the enhanced for-loop.

```java
class MyCollection implements Iterable<String> {
    List<String> list = new ArrayList<>();

    @Override
    public Iterator<String> iterator() {
        return list.iterator();
    }
}
```

### Complex Data Structures 🏗️
Complex data structures involve combinations of basic data structures like arrays, lists, maps, and sets to solve more sophisticated problems.

<img align="center" src="https://github.com/shanibider/-Java-Basics/assets/72359805/dc2e7157-8c73-46b2-b519-be322cd3b86f">


---


## 📫 Connect with me 😊
[![linkedin](https://img.shields.io/badge/linkedin-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/shani-bider/)
[![portfolio](https://img.shields.io/badge/my_portfolio-000?style=for-the-badge&logo=ko-fi&logoColor=white)](https://shanibider.github.io/Portfolio/)
[![gmail](https://img.shields.io/badge/Gmail-D14836?style=for-the-badge&logo=gmail&logoColor=white)](mailto:shanibider@gmail.com)

<footer>
<p style="float:left; width: 20%;">
Copyright © Shani Bider
</p>
</footer>

## License📄

This project is licensed under the MIT License.

