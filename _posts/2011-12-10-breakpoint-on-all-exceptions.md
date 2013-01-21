---
layout: post
title: 'Breakpoint on All Exceptions'
categories:
  - debugging
  - learn-ipad-book
  - xcode

---

In Chapter 9 of the book, I talk about an uncaught exception that will crash the app. Figure 9.4 shows the uncaught exception and the line of code that caused the exception. What I failed to mention is that you might need to set a breakpoint on all exceptions to see the offending line of code. If, for example, Xcode is highlight a line of code in main.m then you need to set a breakpoint on all exceptions.

To set a breakpoint on all exceptions, go to the Breakpoint navigator and click the + button found in the lower left corner. You can set the breakpoint for All, Objective-C, or C++ exceptions. You can also set the break option to On Throw or On Catch. The default settings (All exceptions and On Throw) is all you need to see the offending line of code.

<img src="/images/blog/2011-12-10/ExceptionBreakpoint-1.png" alt="ExceptionBreakpoint" border="0" width="600" height="326" />
