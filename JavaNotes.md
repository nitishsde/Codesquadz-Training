# Java Full Stack Development Notes

## Placement-Focused Notebook

**Scope:** Java, Spring Boot, MySQL, REST API, React.js, AWS and
Generative AI\
**Level:** Basic to Advanced\
**Format:** Theory → Code → Explanation → Placement Notes

------------------------------------------------------------------------

## Page 01 --- Java Introduction

### What is Java?

Java is a high-level, object-oriented, class-based programming language
designed to be portable across operating systems through the Java
Virtual Machine (JVM).

### Why Java is used in industry

-   Object-oriented programming
-   Platform independence
-   Strong ecosystem
-   Automatic memory management
-   Multithreading support
-   Large enterprise ecosystem
-   Spring and Spring Boot support
-   Strong database and API integration

### Important Java features

  Feature                Meaning
  ---------------------- ---------------------------------------------------
  Simple                 Easier syntax than many older languages
  Object-Oriented        Programs are organised around classes and objects
  Platform Independent   Bytecode runs on a JVM
  Robust                 Strong type checking and exception handling
  Secure                 Runtime and language-level security features
  Multithreaded          Supports concurrent execution
  Portable               Same bytecode can run on compatible JVMs
  High Performance       JIT compilation improves runtime performance

### Java execution flow

``` text
Java Source Code
      |
      v
   javac
      |
      v
Bytecode (.class)
      |
      v
     JVM
      |
      v
Operating System
```

### JDK, JRE and JVM

``` text
JDK
 |
 +-- JRE
      |
      +-- JVM
```

-   **JDK:** Tools required to develop and compile Java applications.
-   **JRE:** Runtime environment required to run Java applications.
-   **JVM:** Executes Java bytecode.

### Placement Questions

1.  What is Java?
2.  Why is Java platform independent?
3.  Difference between JDK, JRE and JVM.
4.  What is bytecode?
5.  What is the role of JVM?

------------------------------------------------------------------------

## Page 02 --- First Java Program

### Program

``` java
public class Main {

    public static void main(String[] args) {
        System.out.println("Hello, Java!");
    }
}
```

### Explanation

``` java
public class Main
```

Creates a class named `Main`.

``` java
public static void main(String[] args)
```

This is the standard entry point of a Java application.

-   `public` --- JVM can access the method.
-   `static` --- JVM can call it without creating a `Main` object.
-   `void` --- method returns no value.
-   `main` --- recognised entry-point method.
-   `String[] args` --- command-line arguments.

``` java
System.out.println("Hello, Java!");
```

Prints text to the console.

### Compile and run

``` bash
javac Main.java
java Main
```

### Output

``` text
Hello, Java!
```

### Placement Point

The file name should match the public class name:

``` text
Main.java
```

for:

``` java
public class Main
```

------------------------------------------------------------------------

## Page 03 --- Variables and Data Types

### Primitive data types

``` text
byte
short
int
long
float
double
char
boolean
```

### Example

``` java
public class Main {
    public static void main(String[] args) {

        int age = 22;
        double salary = 25000.50;
        char grade = 'A';
        boolean active = true;

        System.out.println(age);
        System.out.println(salary);
        System.out.println(grade);
        System.out.println(active);
    }
}
```

### Important

-   `int` is commonly used for whole numbers.
-   `long` is used for larger integer values.
-   `double` is commonly used for decimal values.
-   `char` stores one character.
-   `boolean` stores `true` or `false`.

### Placement Questions

-   Primitive vs non-primitive data types.
-   What is type casting?
-   What is the difference between `int` and `Integer`?

------------------------------------------------------------------------

## Page 04 --- Operators

### Main operator groups

``` text
Arithmetic
Relational
Logical
Assignment
Unary
Ternary
Bitwise
```

### Example

``` java
int a = 10;
int b = 5;

System.out.println(a + b);
System.out.println(a > b);
System.out.println(a > 5 && b < 10);
```

### Ternary

``` java
int age = 20;

String result = age >= 18 ? "Adult" : "Minor";

System.out.println(result);
```

------------------------------------------------------------------------

## Page 05 --- Control Statements

### if-else

``` java
int age = 20;

if (age >= 18) {
    System.out.println("Eligible");
} else {
    System.out.println("Not Eligible");
}
```

### switch

``` java
int day = 2;

switch (day) {
    case 1:
        System.out.println("Monday");
        break;

    case 2:
        System.out.println("Tuesday");
        break;

    default:
        System.out.println("Invalid day");
}
```

