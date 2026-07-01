Why This Chapter Is Important

    This topic is asked in almost every Java interview:

       What is JVM?
       Difference between JDK, JRE, and JVM?
       What is bytecode?
       How does Java become platform independent?
       How does Java execute internally?
       What is JIT Compiler?
       What are Class Loaders?

       If you understand this chapter deeply, you'll understand the foundation of Java itself.
1. What Happens When We Run a Java Program?

       Consider:
                public class HelloWorld {
                  public static void main(String[] args) {
                   System.out.println("Hello Java");
                  }
                }
       Execution flow:
                HelloWorld.java
                ↓
                javac compiler
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
       Unlike C/C++, Java never directly produces machine code.
2. What is JVM?
 
       Definition
           JVM stands for: Java Virtual Machine

       JVM is a virtual machine responsible for:

           Loading classes
           Verifying bytecode
           Managing memory
           Executing programs
           Performing garbage collection
       
       Important Point
     
           JVM is platform dependent.

       Examples:

           Windows JVM
           Linux JVM
           Mac JVM

           But:

           Java bytecode is platform independent.

       Responsibilities of JVM

          JVM performs:

             Class Loading
             Memory Management
             Garbage Collection
             Security
             Execution
             Optimization
             Thread Management

3. What is JRE?

       JRE means:

          Java Runtime Environment

          JRE contains:

           JRE
           |
           +---- JVM
           |
           +---- Core Libraries

       JRE can:

          ✅ Run Java programs

          JRE cannot:

          ❌ Compile Java programs

4. What is JDK?

       JDK means:

          Java Development Kit

       JDK contains:

          JDK
          |
          +---- JRE
          |
          +---- JVM

       JDK includes:

          javac
          java
          javadoc
          jar
          jdb
          jconsole
          jshell

Visual Representation

        JDK
          │
          ├── Compiler (javac)
          ├── Debugger
          ├── Documentation Tool
          ├── JRE
          │     │
          │     ├── JVM
          │     └── Libraries

Difference Table

| Feature            | JVM     | JRE   | JDK        |
| ------------------ | ------- | ----- | ---------- |
| Execute Java       | ✅       | ✅     | ✅          |
| Compile Java       | ❌       | ❌     | ✅          |
| Contains Libraries | ❌       | ✅     | ✅          |
| Contains JVM       | —       | ✅     | ✅          |
| Used By            | Runtime | Users | Developers |

5. What is Bytecode?
   
       Example:

             public class Test {
               public static void main(String[] args){
                 System.out.println("Java");
               }
             }

       Compile:

            javac Test.java

       Produces:

            Test.class

           This file contains: Bytecode

       Bytecode is:

            Platform independent
            Intermediate code
            Executed by JVM
            See Bytecode Yourself

       Run:

            javap -c HelloWorld

       Example:

           0: getstatic
           3: ldc
           5: invokevirtual
           8: return

6. Java Execution Process

       Step 1
          Write: Program.java
       Step 2
          Compile: javac Program.java
          Produces: Program.class
       Step 3
          Class Loader loads classes.
       Step 4
          Bytecode Verifier checks security.
       Step 5
          Execution Engine executes.

7. JVM Architecture

                         JVM
                          |
             --------------------------
             |            |           |
            Class Loader  Runtime      Execution
             Subsystem     Memory       Engine
                             |
                     --------------------
                     |        |         |
                     Heap    Stack   Metaspace

8. Class Loader Subsystem

        Class loaders load classes into memory.

        Three loaders exist:

        Bootstrap Loader

          Loads:

          java.lang.*
          java.util.*

        Extension Loader

          Loads:

          JDK extensions

       Application Loader

          Loads:

          Your own classes

       Example
          public class ClassLoaderDemo {

              public static void main(String[] args) {

                  System.out.println(
                      String.class.getClassLoader());

                  System.out.println(
                      ClassLoaderDemo.class.getClassLoader());
              }
          }

       Output:
          null
          jdk.internal.loader.ClassLoaders$AppClassLoader

9. Runtime Memory Areas

       JVM creates:

           Runtime Memory
           |
           ├── Heap
           ├── Stack
           ├── Metaspace
           ├── PC Register
           └── Native Method Stack

        We'll study these deeply in the JVM chapter.

10. Execution Engine

        The execution engine contains:

           Interpreter
           JIT Compiler
           Garbage Collector
           Interpreter Problem

        Interpreter:

           Reads line
           Executes line
           Reads line
           Executes line

           This is slow. JIT Compiler Solution

        JIT:

           Frequently used code
           ↓
           Compile to machine code
           ↓
           Store in cache
           ↓
           Reuse

           This makes Java fast.

Interview Questions

         1. What is JVM?
         2. Difference between JVM and JRE?
         3. Difference between JRE and JDK?
         4. Why is Java platform independent?
         5. What is bytecode?
         6. What is JIT compiler?
         7. Explain Java execution flow.
         8. What are class loaders?
         9. Why is JVM platform dependent?
         10. Explain Java architecture.

Revision Notes
       
                   HelloWorld.java
                         |
                         |
                       javac
                         |
                         |
                   HelloWorld.class
                         |
                         |
                    Class Loader
                         |
                         |
                  Bytecode Verifier
                         |
                         |
                     JVM Memory
                         |
                         |
                  Execution Engine
                   /            \
                  /              \
           Interpreter      JIT Compiler
                  \              /
                   \            /
                    Machine Code
                         |
                         |
                         CPU
                         |
                         |
                    Console Output

**JVM
=
Execution engine

JRE
=
JVM + Libraries

JDK
=
JRE + Development Tools

        Java Program
          ↓
        javac
          ↓
        Bytecode
          ↓
        Class Loader
          ↓
        JVM
          ↓
        Execution Engine
          ↓
        Machine Code

**Coding Exercise**

    Exercise 1

     Write a program that prints:

        Java version
        Vendor
        OS
        Architecture
        User name

    Exercise 2

     Execute:

      javap -c HelloWorld

      Analyze the bytecode generated.