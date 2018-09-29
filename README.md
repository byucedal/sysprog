# ch02intro
Introduction to OS, Chapter 02

Read [Introduction to OS](http://pages.cs.wisc.edu/~remzi/OSTEP/intro.pdf) and answer the following review questions.

1. What is an operating system? What does it do? 
The body of a software, which is responsible for making easier for programs to interact with hardware(like sharing memory), is called OS.
2. **What is virtualization? 
The primary way the OS behaves itself in system is through a general technique that we call virtualization.
3. How does an OS provide access to its features?
It provides some interfaces (APIs), that system calls in order to run programs. Sometimes we call them standard libraries for applications.
4. What illusion does a virtualized CPU provide? The illusion that the system has a very large number of virtual CPUs.  
    - How does this affect the user experience?  User will not sense that many programs are being performed by only one CPU.
    - How does this affect the developer experience?  It will help to developer to make time shorter to do task and divide big job into some small pieces.
    - What if the CPU were not virtualized? It would be much harder to perform several operations together. 
5. What is a memory address? To read memory, one must specify an address to be able to access
the data stored there; to write (or update) memory, one must also specify
the data to be written to the given address.
6. What is memory virtualization? Each process accesses its own private virtual address space, which the OS somehow maps onto the physical memory of the machine.
    - Why would we want this? It allows us to run programs in memory even if there is insufficient memory to begin with. This is the principle behind virtual memory  
8. What happens if you write a C/C++ program that writes past the end of an array?  It depends if the buffer was allocated on the stack or on the heap. It also depends on the computer architecture and it depends on the values that were written.
      - Can this affect other programs? The standard says that undefined behavior can mean anything, so you can't really have any expectations, not even with the same compiler. 
9. What is a thread? A thread is a part of the operating system, which is responsible for execution of only one instruction.
10. Why would we ever write a multi-threaded program? A multi-threaded application takes advantage of running multiple tasks at the same time to speed things up. Multithreading can also take advantage of multiple CPU machines.
11. What is atomicity? Atomic means that an operation is done without the chance for another thread to interrupt it and do something in the middle of it.
    - Is a C/C++ statement atomic? The C standard does not define whether it is atomic or not. In practice it shows it isn't.
    - Is a Java statement atomic? Most operations are indeed atomic. Operations involving 64 bit structures like double / long are not atomic by themselves. The 64 bit operation can be split into 2 32 bit operations.
    - Is an assembler statement atomic? You cannot assume one machine code will execute atomically. 
13. What does persistence mean? In system memory, data can be easily lost, as devices such as DRAM store values in a volatile manner; when power goes away or the system crashes, any data in memory is lost. Thus, we need hardware and software to be able to store data persistently.
14. How does OS hard drive virtualization differ from CPU & memory virtualization? The OS does not create a private, virtualized disk for each application. Rather, it is assumed that often times, users will want to share information that is in files. 
15. How does running multiple programs at the same time increase CPU efficiency? 
Instead of just running one task at a time, the OS would load a lot of tasks into memory and switch between them, which improves CPU utilization. 
16. What is multiprogramming? Multiprogramming is a parallel processing in which several programs are run at the same time on a single processor.
