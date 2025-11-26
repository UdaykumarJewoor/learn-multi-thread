# Multithreading and Concurrency (Java)

This repository contains simple and practical examples to help you understand multithreading and concurrency in Java.  
All examples are clear and beginner-friendly.

This project is still being updated and more examples will be added over time.

---

## Overview

This repository will help you learn:

- How to create threads in different ways  
- How threads work together  
- How to avoid common multithreading problems  
- How to improve performance using threads  
- How to safely share data between threads  
- How to use Java’s concurrency tools  

---

## Basics (Creating Threads)

- **Thread with Runnable**  
  Demonstrates how to create and run a thread using a Runnable.

- **Custom Thread class**  
  Shows how to extend the Thread class to create your own thread behavior.

- **UncaughtExceptionHandler**  
  Explains how to catch errors that occur inside a thread.

- **Bank Robbery Example**  
  A simple example where two threads try to guess a password while another thread monitors them.

---

## Thread Coordination

Examples that show how threads interact and wait for each other:

- **Interrupts**  
  How to stop long-running threads safely.

- **Manual interrupt checking**  
  Useful for loops or tasks that do not throw InterruptedException.

- **Daemon threads**  
  Threads that run in the background and stop automatically when the application ends.

- **join()**  
  Allows one thread to wait until another thread completes.

---

## Performance Optimization

### Performance Concepts

- **Latency**  
  Time taken to complete one task.

- **Throughput**  
  Number of tasks completed in a specific time period.

### Examples

- **Image Processing**  
  Shows the difference between single-thread and multi-thread performance.

- **HTTP Server with Thread Pool**  
  Demonstrates how thread pools improve performance when handling multiple requests.

---

## Data Sharing Between Threads

### Synchronized Usage

Two ways to control access to shared resources:

1. **Synchronized methods**  
   Only one thread can run the method at a time on the same object.

2. **Synchronized blocks**  
   Locks only the required part of the code (critical section).

Note: The synchronized mechanism is reentrant, meaning a thread can enter other synchronized blocks that it already owns.

---

### Atomic Operations

Operations that happen in a single, safe step:

- All object reference assignments  
- Primitive types such as int, short, byte, char, float, boolean

Not atomic:

- long  
- double  

Use the `volatile` keyword to make long and double atomic.

---

### Metrics Aggregation

Shows how to measure execution time of important operations, used for performance monitoring.

---

### Race Conditions

A race condition happens when:

- Multiple threads access the same shared data  
- At least one thread modifies the data  
- Improper timing leads to incorrect results  

Usually caused by non-atomic operations.

---

### Data Races

Happen when the compiler or CPU reorders instructions to improve performance, leading to unexpected results in multithreaded programs.

---

### Deadlocks

- **Deadlock example**  
  Shows how two threads can get stuck waiting on each other.

- **Deadlock prevention**  
  Techniques for avoiding deadlocks.

---

## Advanced Locking

### ReentrantLock

Provides more control than synchronized:

- Can check which thread owns the lock  
- Can check if other threads are waiting  
- Supports fair locking  
- Suitable for complex locking requirements

Examples:

- User interface reading and writing shared data  
- Read/Write locks for read-heavy operations

---

## Inter-Thread Communication

- **Semaphores**  
  Control access to limited resources.

- **Condition variables**  
  Allow threads to wait and notify each other.

- **Matrix Multiplication Example**  
  Demonstrates producer–consumer communication.

---

## Lock-Free Programming

Java provides atomic classes that help in writing lock-free code.

- **Lock-Free Stack**  
  A stack implementation that avoids locking and improves performance.

---

## Future Additions

More examples will be added, including:

- Executors and thread pools  
- Futures and callables  
- Concurrency utilities  
- Parallel streams  
- Advanced real-world scenarios  

---

## Contributions

Suggestions and contributions are welcome.  
This repository is created for learning and knowledge sharing.

