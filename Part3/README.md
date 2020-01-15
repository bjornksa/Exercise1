# Reasons for concurrency and parallelism


To complete this exercise you will have to use git. Create one or several commits that adds answers to the following questions and push it to your groups repository to complete the task.

When answering the questions, remember to use all the resources at your disposal. Asking the internet isn't a form of "cheating", it's a way of learning.

 ### What is concurrency? What is parallelism? What's the difference?
 > Concurrency means that several tasks are running in the same time period (not necessarily in the same instant), while parallellism means that the tasks are running at the exact same time.

 ### Why have machines become increasingly multicore in the past decade?
 > Technincal difficulties with increasing power of single core processors meant that using multithreading and other parallelisation techniques was a more viable option for increasing computational efficiency.

 ### What kinds of problems motivates the need for concurrent execution?
 (Or phrased differently: What problems do concurrency help in solving?)
 > Concurrency can help with embedded systems that interact with several sensors and actuators simultanously, OSes that must handle several applications or computation programs that require high speed

 ### Does creating concurrent programs make the programmer's life easier? Harder? Maybe both?
 (Come back to this after you have worked on part 4 of this exercise)
 > Concurrent programs gives the programmer a more flexible toolset, wich may help to solve some problems that are otherwise imposibble or very inefficient. It also seems to be able to cause a lot of headache and bugs.

 ### What are the differences between processes, threads, green threads, and coroutines?
 > - Processes are instances of computer programs, the execution of the code. (from wikipedia)
 > - The process consists of one or several threads, where all threads in one process share memory.
 > - Green threads are created on the user lever instead of the OS level and don't have access to native OS abilities
 > - Coroutines are similar to threads, but concurrent instead of parallell.

 ### Which one of these do `pthread_create()` (C/POSIX), `threading.Thread()` (Python), `go` (Go) create?
 > Threads

 ### How does pythons Global Interpreter Lock (GIL) influence the way a python Thread behaves?
 > The GIL is a lock that makes sure only one thread can access a particular resource at a given time

 ### With this in mind: What is the workaround for the GIL (Hint: it's another module)?
 > Using the multiprocessing module and creating processes instead of threads, each with their own interpreter allowing concurrency on multicore processors

 ### What does `func GOMAXPROCS(n int) int` change?
 > The number of threads available to threads allocated to the program.
