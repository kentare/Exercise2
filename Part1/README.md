# Mutex and Channel basics

### What is an atomic operation?
>  An atomic operation an operation inside the processor so it can simultanously read and write to the same memory location on the same bus. This prevents other processes or i/o devices to write to the same memory at the same time.
### What is a semaphore?
> A semaphore is a tool to prevent race conditions.

> A semaphore is a variable that grant access to e collection of resources. It has K keys (an integer), and if a thread wants to do something with these resources, it gets a key. With a key it can access one of the resources. If there is no key available, the thread must wait.
A semaphore use primarily two actions: wait() - decrement key variable by 1, and signal() - increment key variable by 1
There are two types of semaphore: Counting semaphore (as the one mentioned above) and Binary Semaphore (which is similar, but not exactly as, a Mutex)

### What is a mutex?
> A Mutex (Mutual Exclusion) is a tool for preventing race conditions.

> A mutex has ownership over a resource, prevents that two threads do not access the same resource at the same time.

### What is the difference between a mutex and a binary semaphore?
> The main difference is the principle of ownership. When a thread locks a mutex (gets access to the resource), then only that thread can unlock the resource again. If another thread tries to unlock a resource it hasn't locked, it will receive an error. Binary semaphores only signals that a resource is ready to be used.

### What is a critical section?
> The critical section is the the period when a shared resource is accessed and protected.

### What is the difference between race conditions and data races?
 > Race conditions are a general term for flaws in the timing or the ordering of execution in the computer that leads to unwanted results. Race Conditions are often non-dermenistic.

 > Data races are a specific form for race condition where two or more threads in a single process access the same memory location concurrently. One of the threads must be writing and the threads are not using mutex to access the resource.

### List some advantages of using message passing over lock-based synchronization primitives.
> *Your answer here*

### List some advantages of using lock-based synchronization primitives over message passing.
> *Your answer here*
