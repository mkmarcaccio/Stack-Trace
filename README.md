# Stack-Trace

## What is Stace Trace?
* Also called a BACKTRACE or STACK TRACE, consists of a collection of stack records, which store an application's movement during its execution. 
* The stack trace includes information about program subroutines and can be used to debug or troubleshoot and is often used to create log files.
* Generates when your app crashes because of an error or an exception.
*  List of the method calls that the application was in the middle of when an Exception was thrown.
*  help software engineers figure out where a problem lies or how various subroutines work together during execution.

## Helpful Tips and Best Practices
* You can also print a stack trace at any point in your app code using methods such as Thread. dumpStack() 
* Can obtain a stack trace from a thread by calling the getStackTrace() method on the Thread instance. 
   * It returns an array of StackTraceElement, from which details about stack frames of the thread can be found.
* Technically, once a block of memory has been allocated on the stack, it cannot be easily removed as there can be other blocks of memory that were allocated before it. Each time a function is called in a program, a block of memory called an activation record is allocated on top of the call stack. Generally, the activation record stores the function's arguments and local variables
* chain of exceptions
   * applications will catch an Exception and re-throw it as the cause of another Exception.
   * What's different about this one is the "Caused by". Sometimes exceptions will have multiple "Caused by" sections. For these, you typically want to find the "root cause", which will be one of the lowest "Caused by" sections in the stack trace.
* Locate the root cause
* a list of Exceptions( or you can say a list of "Cause by")
   * Just like the reason we call it 'stack' is because stack is First in Last out (FILO), the deepest exception was happened in the very beginning, then a chain of exception was generated a series of consequences, the surface Exception was the last one happened in time, but we see it in the first place.
* A tricky and important thing here need to be understand is : the deepest cause may not be the "root cause", because if you write some "bad code", it may cause some exception underneath which is deeper than its layer. For example, a bad sql query may cause SQLServerException connection reset in the bottem instead of syndax error, which may just in the middle of the stack.
*  Another tricky but important thing is inside each "Cause by" block, the first line was the deepest layer and happen first place for this block. 


## Stace Trace Small Demo & Examples
* Demo on Fiddle - [Dotnetfiddle](https://dotnetfiddle.net/)
* Splunk Log Examples 
  * [ProcessFlowAutomation Request BusinessLayer](https://git.rockfin.com/Servicing/process-flow-automation-api/blob/main/ProcessFlowAutomationApi.BusinessLayer/RequestBusinessLayer.cs#L12)

## Possible Upgrade/Opportunity
* Ben.Demystifier
  * [Nick Chapsas Video](https://www.youtube.com/watch?v=JcnucGEaxLo&t=1s)