### Loops

``` java
for (int i = 1; i <= 5; i++) {
    System.out.println(i);
}
```

Placement focus:

-   `break`
-   `continue`
-   nested loops
-   loop complexity

------------------------------------------------------------------------

## Page 06 --- Methods

``` java
public class Calculator {

    static int add(int a, int b) {
        return a + b;
    }

    public static void main(String[] args) {
        int result = add(10, 20);
        System.out.println(result);
    }
}
```

### Method structure

``` text
access-modifier return-type methodName(parameters)
```

### Important concepts

-   Parameter
-   Argument
-   Return type
-   Method overloading
-   Static method
-   Instance method
-   Recursion

------------------------------------------------------------------------

## Page 07 --- Arrays and Strings

### Array

``` java
int[] numbers = {10, 20, 30, 40};

for (int number : numbers) {
    System.out.println(number);
}
```

### String

``` java
String name = "Nitish";

System.out.println(name.length());
System.out.println(name.toUpperCase());
System.out.println(name.charAt(0));
```

### Placement focus

Know the difference between:

``` text
String
StringBuilder
StringBuffer
```

Also understand why `String` is immutable.

------------------------------------------------------------------------

## Page 08 --- OOP: Class and Object

### Class

A class is a blueprint for creating objects.

### Object

An object is an instance of a class.

``` java
class Student {

    String name;
    int age;

    void display() {
        System.out.println(name + " " + age);
    }
}

public class Main {

    public static void main(String[] args) {

        Student student = new Student();

        student.name = "Nitish";
        student.age = 22;

        student.display();
    }
}
```

------------------------------------------------------------------------

## Page 09 --- Four Pillars of OOP

``` text
Encapsulation
Inheritance
Polymorphism
Abstraction
```

### Encapsulation

Keep data private and expose controlled methods.

``` java
class Account {

    private double balance;

    public void setBalance(double balance) {
        this.balance = balance;
    }

    public double getBalance() {
        return balance;
    }
}
```

### Inheritance

``` java
class Animal {
    void eat() {
        System.out.println("Eating");
    }
}

class Dog extends Animal {
    void bark() {
        System.out.println("Barking");
    }
}
```

### Polymorphism

Compile-time:

``` text
Method Overloading
```

Runtime:

``` text
Method Overriding
```

### Abstraction

Implemented mainly using:

``` text
abstract class
interface
```

------------------------------------------------------------------------

## Page 10 --- Constructor, this and super

### Constructor

``` java
class Student {

    String name;

    Student(String name) {
        this.name = name;
    }
}
```

### `this`

Refers to the current object.

### `super`

Refers to the parent class members.

Placement questions:

-   Constructor vs method
-   Default constructor vs parameterised constructor
-   `this` vs `super`

------------------------------------------------------------------------

## Page 11 --- Access Modifiers and Packages

``` text
private
default
protected
public
```

Typical visibility:

  Modifier      Same Class   Same Package         Child Class              Other Package
  ----------- ------------ -------------- ------------------- --------------------------
  private              Yes             No                  No                         No
  default              Yes            Yes   Package dependent                         No
  protected            Yes            Yes                 Yes   Yes, through inheritance
  public               Yes            Yes                 Yes                        Yes

### Package

``` java
package com.example.service;
```

Packages organise related classes and avoid naming conflicts.

------------------------------------------------------------------------

## Page 12 --- Exception Handling

``` java
try {
    int result = 10 / 0;
} catch (ArithmeticException e) {
    System.out.println("Cannot divide by zero");
} finally {
    System.out.println("Completed");
}
```

### Keywords

``` text
try
catch
finally
throw
throws
```

### Important distinction

-   Checked exceptions are checked by the compiler.
-   Unchecked exceptions generally occur at runtime.
-   `throw` explicitly throws an exception.
-   `throws` declares possible exceptions.

------------------------------------------------------------------------

## Page 13 --- Collections Framework

### Hierarchy

``` text
Collection
 |
 +-- List
 |    +-- ArrayList
 |    +-- LinkedList
 |
 +-- Set
      +-- HashSet
      +-- LinkedHashSet
      +-- TreeSet

Map
 |
 +-- HashMap
 +-- LinkedHashMap
 +-- TreeMap
```

### ArrayList

``` java
List<String> names = new ArrayList<>();

names.add("Java");
names.add("Spring");
names.add("React");

System.out.println(names);
```

### HashMap

``` java
Map<Integer, String> students = new HashMap<>();

students.put(101, "Nitish");
students.put(102, "Rahul");

System.out.println(students.get(101));
```

