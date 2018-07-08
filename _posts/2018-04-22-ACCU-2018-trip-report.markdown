---
layout: post
title: ACCU 2018 trip report
date: 2018-04-22T12:00:00Z
categories: jekyll update
---

# Tuesday - Pre Conference Day 2018-04-18

## C++ 17 In Practice : Nicolai Josuttis
A fast and furious day of new C++ twists and turns, gotchas and interesting observations. 

The first thing that leapt out for me is that C++ is now on a strict 3 year revision cycle. It might surprise some of the younger readers that I didn’t know that, but prior to ’11 there was an 8 year gap back to ’03, then 5 years back to ’98 and then prior to that there were no international standards, but this means that major churn is happening in the language and we wrinkles need to keep up.

Towards the end we learned of some deprecations that people working on ’11+’14 need to be aware of, especially when they are deprecated because they didn’t work, not just because they were hard to understand.


The rest of the topics were out and out goodness that is already in most compilers today, so you have no excuse not to be learning this stuff.

# Conference dates Wednesday 2018-04-11 -> Saturday 2018-04-14

## Wednesday

### Diversity & Inclusivity in Tech : Gen Ashley
For a key note this was an all too short talk on Women in IT and Business in general, mostly showcasing what Gen Ashley is doing to help address the situation and maybe where females could get into STEM business, not to take away from her efforts and success, it said little about how females could stay in the business and progress beyond entry. 

Consequently this was followed by a lively series of questions and statements from the audience who I felt were all trying to offer our full support to our female colleagues.

It is a strange one for me, as in most of the companies I have worked for there have always been some strong females role models and 1E, my currently employer, a high proportion of females in the software engineering team and across the company as a whole, it is still not 50/50 but I have the privilege of working with multiple female engineers in all the product teams I’ve worked on.

This was where I made my first new contact at the conference, as a suggestion I made struck a chord with her too, she congratulated me for saying it and a little group formed around us at the end of the talk to continue on our joint themes. This lead to being introduced to more and more people that she knew over the week and having some engaging conversations, and me joining a another community.

### Fighting the controls : Daniele Procida
Because I had attended the day of C++17 which was quite intense (I still haven’t processed it all yet) I decided to try some different topics to feed my mind. 

Daniele’s talk was all about avoiding problems, fault analysis and how we are often misled during these tasks, by drawing a parallel between software engineering and the aerospace industry. Having learnt earlier in my career that it’s the missing pieces in the aftermath of a plane crash that are the important bits in figuring out what went wrong, I felt this would be good talk to attend.

It didn’t disappoint, the checks and balances that pilots have to go through from initiating the start sequence, take off, flight and landing to turning off the plane are immense. And when something goes wrong, the silly mistakes that we know the pilots have made in trying to resolve the situation, some could have been resolved by them sticking to procedure and just RTFM, or simply telling each other  they are doing and the other acknowledging by repeating what the other just said, a similar experience that we have in pair programming, which I don’t do enough of these days. 

The presented main aid to pilots for these situations are books of checklists for certain scenarios that they should follow to diagnose the issue to avoid the pilots panicking and loosing track of reality whilst worrying about killing the 300 passengers sitting behind them. 

A truly fascinating talk for those who have to deal with customer issues under pressure and those who write complex systems for others to use.

### Playing with Projections : Michel Grootjans
I learnt about CQRS and Eventing a long while ago, even before these were a thing, they were a thing. This session was more about insights into what meta data you can get from a simple Event Source as opposed to a database. Historical facts, auditing, rewinding time and spotting bottlenecks.

Only four people attended, so Michel came to sit with us and get our system building his code base and soon we were all analysing his event stream and spotting the diamonds amongst the rocks.

Michel had lots of different language versions of his app, but strangely no C++ for the ACCU conference, so I built him a C++ version that evening as a thank you for getting me a working Docker .Net Core running on my MacBook so we could build his C# app and rescue my attendance at the session. 

I just wanted to point to something! : Jonathan Müller
Jonathan took us through a proposal, he is building a template library for pointers, so that the our C++ code can be descriptive and more restrictive about what can be done with the pointer like objects. Quite a lot of cram into one talk, the intro was quite condensed but slowly it started to make sense as the talk went on. 

### Lightening Talks : Various
5 minute talks from lovely experienced and new presenters.

