---
layout: post
title: 'Class Declaration versus Class Definition'
categories:
  - general
  - objective-c

---

A reader sent me an outstanding question. He pointed out that in chapter 4 of Learning iPad Programming, I wrote:

"To define a class you use @interface. In Listing 4.2, the CoinTosser class definition starts with the line @interface CoinTosser : NSObject. @interface is Objective-C syntax that tells the compiler that what follows is a class definition. CoinTosser is the name of the class. The colon character separates the class name from the name of the superclass. The new class inherits properties and methods from the superclass. The class definition starts with @interface and ends at the first occurrence of @end. This tells the compiler it has reached the end of the class definition."

The reader asked, "Shouldn't class definition be class declaration?" It turns out, class definition is correct.

While many programmers might use declaration and definition interchangeability, there are subtle differences in C and C++. And since Objective-C is a superset of C, those subtle differences apply.

A class <strong>declaration</strong> tells the compiler that a class exists. A class <strong>definition</strong> tells the compiler all the needed information to create an instance of the class. It tells the compiler about its member functions, properties, and so on. With Objective-C, the difference between class declaration and definition can be seen in the syntax.

<code>@class className</code> declares a class, so it's a class declaration. It tells the compiler the name of a class. This is also known as a "forward declaration."

<code>@interface className</code> and its contents defines the class, so it's a class definition.  It tells the compiler all it needs to know about the class, how to create an instance, what properties and methods are contained in the class, and so on.

Here are a couple of additional links that explain the differences as seen in C and C++:

<ul>
<li><a href="http://www.daniweb.com/software-development/cpp/threads/143198/difference-between-a-class-declaration-and-a-class-definition">http://www.daniweb.com/software-development/cpp/threads/143198/difference-between-a-class-declaration-and-a-class-definition</a></li>
<li><a href="http://www.cprogramming.com/declare_vs_define.html">http://www.cprogramming.com/declare_vs_define.html</a></li>
</ul>
