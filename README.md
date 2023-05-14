# Stack-Trace

## What is Stace Trace?
* Also called a BACKTRACE or STACK TRACE, consists of a collection of stack records, which store an application's movement during its execution. 
* The stack trace includes information about program subroutines and can be used to debug or troubleshoot and is often used to create log files.
* Generates when your app crashes because of an error or an exception.

## Helpful Tips and Best Practices
* You can also print a stack trace at any point in your app code using methods such as Thread. dumpStack() 
* Can obtain a stack trace from a thread by calling the getStackTrace() method on the Thread instance. 
    * It returns an array of StackTraceElement, from which details about stack frames of the thread can be found.


## Stace Trace Examples
* Code Example - [ProcessFlowAutomation Request BusinessLayer](https://git.rockfin.com/Servicing/process-flow-automation-api/blob/main/ProcessFlowAutomationApi.BusinessLayer/RequestBusinessLayer.cs#L12)