### Placement focus

Know:

-   ArrayList vs LinkedList
-   HashSet vs TreeSet
-   HashMap internal concept
-   Comparable vs Comparator
-   `equals()` and `hashCode()`

------------------------------------------------------------------------

## Page 14 --- Generics

``` java
List<String> names = new ArrayList<>();
```

Generics provide compile-time type safety.

``` java
class Box<T> {

    private T value;

    public void set(T value) {
        this.value = value;
    }

    public T get() {
        return value;
    }
}
```

------------------------------------------------------------------------

## Page 15 --- Java 8+ Features

### Lambda

``` java
List<Integer> numbers = List.of(10, 20, 30);

numbers.forEach(n -> System.out.println(n));
```

### Stream

``` java
numbers.stream()
       .filter(n -> n > 10)
       .forEach(System.out::println);
```

### Important topics

-   Lambda expressions
-   Functional interfaces
-   Stream API
-   Optional
-   Method references
-   Default methods
-   `Predicate`
-   `Function`
-   `Consumer`
-   `Supplier`

Placement focus:

Understand stream operations:

``` text
filter
map
sorted
distinct
limit
collect
reduce
forEach
```

------------------------------------------------------------------------

## Page 16 --- Multithreading

### Create a thread

``` java
class MyTask extends Thread {

    @Override
    public void run() {
        System.out.println("Task running");
    }
}

public class Main {

    public static void main(String[] args) {

        MyTask task = new MyTask();
        task.start();
    }
}
```

### Placement focus

-   Thread lifecycle
-   Runnable
-   Synchronization
-   Race condition
-   Deadlock
-   ExecutorService
-   Thread pool

------------------------------------------------------------------------

## Page 17 --- SQL and MySQL

### Basic SQL

``` sql
CREATE DATABASE company;

USE company;

CREATE TABLE employee (
    id INT PRIMARY KEY,
    name VARCHAR(100),
    salary DECIMAL(10,2)
);
```

### CRUD

``` sql
INSERT INTO employee VALUES (1, 'Nitish', 25000);

SELECT * FROM employee;

UPDATE employee
SET salary = 30000
WHERE id = 1;

DELETE FROM employee
WHERE id = 1;
```

### Placement focus

-   Primary key
-   Foreign key
-   Constraints
-   Joins
-   Group By
-   Having
-   Subqueries
-   Indexes
-   Normalization
-   Transactions
-   ACID

------------------------------------------------------------------------

## Page 18 --- SQL Joins

### INNER JOIN

Returns matching records.

``` sql
SELECT e.name, d.name
FROM employee e
INNER JOIN department d
ON e.department_id = d.id;
```

### Learn these joins

``` text
INNER JOIN
LEFT JOIN
RIGHT JOIN
SELF JOIN
CROSS JOIN
```

------------------------------------------------------------------------

## Page 19 --- JDBC

### Flow

``` text
Java Application
      |
      v
JDBC API
      |
      v
JDBC Driver
      |
      v
MySQL
```

### Example

``` java
Connection con = DriverManager.getConnection(
    "jdbc:mysql://localhost:3306/company",
    "root",
    "password"
);

PreparedStatement ps =
    con.prepareStatement("SELECT * FROM employee");

ResultSet rs = ps.executeQuery();

while (rs.next()) {
    System.out.println(rs.getString("name"));
}
```

Placement focus:

-   Connection
-   Statement
-   PreparedStatement
-   ResultSet
-   Transactions
-   SQL injection prevention

------------------------------------------------------------------------

## Page 20 --- HTML, CSS and JavaScript

### HTML

Learn:

``` text
Semantic HTML
Forms
Tables
Links
Images
Accessibility
SEO basics
```

### CSS

Learn:

``` text
Selectors
Box Model
Flexbox
Grid
Position
Responsive Design
Media Queries
Transitions
Animations
```

### JavaScript

Learn:

``` text
Variables
Functions
Arrays
Objects
DOM
Events
ES6+
Promises
Async/Await
Fetch API
Modules
```

Placement focus:

Do not stop at syntax. Build small applications.

------------------------------------------------------------------------

## Page 21 --- React.js

### Core topics

``` text
Components
JSX
Props
State
Events
Forms
Hooks
Routing
API Integration
Authentication
```

### useState

``` jsx
import { useState } from "react";

function Counter() {

    const [count, setCount] = useState(0);

    return (
        <button onClick={() => setCount(count + 1)}>
            {count}
        </button>
    );
}

export default Counter;
```