The one that stood out for me the most was one on Inclusivity and introduced a community that is slowly building a following, #include<C++>, an inclusive nurturing community for those having some interest in C++. The community is open to everyone, the biggest demands being those who can be welcoming, kind and look out for each other. They have a discord server with various other threads. 

## Thursday

### Kotlin/Native – Embracing existing ecosystems : Hadi Hariri
A strange one for a key note, but it was a good introduction and tour of the language. Kotlin seems infinitely flexible, even down to creating new language keywords on the fly, of course showcased all inside JetBrains IDE that make it all that much more easy to work with.

### Finally Executors for C++ : Detlef Vollmann
Three proposals are fighting it out for acceptance in the C++20 standard for the equivalent of promises for futures and asyncs that some might be familiar with already.

### Mocking Frameworks considered, harmful?! : Peter Sommerlad
Peter talked us through his views on various mocking frameworks and a home grown alternative, literally. Writing our own thin classes to stand in where we might use the mocking framework. Citing complexities in the macros behind the scenes that make it very hard to figure out what is wrong with the code using the traditional mocking frameworks for C++.


Personally I don’t find GMock so bad, yes it’s got hideous macros in it behind the scenes, but it does the job and I suspect we’d all end up building our own framework instead.

### C++ Countdown Pub Quiz : Jon Jagger
This might seem like taking a liberty on work time, but it does help with breaking down the barriers between people and getting to know each other, whilst figuring out how to write the smallest piece of C++ that uses exactly n specific well chosen C++ tokens that will compile using the given compiler (actually hosted in Cyber Dojo). 

For example you must use tokens ‘include’, ‘this’, ‘—‘, ‘virtual’ and ‘for’. A possible answer is shown to the right but is it the smallest; who knew you could decrement ‘this’, and what does this code do, does it break? Luckily that 'does it break' bit wasn't part of the quiz but is an interesting question. It was exciting, fun and a good way to break down barriers.

Cyber Dojo also runs a charity to teach children how to program in far flung lands who otherwise wouldn’t have access to computers.

### Lightning Talks : Various
I missed this session because by this point I was struggling with the lack of sleep due to staying up late the other evenings (or actually very early) coding and talking, well for me mostly being a listener, but engaging with the conversations around me where I could.

Besides I had to mentally prepare for the dinner too, which is quite an intense experience when one is a socially shy cautious bear at heart.

### Conference Dinner
A truly magical evening hosted by the utterly lovely ACCU Chair, Russel Winder, who held the whole week together perfectly.

A chance to reconnect to people I hadn’t spoken to yet from my ACCU 2013 visit and catch up with those I’d spoken to already and making some new contacts. 

Each course of the meal is held at a different table and we move around to mix and mingle the conversation, so it involves a lot of introductions and working at talking to each other. There was one awkward moment when the person to my right clearly wanted to ignore me, they and their friend hadn’t moved tables either, a bit of an alpha male love-in against the spirit of the event. It quite shocked him that I offered him and his friend some wine before pouring my own, I think he was expecting me to run away or ignore him back.

The other people that I spoke to were utterly lovely, and the last table I walked way over to the other side of the room and plonked myself down without looking at who was at the table. Turns out I sat next to the person I connected with at the first key-note and we continued our conversations.

## Friday

### The Shape of a Program : Lisa Lippincott

I’m quite spacial mentally and I’ve always visualised programs in my head as abstract shapes with connections and tunnels, recursions, zips, loops and so on … Lisa is a topological mathematician and presented an interesting view on computer programs and formally describing them in topological terms. 

### Linux User/Kernel ABI: Greg Law
A live kernel debugging session showing how C actually calls into the kernel and how user and kernel modes are protected, the proc filesystem and other intimate details of the layer below the main function and above those system entry points on the stack.

### C++ Today: The Beast is Back : Jon Kalb
This could maybe be titled “C++ from the Beginning to Today”, I suspect we might not have got to the end of what Jon had planned just because of the audience participation, but this is conference and this was a fantastic talk by Jon about the history revolving around C++, why and where it was built, how it has evolved over the intervening period and helped in so many different industries, strange quirks and anecdotes.

The fantastic four coding patterns of Continuous Delivery : Luca Minudel
I had some great hopes for this talk as at the time of writing I’m in the process of doing exactly this to Azure. Unfortunately for me the talk was about someone’s discovery of needing to do CI and CD, rather than pushing the boundaries of the topic, so I ducked out early and switched channel to …

