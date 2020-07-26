# PART 1: GETTING STARTED

* Introduction and Concepts
  * Join and Sleep
  * How Threading Works
  * Threads vs Process
  * Threading's Uses and Misuses
* Creating and Starting Threads
  * Passing Data to a Thread
  * Naming Threads
  * Foreground and Background Threads
  * Exception Handling
* Thread Pooling
  * Entering the Thread Pool via TPL
  * Entering the Thread Pool Without TPL
  * Optimizing the Thread Pool





## Thread Pooling
원문 : http://www.albahari.com/threading/#_Thread_Pooling

* Whenever you start a thread, a few hundred microseconds are spent organizing such things as a fresh private local variable stack.
* Each thread also consumes (by default) around 1 MB of memory.
* The **thread pool** cuts these overheads by sharing and recycling threads

* There are a number of ways to enter the thread pool:
 * Via the Task Parallel Library (from Framework 4.0)
 * By calling ThreadPool.QueueUserWorkItem
 * Via asynchronous delegates
 * Via BackgroundWorker

* There are a few things to be wary of when using pooled threads:
 * You cannot set the Name of a pooled thread
 * Pooled threads are always background threads
 * Blocking a pooled thread may trigger additional latency
 
 
 ### Entering the Thread Pool via TPL
 
 * You can enter the thread pool easily using the Task classes in the Task Parallel Library.
 
 
 
 
 