### Placement focus

Know:

-   Props vs state
-   `useState`
-   `useEffect`
-   Controlled components
-   React Router
-   API calls
-   Component reusability

------------------------------------------------------------------------

## Page 22 --- Servlet and JSP

### Servlet concepts

-   Servlet lifecycle
-   Request
-   Response
-   GET
-   POST
-   Sessions
-   Cookies
-   Filters

### JSP

-   JSP lifecycle
-   Expression Language
-   JSTL
-   MVC pattern

This section is useful for understanding the evolution from traditional
Java web applications to Spring Boot.

------------------------------------------------------------------------

## Page 23 --- Spring Framework

### Core concepts

``` text
IoC
Dependency Injection
Beans
ApplicationContext
Component Scanning
Configuration
```

### Example

``` java
@Service
public class UserService {

    public String getUser() {
        return "Nitish";
    }
}
```

### Important annotations

``` text
@Component
@Service
@Repository
@Controller
@Autowired
@Configuration
@Bean
```

------------------------------------------------------------------------

## Page 24 --- Spring Boot Introduction

Spring Boot simplifies development of production-oriented Spring
applications using auto-configuration, starters and embedded servers.

### Basic application

``` java
@SpringBootApplication
public class Application {

    public static void main(String[] args) {
        SpringApplication.run(Application.class, args);
    }
}
```

### Common project structure

``` text
src/main/java
|
+-- controller
+-- service
+-- repository
+-- entity
+-- dto
+-- exception
+-- config
|
+-- Application.java
```

------------------------------------------------------------------------

## Page 25 --- Spring Boot REST API

### Controller

``` java
@RestController
@RequestMapping("/api/users")
public class UserController {

    @GetMapping
    public String getUsers() {
        return "User list";
    }
}
```

### HTTP methods

``` text
GET
POST
PUT
PATCH
DELETE
```

### Status codes

``` text
200 OK
201 Created
204 No Content
400 Bad Request
401 Unauthorized
403 Forbidden
404 Not Found
409 Conflict
500 Internal Server Error
```

------------------------------------------------------------------------

## Page 26 --- Spring Boot CRUD

### Entity

``` java
@Entity
public class User {

    @Id
    @GeneratedValue(strategy = GenerationType.IDENTITY)
    private Long id;

    private String name;
    private String email;
}
```

### Repository

``` java
public interface UserRepository
        extends JpaRepository<User, Long> {
}
```

### Service

``` java
@Service
public class UserService {

    private final UserRepository repository;

    public UserService(UserRepository repository) {
        this.repository = repository;
    }
}
```

### Controller

``` java
@RestController
@RequestMapping("/api/users")
public class UserController {

    private final UserService service;

    public UserController(UserService service) {
        this.service = service;
    }
}
```

Placement focus:

Understand the flow:

``` text
Request
  ↓
Controller
  ↓
Service
  ↓
Repository
  ↓
Database
```

------------------------------------------------------------------------

## Page 27 --- JPA and Hibernate

### Important annotations

``` text
@Entity
@Id
@GeneratedValue
@Column
@OneToOne
@OneToMany
@ManyToOne
@ManyToMany
@JoinColumn
```

### Important concepts

-   ORM
-   Entity lifecycle
-   Lazy loading
-   Eager loading
-   Relationships
-   JPQL
-   Transactions
-   N+1 query problem

------------------------------------------------------------------------

## Page 28 --- DTO and Validation

### DTO

A DTO separates API request/response models from persistence entities.

``` java
public class UserRequest {

    private String name;
    private String email;
}
```

### Validation

``` java
@NotBlank
@Email
@Size
@NotNull
@Min
@Max
```

Placement focus:

Do not expose database entities blindly in every API. Learn DTO-based
API design.

------------------------------------------------------------------------

## Page 29 --- Exception Handling

### Global exception handler

``` java
@RestControllerAdvice
public class GlobalExceptionHandler {

    @ExceptionHandler(RuntimeException.class)
    public ResponseEntity<String> handle(RuntimeException ex) {
        return ResponseEntity
                .badRequest()
                .body(ex.getMessage());
    }
}
```

Benefits:

-   Consistent API responses
-   Cleaner controllers
-   Centralised error handling

------------------------------------------------------------------------

## Page 30 --- Spring Security and JWT

### Authentication flow

``` text
Login
  ↓
Validate Credentials
  ↓
Generate JWT
  ↓
Client Stores Token
  ↓
Client Sends Authorization Header
  ↓
Server Validates Token
  ↓
Protected API
```