### Cryptography for Programmers : Daniel James
… and learnt a thing or two about the various technologies that I don’t use now, but what particular problem they solved and hence their place in the evolution of cryptographic techniques, why they were compromised and what succeeded them. This helps to decode some of the strange acronyms that revolve around the various algorithms.

### Lightning Talks : Various
One talk stood out for me in this line up, one of the speakers stood up and gave an extremely brave talk about his mental breakdown a couple of years back due to the pressures he was under.  To be honest most of the detail of the speech has gone from my head, just the emotion remains, and this reminds me of another community I have grown into over the past 15 years since the death of my previous partner, who have a similar informal evening of sharing from whoever wants to perform whilst away on retreat/holiday.

At the time it was quite a profound speech that moved me to tears, mostly because I very narrowly avoided a similar situation myself so I know how easy it is to happen, but also I have a few friends that have also gone through the same thing, and my own brother took his own life over what I can only assume were acute and chronic work pressures for him, we have no other explanation.

### Bloomberg Event
By now it was obvious to me that I was struggling way too much with talking to people, potentially exposing my weaknesses in front of all these vastly clever intimidating people.

I hadn’t initially planned on attending this event, and there was a clear split in people who weren’t going along and those that were. A guy in the hotel reception pounced on me as I walked through wondering what to do next for the evening and asked whether I would be interested in playing a chess tournament. I replied that I can just about move the pieces in the right directions but was nowhere near able to compete at chess. This didn’t matter he said, it’s just a fun evening.

I was petrified almost, but I went along, I joined in, I moved the pieces, punched the clock, doing something I’ve seen but never done before. I failed with a checkmate at the first round, but hey, 32 people took part in the competition and exposed themselves in front of everyone else, there were about 50 others that didn’t. I achieved a small victory for myself.

Later the music started, some of the attendees grabbed guitars and another a laptop and suddenly there was a big jam going on with an computer program being altered live that was controlling all the hardware involved, the laptop screen relayed on a big screen for everyone to see, it was cool man. Some people have awesome talents.

More connections made and another successful and late night/early morning, it’s been a while since I’ve survived on three hours sleep a day.

## Saturday
### Creating an Incremental Architecture for your System : Giovanni Asproni
Another great speaker and a reassuring talk on the benefits of an Agile approach to software development. Agile has only came into my working life as a practice since I joined 1E, although I dabbled with eXtreme Programming when I was HoE about 14 years ago at a small company as the notion was first emerging.

### Hacker’s guide to Rust Programming : Vigneshwer Dhinakaran
Vigneshwer give a us an introduction to Rust, dubbed the Hacker’s guide I was expecting something quite low level and was constantly hearing that Rust is a system programming language, however all the examples that were given were actually quite high level apps, like web sites and file storage. Potentially the improvements they saw were from re-writing the app given the hindsight knowledge they had gained, not re-writing it in Rust.

It was my first insight into Rust, as I had only heard about it at the conference, so I raised the question buzzing around in my head, Vigneshwer had no experience of using Rust at the system level, so it was easy to forgive his skipping lightly over this. 

Luckily some members of the audience came over to speak to me later after the talk and explained some of the projects they are working on, mostly embedded hardware on micro controllers and they reassured me that Rust certainly is a language that can take you down to the required level, where your app is the operating system.  

### Turtles! Hill climbing! Hammers! Paper bags! : Frances Buontempo
I love Frances’ talks, she has a way of making what I know are vastly complex algorithms and notions simple to take in from the outset. The last talk I attended back in 2013 was on how to program our way out of a paper bag, for which we received certificates. This time it was how to get into the bag and find the cosiest place for our little turtle-bug to reside. The scenarios building to more and more complex models of a paper bag and swarms of ‘turtles’ all trying to solve the problem en-masse using various machine learning techniques. 

### Software development – learning to walk again : Seb Rose
Winding up the conference was Seb’s talk essentially about being Agile in the software industry because we don’t know what is around the next corner. Recounting the tales of a recent solo walking trip in the south of France, the big plans he made in anticipation of the excursion that became smaller and smaller as holiday time approached and realities kicked in, then mishaps along the way that caused changes of plans and adapting to the resources in the environment surrounding him when necessary.

# In conclusion

A wonderful close for me, as this was pretty much my experience of the conference, not what I planned beforehand, and many re-plannings along the way, and I failed to hold back the tears from the warmth and love I felt from everyone in the room for the ups and downs we get along the road in our software engineering careers.

