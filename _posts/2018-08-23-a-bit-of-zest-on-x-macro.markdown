---
layout: post
title: A bit of zest on X-Macro
date: 2018-08-23T08:40:00Z
categories: jekyll update
---

Back in 1994 I came across a technique of generating C++ code through Macros. 

Macros in modern C++ are generally avoided like the plague by developers these days ... but they still have their uses even in modern code ... especially when memory is tight. 

I've used this pattern many times over the years but I have never had a name for it.

A colleague asked me to review some of their code the other day and I was surprised to see something very similar to the pattern I knew ... except I was stumped for a moment or two as to how it worked.

My colleague was using the [X Macro](https://en.wikipedia.org/wiki/X_Macro){:target="_blank"} technique.

My difficulty with the code was ... where is X defined ... I was scouring the list of #includes and the files to find it ... but I couldn't.

Then it dawned on me that it would just use X when instantiated and X would be replaced if it was also #defined somewhere ... then I searched for definitions of macro X ... low and behold I found loads of #defines and #undef of X all over the place along with lots of comments explaining what is happening ... because X is not a very discriptive name for a macro.

It works obviously ... but it was not the refined technique I knew ... and I was kind of left with the feeling that it was half defined.

The zest that I add for the world on the X Macro pattern is this ... and using the same terms as the X Macro wiki page above ... instead of ...

```cpp
#define LIST_OF_VARIABLES \
    X(value1) \
    X(value2) \
    X(value3)
```

... I do this ...

```cpp
#define LIST_OF_VARIABLES(X) \
    X(value1) \
    X(value2) \
    X(value3)
```

... but when I used it tend to be a bit more descriptive ... and I also tend to group many related things together ... to illustrate I use a familiar if artificial example ... in the definition of where I want to gather the related information I define a destributor that takes a selector ...

```cpp
#define EVENT_CODE_GENERATOR(SELECTOR) \
    SELECTOR(LeftMouseDown, LBUTTONDOWN, 0x0201) \
    SELECTOR(LeftMouseUp, LBUTTONUP, 0x0202) \
    SELECTOR(LeftMouseDoubleClick, LBUTTONDBLCLK, 0x0203)
```

... and then when it is used ... say to generate an enumeration definition ...

```cpp

#define EVENT_ENUMS(function, message, number) WM_##message=number, 

typedef enum { EVENT_CODE_GENERATOR( EVENT_ENUMS ) MaxEventNumber } Events;

```

This actually generates this code (ignoring whitespace)...

```cpp

typedef enum { WM_LBUTTONDOWN=0x0201, WM_LBUTTONUP=0x0202,
               WM_LBUTTONDBLCLK=0x0203, MaxEventNumber } Events;

```

... the beauty of this is that the EVENT_CODE_GENERATOR can be reused for many things like generating human readable strings or function definitions for these events ... and the SELECTOR parameter can be given a nice name that flows with the code in context around it.

A fuller example can be found at [Compiler Explorer](https://godbolt.org/z/QAl4Kv){:target="_blank"}