### Important topics

-   Authentication
-   Authorization
-   Password hashing
-   JWT
-   Roles
-   Permissions
-   CORS
-   CSRF
-   Spring Security filters

------------------------------------------------------------------------

## Page 31 --- Git and GitHub

### Essential commands

``` bash
git init
git clone <url>
git status
git add .
git commit -m "message"
git push
git pull
git branch
git switch
git merge
```

### Professional workflow

``` text
Create branch
    ↓
Develop
    ↓
Test
    ↓
Commit
    ↓
Push
    ↓
Pull Request
    ↓
Code Review
    ↓
Merge
```

------------------------------------------------------------------------

## Page 32 --- Maven

### Maven project

``` text
pom.xml
src/main/java
src/main/resources
src/test/java
```

### Commands

``` bash
mvn clean
mvn compile
mvn test
mvn package
mvn install
```

### Important `pom.xml` areas

-   Project metadata
-   Dependencies
-   Plugins
-   Build configuration
-   Profiles

------------------------------------------------------------------------

## Page 33 --- AWS Fundamentals

### Cloud models

``` text
IaaS
PaaS
SaaS
```

### Important AWS services for a Java developer

``` text
EC2       -> Application server
S3        -> Object storage
RDS       -> Managed relational database
IAM       -> Identity and access
VPC       -> Networking
CloudWatch -> Monitoring
Route 53  -> DNS
ELB       -> Load balancing
```

------------------------------------------------------------------------

## Page 34 --- Deploy Spring Boot on AWS

### Basic architecture

``` text
GitHub
   |
   v
Build JAR
   |
   v
AWS EC2
   |
   v
Spring Boot
   |
   v
AWS RDS / MySQL
```

### Basic commands

``` bash
mvn clean package
```

Run the generated JAR:

``` bash
java -jar target/application.jar
```

### Deployment checklist

``` text
Build
Test
Configure environment variables
Configure security group
Deploy JAR
Start application
Configure database
Test API
Monitor logs
```

Never commit:

``` text
passwords
API keys
AWS credentials
JWT secrets
database credentials
```

------------------------------------------------------------------------

## Page 35 --- Generative AI Fundamentals

### AI hierarchy

``` text
Artificial Intelligence
        |
        v
Machine Learning
        |
        v
Deep Learning
        |
        v
Generative AI
        |
        v
Large Language Models
```

### Important concepts

-   LLM
-   Token
-   Context window
-   Prompt
-   Embedding
-   Vector database
-   RAG
-   AI API
-   Tool calling
-   Structured output

------------------------------------------------------------------------

## Page 36 --- GenAI Application Integration

### Full-stack AI architecture

``` text
React
  |
  v
Spring Boot
  |
  v
AI Provider API
  |
  v
LLM
  |
  v
Response
  |
  v
Spring Boot
  |
  v
React UI
```

### Example backend responsibility

``` text
Receive user prompt
       ↓
Validate request
       ↓
Apply application rules
       ↓
Call AI service
       ↓
Validate response
       ↓
Return structured response
```

### Placement focus

Understand the difference between:

``` text
Calling an AI API
        vs
Building an AI-powered application
```

A real application should handle authentication, validation, rate
limits, errors, logging, secrets and cost control.

------------------------------------------------------------------------

## Page 37 --- Full Stack Architecture

### Standard architecture

``` text
                  Browser
                     |
                     v
                React.js
                     |
                  HTTP/JSON
                     |
                     v
             Spring Boot API
                     |
              Controller
                     |
                  Service
                     |
                Repository
                     |
                 JPA/Hibernate
                     |
                     v
                  MySQL
```

### Cloud version

``` text
User
 |
 v
React Application
 |
 v
AWS
 |
 v
Spring Boot
 |
 v
RDS MySQL
```

------------------------------------------------------------------------

## Page 38 --- Placement-Level Projects

### Project 01 --- Student Management System

Features:

-   CRUD
-   Search
-   Pagination
-   MySQL
-   Spring Boot
-   React

### Project 02 --- E-Commerce Application

Features:

-   Registration
-   Login
-   JWT
-   Products
-   Categories
-   Cart
-   Orders
-   Admin
-   Payment integration concept
-   REST APIs

### Project 03 --- AI-Powered Application

Features:

-   User authentication
-   AI chat
-   Prompt handling
-   Chat history
-   Spring Boot API
-   React UI
-   MySQL
-   AI API integration

