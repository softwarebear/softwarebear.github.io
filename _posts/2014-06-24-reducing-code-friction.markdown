---
layout: post
title: Reducing code friction in mixed C and C++ cross platform projects
date: 2014-06-24T18:00:00Z
categories: jekyll update
---

So I've just inherited a very new project where part of the code is written in C and C++, a language I loved but put on the back burner about 12 years ago whilst I concentrated on C# ... I have kept up to date with it (C++11)  ... but it has amazed me how slooooow it is to develop code on this platform ... much slower than I remember ... especially when there is no code discipline in place.

Unfortunately the code I have inherited looks like it was written about 20 years ago ... rather than last year.

This frustrates me a lot as it's just lack of software crafting discipline that has got it into this state so quickly and resulted in code that is so viscous it's unbelievable.

Some things that we will be doing to help loosen the code up a bit :

### Unicode
Decide on your standard for text interchange.

UTF8 seems to be the most portable form across the various platforms we use (Win/Mac/Linux).

wchar_t changes size similarly to int, fantastic !

There are new types to combat this, std::u16string and std::u32string ... which may or may not be equivalent to std::wstring ... depending on your platform.

### Strings
std::basic_string<> is heavenly to most C++ programmers ... but those C lovers have their arrays of characters ... why would you need anything else ... ?

Maybe to avoid dealing with malloc and free or global statics with their threading issues, etc ?

### Premature Optimising
C/C++ dudes love optimising ... even extending it to the source code ... boy the compiler must be grateful.

What is the point of making something super optimal if it is only going to execute once per run or maybe a few times ... rather than billions of times per run ... prefer readable clear code and classes with nice encapsulation.

### Extern "C"
This is an abomination these days ... you only need this to talk to old libraries that you can't compile any more.

Prefer using .cpp files and compiling them with a C++ compiler, you get a better language environment and don't have to keep writing layers of crap to translate C++ down to C ... I thought you liked to optimise things ?

### Resharper
I've learnt a lot from the C# world, one tool that is slowly moving into the C++ world is Resharper ... heaven sent ... this product can currently navigate your code brilliantly ... it makes an attempt to do the other stuff that Resharper is excellent at ... it's still in development ... has some rough edges ... but given the amount I rely on this tool in C# ... it will be my best friend forever if they complete the C++ side.

Please give this tool your support ... give it a try ... feedback your findings to JetBrains.

### Posix
Do you write your system stuff with OS specific stuff and partition it off to separate platforms or use std stuff as much as possible ?

This depends on what you need to do obviously, but it becomes hard to keep all the builds in sync.

### Macros
It's easy to avoid macros ... especially with C++ templates. 

Absolutely no need for macros any more.

What about xplatform stuff though ... easy ... divide your libraries up into generic and OS specific parts ... declare everything in the generic ... define most of your stuff in the generic library ... define the specific stuff twice for each platform ... this forces you to think more about doing it and whether you can avoid it ... rather than just using a MACRO sledgehammer.

This leaves the code clean and readable ... not in a nested spaghetti of #ifdefs.

### SOLID Principles
Yes these apply to C++ too ... oh yes they do.

### TDD / Unit Testing
Get hold of a good Unit Testing library (GoogleTest, CppUnit ... there's lots of them).

Write unit tests.

Preferably before your implement anything.

Simples.