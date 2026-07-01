1. What is Java?

       Java is a high-level, object-oriented, class-based, platform-independent programming language developed by Sun
       Microsystems (now Oracle).
       Its primary goal was:"Write Once, Run Anywhere (WORA)"
       This means:
       Write Java Code
       ↓
       Compile to Bytecode
       ↓
       Run on any JVM
       ↓
       Execute on any OS
       Unlike C/C++, Java code is not compiled directly into machine code.

2. History of Java

       | Year | Event |
       | ---- | ------------------------ |
       | 1991 | Project Green started |
       | 1995 | Java officially released |
       | 2006 | Open source via OpenJDK |
       | 2014 | Java 8 released |
       | 2021 | Java 17 LTS |
       | 2023 | Java 21 LTS |

3. Why was Java Created?

       Before Java:

          C was powerful but unsafe
          C++ was complex
          Programs were platform dependent
          Memory management was manual
     
       Java solved this by providing:

          Platform independence
          Automatic garbage collection
          Object-oriented programming
          Better security
          Simpler syntax

4. Features of Java

   Simple

        Example:
            int age = 25;

   Object-Oriented

        Java supports:
          Encapsulation
          Inheritance
          Polymorphism
          Abstraction
        Example:
         class Car {
           void start() {
             System.out.println("Car started");
           }
         }

   Platform Independent

         C Program:
           Source Code
           ↓
           Compiler
           ↓
           Machine Code
         Java Program:
           Source Code
           ↓
           javac
           ↓
           Bytecode
           ↓
           JVM
           ↓
           Machine Code

   Secure

         Java provides:
           No pointers
           Bytecode verification
           Class loaders
           Security manager
           Sandboxing

   Robust

         Features:

            Exception handling
            Garbage collection
            Strong type checking
            Multithreaded

         Example:

            class MyThread extends Thread {
            
                public void run() {
                    System.out.println("Running");
                }
            
                public static void main(String[] args) {
                    new MyThread().start();
                }
            
            }

   Distributed

         Java supports:

            RMI
            Networking
            Web services
            REST APIs

   Dynamic

         Java supports:
         
            Reflection
            Dynamic class loading
            Runtime binding

5. Java Editions

   Java SE

       Used for:
       
        Core Java
        Desktop applications
        Utilities

       Examples:

        Collections
        Streams
        Concurrency

   Jakarta EE (formerly Java EE)

       Used for:

        Enterprise applications
        Web applications
        Microservices

       Examples:

        Servlets
        JPA
        JMS

   Java ME

       Used for:

        Embedded systems
        IoT devices

6. Java Ecosystem

        Java
        │
        ├── Core Java
        ├── Maven
        ├── Gradle
        ├── Spring Boot
        ├── Hibernate
        ├── JUnit
        ├── Docker
        ├── Kubernetes
        ├── PostgreSQL
        └── Cloud

7. First Java Program

       public class HelloWorld {

       public static void main(String[] args) {

            System.out.println("Hello Java");
       }
       }

8. What Happens Internally?

       HelloWorld.java
       ↓
       javac
       ↓
       HelloWorld.class
       ↓
       Class Loader
       ↓
       JVM
       ↓
       Execution Engine
       ↓
       Machine Code
       ↓
       CPU

Assignment

    Research and answer:

       Why was the language initially called "Oak"?
       Who invented Java?
       Why did Oracle acquire Java?
       Why is Java still popular after 30 years?
       What companies use Java today?

Revision Notes

    Java =
          High-level
          Object-oriented
          Platform-independent
          Robust
          Secure
          Portable
          Multithreaded
          Distributed
          Dynamic
    
    Compilation:

         .java
         ↓
         javac
         ↓
         .class
         ↓
         JVM
         ↓
         Machine Code