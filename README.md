Multithreading and Concurrency

This repository contains simple examples to help you understand how multithreading and concurrency work in Java.
Even though the code is in Java, the ideas apply to most programming languages.

This project is still being updated.

About this Repository

I created this repository as a personal reference for learning how to build fast, scalable, and thread-safe applications.
It collects the basic concepts, common patterns, and performance techniques used in multithreading.

1. Creating Threads

This section covers different ways to create and run threads:

Using the Thread class and Runnable

Creating a custom Thread class

Setting an UncaughtExceptionHandler

A simple case study where two threads try to break a vault password while another thread tries to catch them

2. Thread Coordination

Examples that show how threads interact and how to control them:

Handling and checking interrupts

Using daemon threads

Using join to wait for a thread to complete

3. Performance Improvements

Basic performance terms:

Latency: time taken to complete one task

Throughput: tasks completed per time unit

Reducing Latency

Includes an example using image recoloring to compare sequential and multithreaded execution.

Improving Throughput

Shows how thread pools help reuse threads and handle many tasks efficiently.
Also includes an HTTP server example that uses a thread pool for heavy CPU work.

4. Sharing Data Between Threads

Covers safe ways to share data:

Synchronized (Monitors)

Synchronizing entire methods

Synchronizing only specific code blocks (critical sections)

Explanation of reentrant behavior

Atomic Operations

Most primitives are atomic except long and double

volatile can make long and double safe

Reference assignments are atomic

Measuring Code Performance

How to measure execution time of operations when running in production-like conditions.

5. Race Conditions and Data Races

Explains when race conditions occur:

Multiple threads access the same resource

At least one modifies it

Timing affects correctness

Also explains how compilers and CPUs can reorder instructions, which can lead to data races without proper synchronization.

6. Deadlocks

Explains how deadlocks occur and ways to prevent them by controlling lock order and avoiding circular waits.

7. Advanced Locking
Reentrant Locks

Offer more control than synchronized, such as checking lock ownership and waiting threads.

Read/Write Locks

Useful when many threads read data but only a few modify it.

Example

Shows a UI thread that reads data while a worker thread writes to the same shared resource.

8. Inter-Thread Communication

Ways threads communicate:

Semaphores

Condition variables

Producer–consumer example using wait and notify, including back-pressure logic for matrix multiplication

9. Lock-Free Techniques

Java provides lock-free atomic classes:

AtomicInteger

AtomicLong

AtomicReference

Includes an example of a lock-free stack which performs better than a blocking stack in many cases.
