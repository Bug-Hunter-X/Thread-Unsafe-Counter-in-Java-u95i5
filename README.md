# Thread-Unsafe Counter in Java

This repository demonstrates a common concurrency bug in Java: an incorrect implementation of a counter class that is not thread-safe.  When multiple threads increment the counter simultaneously, race conditions can lead to inaccurate results. The counter's value will often be less than the expected total.

The `Counter.java` file contains the flawed counter implementation. The `Main.java` file shows how the bug manifests when multiple threads access the counter concurrently.

A solution is presented in the `CounterSolution.java` file to demonstrate how to fix the problem using appropriate synchronization mechanisms. The solution uses the `AtomicInteger` class which provides atomic operations for better thread safety.