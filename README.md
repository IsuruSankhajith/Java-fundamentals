# Java Fundamentals

Welcome to the **Java Fundamentals** repository! This repository is designed to help beginners understand the core concepts of Java programming, starting from basic syntax to more advanced topics like Object-Oriented Programming (OOP), Exception Handling, and Multithreading.

## Table of Contents

1. [Introduction to Java](#introduction-to-java)
2. [Basic Concepts](#basic-concepts)
3. [Object-Oriented Programming (OOP)](#object-oriented-programming-oop)
4. [Exception Handling](#exception-handling)
5. [Collections Framework](#collections-framework)
6. [Input/Output (I/O)](#inputoutput-io)
7. [Multithreading](#multithreading)
8. [Memory Management](#memory-management)
9. [Advanced Java Topics](#advanced-java-topics)
10. [Best Practices](#best-practices)

### Introduction to Java

#### **Brief History of Java**
- **Origin:** Java was developed by Sun Microsystems in 1995. It was initiated as a project called "Oak" by James Gosling and his team, aiming to create a platform-independent language for embedded systems. 
- **Evolution:** After rebranding as Java, it quickly became popular due to its "write once, run anywhere" philosophy, which allows Java programs to run on any device with a compatible JVM.
- **Acquisition by Oracle:** In 2010, Oracle Corporation acquired Sun Microsystems and continues to develop Java, ensuring its relevance in modern software development.

#### **Features of Java**
- **Platform Independence:** Java code is compiled into bytecode, which can run on any device with a JVM, making it platform-independent.
- **Object-Oriented:** Java follows the principles of object-oriented programming (OOP), which include inheritance, polymorphism, encapsulation, and abstraction.
- **Simple:** Java's syntax is similar to C++, but with more straightforward features and fewer complexities like pointers and operator overloading.
- **Secure:** Java provides robust security features like bytecode verification, a secure runtime environment, and automatic memory management (garbage collection).
- **Multi-threaded:** Java supports multi-threading, allowing multiple threads to run concurrently, making it efficient for multitasking.
- **Robust:** Java emphasizes error checking during compile-time and runtime, reducing the chances of crashes and making it reliable.
- **High Performance:** Java's Just-In-Time (JIT) compiler enables high performance by converting bytecode into native machine code at runtime.
- **Dynamic:** Java is designed to adapt to an evolving environment, with runtime capabilities to load new classes and support dynamic linking.

#### **Java Development Kit (JDK), Java Runtime Environment (JRE), and Java Virtual Machine (JVM)**
- **JDK (Java Development Kit):**
  - The JDK is a software development kit used to develop Java applications. It includes the JRE, an interpreter/loader (Java), a compiler (javac), an archiver (jar), a documentation generator (Javadoc), and other tools needed for Java development.
  - The JDK is necessary for compiling Java source code into bytecode and for running Java programs.

- **JRE (Java Runtime Environment):**
  - The JRE is a subset of the JDK and provides the libraries, Java Virtual Machine (JVM), and other components to run applications written in Java.
  - It does not include development tools like a compiler or debugger. The JRE is used primarily to run Java applications on your machine.

- **JVM (Java Virtual Machine):**
  - The JVM is the heart of the Java programming language. It is responsible for converting the bytecode into machine-specific code and executing it.
  - The JVM provides platform independence, as the same bytecode can run on any operating system with a compatible JVM.
  - JVM also manages system memory and provides garbage collection, ensuring efficient memory usage.

This section provides a foundational understanding of Java, covering its origins, key features, and the tools involved in Java development and execution.

### Basic Syntax

#### **Structure of a Java Program**
A typical Java program consists of the following components:
- **Package declaration** (optional)
- **Import statements** (optional)
- **Class declaration**
- **Main method** (`public static void main(String[] args)`)
- **Statements inside the main method**

Example:
```java
public class HelloWorld {
    public static void main(String[] args) {
        System.out.println("Hello, World!");  // Prints message to console
    }
}
```

#### **Comments**
Java supports three types of comments:
1. **Single-line comment**: Begins with `//` and lasts for one line.
   ```java
   // This is a single-line comment
   ```
2. **Multi-line comment**: Starts with `/*` and ends with `*/`.
   ```java
   /* This is a multi-line comment.
      It spans multiple lines. */
   ```
3. **Documentation comment**: Used for generating documentation and starts with `/**` and ends with `*/`.
   ```java
   /**
    * This is a documentation comment.
    * It is used to describe methods and classes.
    */
   ```

#### **Data Types**
Java data types are divided into two categories:

1. **Primitive Data Types**: These are predefined by Java.
   - **byte** (1 byte)
   - **short** (2 bytes)
   - **int** (4 bytes)
   - **long** (8 bytes)
   - **float** (4 bytes)
   - **double** (8 bytes)
   - **char** (2 bytes, Unicode character)
   - **boolean** (`true` or `false`)

2. **Non-Primitive Data Types**: These are created by the programmer (objects, arrays, etc.).
   - Examples: String, Arrays, Classes, Interfaces

#### **Variables and Constants**
- **Variables**: Used to store data values. They must be declared before use.
   ```java
   int age = 25;
   String name = "Alice";
   ```
- **Constants**: Variables whose value cannot be changed once assigned. Declared using the `final` keyword.
   ```java
   final double PI = 3.14159;
   ```

#### **Operators**
1. **Arithmetic Operators**: Used to perform basic arithmetic operations.
   - `+` (Addition), `-` (Subtraction), `*` (Multiplication), `/` (Division), `%` (Modulus)

2. **Relational Operators**: Compare values and return a boolean result.
   - `==` (Equal to), `!=` (Not equal to), `>` (Greater than), `<` (Less than), `>=` (Greater than or equal to), `<=` (Less than or equal to)

3. **Logical Operators**: Perform logical operations and return boolean values.
   - `&&` (Logical AND), `||` (Logical OR), `!` (Logical NOT)

4. **Bitwise Operators**: Perform bit-level operations.
   - `&` (Bitwise AND), `|` (Bitwise OR), `^` (Bitwise XOR), `~` (Bitwise NOT), `<<` (Left shift), `>>` (Right shift)

5. **Assignment Operators**: Used to assign values to variables.
   - `=` (Simple assignment), `+=`, `-=`, `*=`, `/=`, `%=` (Compound assignment)

Certainly! Below is a comprehensive set of notes for **Section 3: Control Flow Statements** in Java Fundamentals. This section covers Conditional Statements, Looping Statements, and Branching Statements, complete with explanations and code examples to help you understand and apply these concepts effectively.

---

## Control Flow Statements

Control Flow Statements in Java determine the order in which statements are executed in a program. They allow you to control the flow of your program's execution based on certain conditions or repeatedly execute a block of code.

### 3.1 **Conditional Statements**

Conditional statements execute different blocks of code based on whether a specified condition is true or false. They are fundamental for making decisions within your program.

#### 3.1.1 `if` Statement

- **Syntax:**
  ```java
  if (condition) {
      // code to be executed if condition is true
  }
  ```
- **Description:** Executes the block of code only if the specified condition is `true`.

- **Example:**
  ```java
  int number = 10;
  if (number > 5) {
      System.out.println("Number is greater than 5.");
  }
  ```
  
#### 3.1.2 `if-else` Statement

- **Syntax:**
  ```java
  if (condition) {
      // code to be executed if condition is true
  } else {
      // code to be executed if condition is false
  }
  ```
- **Description:** Provides an alternative block of code to execute when the condition is `false`.

- **Example:**
  ```java
  int number = 3;
  if (number > 5) {
      System.out.println("Number is greater than 5.");
  } else {
      System.out.println("Number is 5 or less.");
  }
  ```

#### 3.1.3 `else-if` Ladder

- **Syntax:**
  ```java
  if (condition1) {
      // code
  } else if (condition2) {
      // code
  } else if (condition3) {
      // code
  } else {
      // default code
  }
  ```
- **Description:** Allows multiple conditions to be checked in sequence. Executes the block of the first `true` condition.

- **Example:**
  ```java
  int score = 85;
  if (score >= 90) {
      System.out.println("Grade: A");
  } else if (score >= 80) {
      System.out.println("Grade: B");
  } else if (score >= 70) {
      System.out.println("Grade: C");
  } else {
      System.out.println("Grade: F");
  }
  ```

#### 3.1.4 `switch` Statement

- **Syntax:**
  ```java
  switch (expression) {
      case value1:
          // code
          break;
      case value2:
          // code
          break;
      // more cases
      default:
          // default code
  }
  ```
- **Description:** Selects one of many code blocks to execute based on the value of an expression. Efficient for handling multiple discrete values.

- **Example:**
  ```java
  int day = 3;
  switch (day) {
      case 1:
          System.out.println("Monday");
          break;
      case 2:
          System.out.println("Tuesday");
          break;
      case 3:
          System.out.println("Wednesday");
          break;
      default:
          System.out.println("Invalid day");
  }
  ```

### 3.2 **Looping Statements**

Looping statements are used to execute a block of code repeatedly as long as a specified condition is met. They are essential for tasks that require repetition.

#### 3.2.1 `for` Loop

- **Syntax:**
  ```java
  for (initialization; condition; update) {
      // code to be executed
  }
  ```
- **Description:** Ideal for situations where the number of iterations is known beforehand.

- **Example:**
  ```java
  for (int i = 1; i <= 5; i++) {
      System.out.println("Iteration: " + i);
  }
  ```

#### 3.2.2 `while` Loop

- **Syntax:**
  ```java
  while (condition) {
      // code to be executed
  }
  ```
- **Description:** Continues to execute the block of code as long as the condition remains `true`. Best used when the number of iterations is not known.

- **Example:**
  ```java
  int i = 1;
  while (i <= 5) {
      System.out.println("Iteration: " + i);
      i++;
  }
  ```

#### 3.2.3 `do-while` Loop

- **Syntax:**
  ```java
  do {
      // code to be executed
  } while (condition);
  ```
- **Description:** Similar to the `while` loop, but guarantees that the block of code is executed at least once before the condition is tested.

- **Example:**
  ```java
  int i = 1;
  do {
      System.out.println("Iteration: " + i);
      i++;
  } while (i <= 5);
  ```

### 3.3 **Branching Statements**

Branching statements alter the flow of control by transferring execution to different parts of the program. They are used to exit loops or methods prematurely.

#### 3.3.1 `break` Statement

- **Description:** Terminates the nearest enclosing loop (`for`, `while`, or `do-while`) or `switch` statement and transfers control to the statement immediately following the loop or `switch`.

- **Example in a Loop:**
  ```java
  for (int i = 1; i <= 10; i++) {
      if (i == 5) {
          break; // Exit the loop when i is 5
      }
      System.out.println("i = " + i);
  }
  // Output: i = 1, i = 2, i = 3, i = 4
  ```

- **Example in a `switch`:**
  ```java
  char grade = 'B';
  switch (grade) {
      case 'A':
          System.out.println("Excellent!");
          break;
      case 'B':
          System.out.println("Good!");
          break;
      default:
          System.out.println("Invalid grade");
  }
  // Output: Good!
  ```

#### 3.3.2 `continue` Statement

- **Description:** Skips the current iteration of the nearest enclosing loop and proceeds with the next iteration.

- **Example:**
  ```java
  for (int i = 1; i <= 5; i++) {
      if (i == 3) {
          continue; // Skip the rest of the loop when i is 3
      }
      System.out.println("i = " + i);
  }
  // Output: i = 1, i = 2, i = 4, i = 5
  ```

#### 3.3.3 `return` Statement

- **Description:** Exits from the current method and optionally returns a value to the caller. It can be used to terminate the execution of a method at any point.

- **Example in a Method:**
  ```java
  public static int findFirstPositive(int[] numbers) {
      for (int num : numbers) {
          if (num > 0) {
              return num; // Exit the method and return the first positive number
          }
      }
      return -1; // Return -1 if no positive number is found
  }

  // Usage
  int[] nums = {-3, -2, 0, 4, 5};
  int firstPositive = findFirstPositive(nums);
  System.out.println("First positive number: " + firstPositive);
  // Output: First positive number: 4
  ```

---

## **Key Points to Remember**

1. **Conditional Statements:**
   - Use `if` when a single condition needs to be checked.
   - Use `if-else` when you have two possible paths.
   - Use `else-if` for multiple conditions.
   - Use `switch` for selecting among multiple discrete values, especially when dealing with enumerated types or constants.

2. **Looping Statements:**
   - Use `for` loops when the number of iterations is known.
   - Use `while` loops when the number of iterations is not known and depends on a condition.
   - Use `do-while` loops when the code block needs to execute at least once regardless of the condition.

3. **Branching Statements:**
   - Use `break` to exit loops or `switch` statements prematurely.
   - Use `continue` to skip the current iteration and proceed with the next one.
   - Use `return` to exit from methods, optionally returning a value.

4. **Best Practices:**
   - Ensure loop conditions eventually become `false` to avoid infinite loops.
   - Use `switch` statements for better readability when dealing with multiple discrete values.
   - Avoid excessive use of `break` and `continue` as they can make the code harder to follow.
   - Use meaningful conditions and ensure they are clear and maintainable.

---

## **Additional Examples**

### Example 1: Nested `if-else` Statements
```java
int age = 25;
double income = 50000.0;

if (age > 18) {
    if (income > 30000) {
        System.out.println("Eligible for loan.");
    } else {
        System.out.println("Income too low for loan.");
    }
} else {
    System.out.println("Not eligible due to age.");
}
```

### Example 2: Enhanced `for` Loop with `continue`
```java
int[] numbers = {1, 2, 3, 4, 5};
for (int num : numbers) {
    if (num % 2 == 0) {
        continue; // Skip even numbers
    }
    System.out.println("Odd number: " + num);
}
// Output: Odd number: 1, Odd number: 3, Odd number: 5
```

### Example 3: `switch` Statement with `enum`
```java
enum Day {
    MONDAY, TUESDAY, WEDNESDAY, THURSDAY, FRIDAY, SATURDAY, SUNDAY
}

public static void printDayType(Day day) {
    switch (day) {
        case SATURDAY:
        case SUNDAY:
            System.out.println(day + " is a weekend.");
            break;
        default:
            System.out.println(day + " is a weekday.");
    }
}

// Usage
printDayType(Day.MONDAY); // Output: MONDAY is a weekday.
printDayType(Day.SUNDAY); // Output: SUNDAY is a weekend.
```

---

### Methods

#### 4.1 **Defining Methods**
- **Syntax:**
  ```java
  returnType methodName(parameters) {
      // method body
  }
  ```
- Example:
  ```java
  public int add(int a, int b) {
      return a + b;
  }
  ```
  - `returnType`: The type of value the method returns (e.g., `int`, `void`).
  - `methodName`: Name of the method, following Java naming conventions.
  - `parameters`: Variables passed to the method (optional).
  - `method body`: Code block executed when the method is called.

#### 4.2 **Method Parameters and Return Types**
- **Parameters:**
  - Methods can accept input values called parameters.
  - Example:
    ```java
    public void greet(String name) {
        System.out.println("Hello, " + name);
    }
    ```
    - `String name`: A parameter of type `String`.

- **Return Types:**
  - The return type defines what data type the method will return.
  - If a method doesn't return anything, use `void`.
  - Example:
    ```java
    public int multiply(int x, int y) {
        return x * y;
    }
    ```
    - Return type: `int`, meaning the method returns an integer.

#### 4.3 **Method Overloading**
- Method overloading allows multiple methods to have the same name but different parameters (number, type, or both).
- **Key Points:**
  - Overloaded methods must differ in parameter list.
  - Return type alone cannot differentiate overloaded methods.
  
- Example:
  ```java
  public int add(int a, int b) {
      return a + b;
  }

  public double add(double a, double b) {
      return a + b;
  }

  public int add(int a, int b, int c) {
      return a + b + c;
  }
  ```
  - Here, the method `add()` is overloaded with different parameter types and counts.

#### 4.4 **Recursion**
- Recursion occurs when a method calls itself to solve a problem.
- **Key Points:**
  - Must have a base condition to avoid infinite recursion.
  - Useful for problems that can be divided into similar sub-problems (e.g., factorial, Fibonacci sequence).

- Example:
  ```java
  public int factorial(int n) {
      if (n == 0) {
          return 1; // Base condition
      } else {
          return n * factorial(n - 1); // Recursive call
      }
  }
  ```
  - In this example, the method calls itself to compute the factorial of `n`.

### Object-Oriented Programming (OOP) Concepts

#### 5.1 **Classes and Objects**
   - **Class**: A blueprint or template for creating objects. It defines attributes (fields) and behaviors (methods).
   - **Object**: An instance of a class. Objects hold the actual data and can perform actions defined by methods.

   ```java
   class Car {
       String model;
       int year;

       void displayInfo() {
           System.out.println("Model: " + model + ", Year: " + year);
       }
   }

   public class Main {
       public static void main(String[] args) {
           Car myCar = new Car();  // Creating an object
           myCar.model = "Toyota";
           myCar.year = 2020;
           myCar.displayInfo();
       }
   }
   ```

#### 5.2 **Constructors**
   - A special method that initializes objects of a class.
   - It has the same name as the class and no return type.
   - Can be **parameterized** or **non-parameterized**.
   
   ```java
   class Car {
       String model;
       int year;

       // Constructor
       Car(String m, int y) {
           model = m;
           year = y;
       }
   }
   ```

#### 5.3 **`this` Keyword**
   - Refers to the current instance of the class.
   - Used to avoid ambiguity between class attributes and method parameters.

   ```java
   class Car {
       String model;
       int year;

       Car(String model, int year) {
           this.model = model;  // Referring to instance variables
           this.year = year;
       }
   }
   ```

#### 5.4 **Inheritance**
   - Allows one class to inherit the properties and methods of another class.
   - Promotes code reuse and establishes a parent-child relationship.

   ```java
   class Vehicle {
       String fuelType;
   }

   class Car extends Vehicle {
       String model;
   }
   ```

#### 5.5 **`super` Keyword**
   - Refers to the parent class’s instance.
   - Used to call parent class constructors or methods.

   ```java
   class Vehicle {
       Vehicle() {
           System.out.println("Vehicle Constructor");
       }
   }

   class Car extends Vehicle {
       Car() {
           super();  // Calls parent class constructor
           System.out.println("Car Constructor");
       }
   }
   ```

#### 5.6 **Method Overriding**
   - Redefining a method in a child class that already exists in the parent class.
   - The overridden method should have the same name, parameters, and return type.

   ```java
   class Vehicle {
       void start() {
           System.out.println("Vehicle is starting");
       }
   }

   class Car extends Vehicle {
       @Override
       void start() {
           System.out.println("Car is starting");
       }
   }
   ```

#### 5.7 **Polymorphism**
   - The ability of an object to take many forms.
   - **Compile-time polymorphism** (Method Overloading) and **Runtime polymorphism** (Method Overriding).

#### 5.8 **Compile-time Polymorphism (Method Overloading)**
   - Method overloading happens when multiple methods have the same name but different parameters (type, number, or both).
   
   ```java
   class MathOperations {
       int add(int a, int b) {
           return a + b;
       }

       int add(int a, int b, int c) {
           return a + b + c;
       }
   }
   ```

#### 5.9 **Runtime Polymorphism (Method Overriding)**
   - Achieved through method overriding, where the method to be executed is determined at runtime based on the object type.

   ```java
   Vehicle myVehicle = new Car();
   myVehicle.start();  // Calls Car's start() method
   ```

#### 5.10 **Encapsulation**
   - The practice of bundling data (fields) and methods that operate on the data within a class and restricting access to them.
   - Achieved using **private** access modifiers and providing **getter** and **setter** methods.

   ```java
   class Car {
       private String model;
       
       public String getModel() {
           return model;
       }
       
       public void setModel(String model) {
           this.model = model;
       }
   }
   ```

#### 5.11 **Abstraction**
   - Hiding the implementation details and showing only essential information.
   - Achieved using **abstract classes** and **interfaces**.

   ```java
   abstract class Vehicle {
       abstract void start();
   }

   class Car extends Vehicle {
       void start() {
           System.out.println("Car is starting");
       }
   }
   ```

#### 5.12 **Interfaces vs Abstract Classes**
   - **Interface**: A contract that a class can implement. It only contains abstract methods (Java 8 allows default methods).
   - **Abstract Class**: Can have both abstract and concrete methods. Cannot be instantiated.

   ```java
   interface Drivable {
       void drive();
   }

   class Car implements Drivable {
       public void drive() {
           System.out.println("Driving a car");
       }
   }
   ```

### Exception Handling

Exception handling in Java is a mechanism used to handle runtime errors, ensuring the normal flow of the program isn't disrupted. Java uses `try`, `catch`, `finally`, `throw`, and `throws` keywords to handle exceptions.

#### 6.1 **Types of Exceptions**

- **Checked Exceptions**: 
  - These are exceptions that are checked at compile-time. If a method throws a checked exception, it must either handle the exception using a `try-catch` block or declare it using the `throws` keyword.
  - Examples: `IOException`, `SQLException`

- **Unchecked Exceptions**: 
  - These are exceptions that occur at runtime and are not checked during compilation. They are subclasses of `RuntimeException`. These don't need to be explicitly caught or declared.
  - Examples: `NullPointerException`, `ArrayIndexOutOfBoundsException`, `ArithmeticException`

#### 6.2 **try, catch, finally Blocks**

- **try block**: This block contains code that might throw an exception. The code within the `try` block is executed, and if an exception occurs, the control is passed to the `catch` block.

  ```java
  try {
      // Code that may throw an exception
  }
  ```

- **catch block**: This block catches the exception thrown by the `try` block and handles it.

  ```java
  catch (ExceptionType e) {
      // Handle the exception
  }
  ```

- **finally block**: This block is always executed, regardless of whether an exception is thrown or not. It's typically used for cleanup operations like closing a file or database connection.

  ```java
  finally {
      // Code that will always execute
  }
  ```

##### Example:

```java
try {
    int data = 50 / 0;  // This will throw ArithmeticException
} catch (ArithmeticException e) {
    System.out.println("Exception caught: " + e);
} finally {
    System.out.println("Finally block executed");
}
```

#### 6.3 **Throwing and Catching Exceptions**

- **throw keyword**: The `throw` keyword is used to explicitly throw an exception from a method or any block of code.

  ```java
  throw new ArithmeticException("Division by zero");
  ```

- **throws keyword**: When a method is capable of throwing an exception that it does not handle, it must declare it using the `throws` keyword in the method signature.

  ```java
  public void myMethod() throws IOException {
      // Code that may throw IOException
  }
  ```

#### 6.4 **Custom Exceptions**

Java allows you to create your own exceptions by extending the `Exception` class (for checked exceptions) or the `RuntimeException` class (for unchecked exceptions).

##### Example of a Custom Exception:

```java
class CustomException extends Exception {
    public CustomException(String message) {
        super(message);
    }
}

public class TestCustomException {
    public static void main(String[] args) {
        try {
            throw new CustomException("This is a custom exception");
        } catch (CustomException e) {
            System.out.println("Caught: " + e.getMessage());
        }
    }
}
```

In this example, `CustomException` is a user-defined exception that can be thrown and caught just like built-in exceptions.

### Java Collections Framework

#### **Overview of Collections**
The **Java Collections Framework (JCF)** provides a unified architecture for storing and manipulating groups of objects. It includes interfaces, classes, and algorithms to work with different types of collections such as lists, sets, and maps.

- **Collection**: The root interface for all the collections. It provides methods for adding, removing, and querying elements.
- **Collections Class**: A utility class that provides static methods to operate on collections (like sorting, searching).

#### **Key Interfaces in the Java Collections Framework**

1. **List Interface**  
   A **List** is an ordered collection that allows duplicate elements. It maintains insertion order and can be accessed by index.

   - **Implementations**: `ArrayList`, `LinkedList`, `Vector`
   - **Common Methods**:
     - `add(E element)`: Adds an element to the list.
     - `get(int index)`: Retrieves an element at the specified index.
     - `remove(int index)`: Removes an element at the specified index.
     - `size()`: Returns the number of elements in the list.

2. **Set Interface**  
   A **Set** is a collection that doesn't allow duplicate elements. It does not maintain the order of insertion (except for LinkedHashSet).

   - **Implementations**: `HashSet`, `TreeSet`, `LinkedHashSet`
   - **Common Methods**:
     - `add(E element)`: Adds an element if it is not already present.
     - `remove(Object o)`: Removes the specified element.
     - `size()`: Returns the size of the set.

3. **Map Interface**  
   A **Map** is a collection of key-value pairs. Each key is unique, and it maps to a single value. It does not inherit from `Collection`.

   - **Implementations**: `HashMap`, `TreeMap`, `LinkedHashMap`
   - **Common Methods**:
     - `put(K key, V value)`: Associates the specified value with the specified key.
     - `get(Object key)`: Retrieves the value for the given key.
     - `remove(Object key)`: Removes the key-value pair for the specified key.
     - `size()`: Returns the number of key-value mappings.

#### **Implementations of Collection Interfaces**

1. **ArrayList**  
   A resizable array implementation of the `List` interface. Provides fast random access but slow insertions and deletions in the middle.

   - Backed by an array.
   - Allows duplicates.
   - Dynamic resizing.

2. **LinkedList**  
   A doubly linked list implementation of `List`. It allows for faster insertions and deletions compared to `ArrayList` but slower random access.

   - Implements both `List` and `Deque` (supports FIFO and LIFO operations).
   - Allows duplicates.

3. **HashSet**  
   Implements the `Set` interface, backed by a hash table. It doesn't maintain the order of elements and allows `null` values.

   - Fast lookup and insertion.
   - Does not allow duplicates.

4. **TreeSet**  
   Implements `Set`, but maintains a sorted order of elements. It's backed by a Red-Black Tree.

   - Sorted order (natural or custom comparator).
   - Does not allow duplicates.

5. **HashMap**  
   An implementation of the `Map` interface, backed by a hash table. Provides fast access to key-value pairs but doesn't guarantee order.

   - Allows `null` keys and values.
   - Unordered.

6. **TreeMap**  
   Implements `Map` and maintains the keys in sorted order. Backed by a Red-Black Tree.

   - Keys are sorted.
   - Does not allow `null` keys.

#### **Iterators and Loops with Collections**

- **Iterator**: An object that allows traversal over elements in a collection one by one. It supports methods like `hasNext()`, `next()`, and `remove()`.
  - Example:
    ```java
    Iterator<String> iterator = list.iterator();
    while(iterator.hasNext()) {
        String element = iterator.next();
        // Process element
    }
    ```

- **Enhanced for Loop**: A simplified loop to iterate over collections or arrays.
  - Example:
    ```java
    for (String element : list) {
        // Process element
    }
    ```

- **ListIterator**: A specialized iterator for lists that allows bidirectional traversal.
  - Methods: `hasPrevious()`, `previous()`

This section will help in understanding how Java collections work and how to use them efficiently in Java programs.

Here’s a more detailed breakdown for your notes on **File Handling**, **Multithreading**, and **Java Input/Output (I/O)**:

---

### 8. **File Handling**
Java provides a robust way to handle files through classes in the `java.io` package.

#### a. **Reading and Writing Files**
   - **Reading Files**
     - `FileReader`: Used for reading character files.
     - `BufferedReader`: Wraps `FileReader` for efficient reading of large files or multiple lines.
     - Example: 
       ```java
       BufferedReader br = new BufferedReader(new FileReader("file.txt"));
       String line;
       while ((line = br.readLine()) != null) {
           System.out.println(line);
       }
       br.close();
       ```

   - **Writing Files**
     - `FileWriter`: Used for writing to character files.
     - `BufferedWriter`: Provides efficient writing by buffering output.
     - Example:
       ```java
       BufferedWriter bw = new BufferedWriter(new FileWriter("output.txt"));
       bw.write("Hello, World!");
       bw.close();
       ```

#### b. **Handling Input and Output (I/O) Streams**
   - **Byte Streams**: Handle I/O of raw binary data.
     - `FileInputStream` and `FileOutputStream`: Used to read and write raw bytes.
     - Example:
       ```java
       FileInputStream fis = new FileInputStream("input.bin");
       int data;
       while ((data = fis.read()) != -1) {
           System.out.print((char) data);
       }
       fis.close();
       ```

   - **Character Streams**: Handle I/O of characters (text).
     - `FileReader` and `FileWriter`: For character file I/O.

#### c. **Serialization and Deserialization**
   - **Serialization**: The process of converting an object into a byte stream to save to a file or transfer over a network.
     - Implement `Serializable` interface to allow a class to be serialized.
     - Example:
       ```java
       ObjectOutputStream oos = new ObjectOutputStream(new FileOutputStream("object.ser"));
       oos.writeObject(myObject);
       oos.close();
       ```

   - **Deserialization**: The process of converting the byte stream back into an object.
     - Example:
       ```java
       ObjectInputStream ois = new ObjectInputStream(new FileInputStream("object.ser"));
       MyClass obj = (MyClass) ois.readObject();
       ois.close();
       ```

---

### 9. **Multithreading**
Multithreading allows concurrent execution of two or more threads for maximum utilization of CPU.

#### a. **Creating Threads**
   - **Extending `Thread` Class**: Create a thread by extending the `Thread` class and overriding the `run()` method.
     - Example:
       ```java
       class MyThread extends Thread {
           public void run() {
               System.out.println("Thread is running");
           }
       }
       MyThread t1 = new MyThread();
       t1.start();
       ```

   - **Implementing `Runnable` Interface**: Another way to create a thread by implementing the `Runnable` interface.
     - Example:
       ```java
       class MyRunnable implements Runnable {
           public void run() {
               System.out.println("Thread is running");
           }
       }
       Thread t1 = new Thread(new MyRunnable());
       t1.start();
       ```

#### b. **Thread Lifecycle**
   - **New**: Thread is created but not yet started.
   - **Runnable**: After `start()` is called, the thread is ready to run.
   - **Running**: When the thread is actively executing.
   - **Blocked/Waiting**: When the thread is waiting for some condition or resources.
   - **Terminated**: When the thread completes execution.

#### c. **Synchronization**
   - Used to prevent thread interference and consistency problems when multiple threads try to access shared resources.
   - **Synchronized block/method**:
     ```java
     synchronized(this) {
         // critical section
     }
     ```

#### d. **Inter-thread Communication**
   - Threads can communicate using methods like `wait()`, `notify()`, and `notifyAll()`.
   - Example:
     ```java
     synchronized(obj) {
         obj.wait();   // thread waits
         obj.notify(); // wakes up waiting thread
     }
     ```

---

### 10. **Java Input/Output (I/O)**
Java provides powerful I/O classes in the `java.io` package for handling input and output operations.

#### a. **Streams (Byte Streams, Character Streams)**
   - **Byte Streams**: Handle binary data (e.g., images, files).
     - `InputStream` and `OutputStream`: Parent classes for byte-based I/O.
     - Example:
       ```java
       FileInputStream fis = new FileInputStream("input.txt");
       FileOutputStream fos = new FileOutputStream("output.txt");
       int data;
       while ((data = fis.read()) != -1) {
           fos.write(data);
       }
       fis.close();
       fos.close();
       ```

   - **Character Streams**: Handle character data (text).
     - `Reader` and `Writer`: Parent classes for character-based I/O.

#### b. **Reading and Writing Files**
   - Reading and writing character-based files using `FileReader` and `FileWriter`.
   - Buffered reading and writing using `BufferedReader` and `BufferedWriter`.

#### c. **Buffering**
   - **Buffered Streams**: Improve performance by reducing the number of I/O operations.
   - Example of buffered input:
     ```java
     BufferedReader br = new BufferedReader(new FileReader("file.txt"));
     String line;
     while ((line = br.readLine()) != null) {
         System.out.println(line);
     }
     br.close();
     ```

  Sure! Here's an explanation for each of the Java 8 features and best practices:

### **11. Java 8 Features**

**Lambda Expressions:**
- **Definition:** Lambda expressions provide a clear and concise way to represent one method interface using an expression. They are often used to implement functional interfaces.
- **Syntax:** `(parameters) -> expression` or `(parameters) -> { statements }`
- **Example:** `(a, b) -> a + b` defines a lambda expression that takes two parameters and returns their sum.

**Functional Interfaces:**
- **Definition:** An interface with exactly one abstract method. They can have multiple default or static methods.
- **Usage:** Functional interfaces are used as the basis for lambda expressions.
- **Example:** `@FunctionalInterface` annotation can be used to indicate that an interface is intended to be functional.
  ```java
  @FunctionalInterface
  public interface MyFunctionalInterface {
      void singleAbstractMethod();
  }
  ```

**Streams API:**
- **Definition:** The Streams API allows you to process sequences of elements (e.g., collections) in a functional style.
- **Key Methods:**
  - `filter()`: Filters elements based on a predicate.
  - `map()`: Transforms elements using a function.
  - `reduce()`: Aggregates elements using a binary operator.
  - `collect()`: Collects results into a collection.
- **Example:**
  ```java
  List<String> names = Arrays.asList("Alice", "Bob", "Charlie");
  List<String> filteredNames = names.stream()
                                    .filter(name -> name.startsWith("A"))
                                    .collect(Collectors.toList());
  ```

**Optional Class:**
- **Definition:** A container object which may or may not contain a value. It's used to avoid `null` checks and `NullPointerException`.
- **Key Methods:**
  - `of()`: Creates an Optional with a non-null value.
  - `empty()`: Creates an empty Optional.
  - `isPresent()`: Checks if a value is present.
  - `ifPresent()`: Executes a block of code if a value is present.
  - `orElse()`: Provides a default value if no value is present.
- **Example:**
  ```java
  Optional<String> optionalName = Optional.of("Alice");
  String name = optionalName.orElse("Default Name");
  ```

**Method References:**
- **Definition:** A shorthand notation of a lambda expression to call a method. It allows for cleaner and more readable code.
- **Syntax:** `ClassName::methodName` or `instance::methodName`
- **Example:**
  ```java
  List<String> names = Arrays.asList("Alice", "Bob", "Charlie");
  names.forEach(System.out::println);
  ```

**Default Methods:**
- **Definition:** Methods in interfaces that have a body. They provide default implementations that can be overridden by implementing classes.
- **Usage:** Allows you to add new methods to interfaces without breaking existing implementations.
- **Example:**
  ```java
  public interface MyInterface {
      default void defaultMethod() {
          System.out.println("This is a default method.");
      }
  }
  ```

### **12. Java Best Practices**

**Code Conventions:**
- **Definition:** Guidelines and rules for writing code to ensure readability and consistency.
- **Key Points:**
  - Follow naming conventions (e.g., camelCase for variables, PascalCase for classes).
  - Use proper indentation and spacing.
  - Keep methods short and focused on a single task.
  - Comment code where necessary to explain complex logic.

**Exception Handling Best Practices:**
- **Definition:** Guidelines for effectively handling exceptions to ensure robustness and maintainability.
- **Key Points:**
  - Use specific exceptions rather than generic ones.
  - Avoid catching `Throwable` or `Exception` unless absolutely necessary.
  - Always provide meaningful messages in exceptions.
  - Don’t swallow exceptions; always handle them appropriately or log them.
  - Use `try-with-resources` for automatic resource management.

**Effective Use of Collections:**
- **Definition:** Best practices for using Java Collections Framework efficiently.
- **Key Points:**
  - Choose the right collection type for your needs (e.g., `ArrayList` for fast access, `LinkedList` for frequent insertions/removals).
  - Use generics to ensure type safety.
  - Understand and use the differences between `List`, `Set`, and `Map`.
  - Use immutable collections where applicable.

**Writing Clean and Maintainable Code:**
- **Definition:** Practices for writing code that is easy to read, understand, and maintain.
- **Key Points:**
  - Follow Single Responsibility Principle (SRP) to ensure classes and methods have one reason to change.
  - Write self-explanatory code by using descriptive names and breaking down complex logic into smaller methods.
  - Refactor code regularly to improve readability and remove redundancy.
  - Use unit tests to ensure code correctness and facilitate refactoring.

This structure should give you a solid foundation for understanding and applying Java 8 features and best practices effectively.

1. Clone the repository:
    ```bash
    git clone https://github.com/your-username/java-fundamentals.git
    ```
2. Explore the `src/` folder for code examples on each topic.

## Contributing

Feel free to fork this repository and contribute by submitting pull requests. Please ensure that your code follows standard Java best practices.

## License

This repository is licensed under the MIT License. See the [LICENSE](LICENSE) file for more details.