### Project 04 --- AWS Deployment

Deploy one complete project with:

``` text
React
Spring Boot
MySQL/RDS
AWS
GitHub
```

------------------------------------------------------------------------

## Page 39 --- DSA for Java Placement

### Must-know topics

``` text
Arrays
Strings
HashMap
HashSet
Linked List
Stack
Queue
Binary Search
Sorting
Trees
Heap
Graphs
Recursion
Backtracking
Greedy
Dynamic Programming
```

### Problem-solving patterns

``` text
Two Pointers
Sliding Window
Prefix Sum
Binary Search
Fast/Slow Pointer
Hashing
DFS
BFS
```

### Placement rule

Do not only read DSA theory.

For every topic:

``` text
Understand
   ↓
Implement in Java
   ↓
Solve Problems
   ↓
Analyse Complexity
   ↓
Review Mistakes
```

------------------------------------------------------------------------

## Page 40 --- Java Interview Quick Revision

### OOP

-   Encapsulation
-   Inheritance
-   Polymorphism
-   Abstraction

### Collections

-   List
-   Set
-   Map
-   Queue
-   HashMap
-   ArrayList

### Java Core

-   String
-   Exception handling
-   Multithreading
-   Java 8
-   JVM
-   Memory
-   Garbage Collection

### Spring Boot

-   IoC
-   DI
-   REST
-   JPA
-   Hibernate
-   Validation
-   Exception handling
-   Security
-   JWT

### Database

-   SQL
-   Joins
-   Indexes
-   Normalization
-   Transactions
-   ACID

### Project

Be ready to explain:

``` text
Problem
Architecture
Technology
Database
APIs
Authentication
Challenges
Solutions
Testing
Deployment
```

------------------------------------------------------------------------

# Placement Revision Order

When time is limited, revise in this order:

``` text
1. Java + OOP
2. Collections
3. Exception Handling
4. Java 8+
5. SQL + MySQL
6. Spring Boot
7. REST APIs
8. JPA + Hibernate
9. Spring Security + JWT
10. React fundamentals
11. Git + GitHub
12. AWS basics
13. Project architecture
14. DSA
15. GenAI integration
```

------------------------------------------------------------------------

# Final Full Stack Skill Map

``` text
JAVA
 |
 +-- OOP
 +-- Collections
 +-- Exception Handling
 +-- Multithreading
 +-- Java 8+
 |
 +-- JDBC
 |
 +-- SQL / MySQL
 |
 +-- Spring
 |
 +-- Spring Boot
 |      |
 |      +-- REST API
 |      +-- JPA
 |      +-- Hibernate
 |      +-- Security
 |      +-- JWT
 |
 +-- React.js
 |
 +-- Git / GitHub
 |
 +-- Maven
 |
 +-- AWS
 |
 +-- GenAI
 |
 +-- Full Stack Projects
```

------------------------------------------------------------------------

# Repository Structure

``` text
Java-Full-Stack-Training/
|
+-- 01-java-basics/
+-- 02-oop/
+-- 03-advanced-java/
+-- 04-collections/
+-- 05-exception-handling/
+-- 06-multithreading/
+-- 07-java-8-plus/
+-- 08-sql-mysql/
+-- 09-jdbc/
+-- 10-html-css/
+-- 11-javascript/
+-- 12-react/
+-- 13-servlet-jsp/
+-- 14-spring/
+-- 15-spring-boot/
+-- 16-rest-api/
+-- 17-jpa-hibernate/
+-- 18-security-jwt/
+-- 19-git-github/
+-- 20-maven/
+-- 21-aws/
+-- 22-genai/
+-- 23-full-stack-projects/
+-- 24-dsa/
+-- 25-interview-preparation/
|
+-- assignments/
+-- problem-statements/
+-- screenshots/
|
+-- README.md
+-- .gitignore
```

------------------------------------------------------------------------

# Learning Principle

``` text
Theory
  ↓
Code
  ↓
Practice
  ↓
Problem Solving
  ↓
Project
  ↓
GitHub
  ↓
Deployment
  ↓
Interview
```

**Goal:** Learn concepts well enough to explain them, implement them in
Java, use them inside a real application, and discuss the implementation
in an interview.

------------------------------------------------------------------------

## Author

**Nitish Singh**

B.Tech CSE\
Java Full Stack Development Training

Focus:

``` text
Java
Spring Boot
React.js
MySQL
REST APIs
AWS
Generative AI
DSA
```

GitHub: `https://github.com/nitishsde`
