---
date: '2022-4-7'
title: 'Programming Paradigms Learning Project'
excerpt: 'Starting my first public learning journal on learning different ways to program'
categories:
  - 'Programming Paradigms'
  - 'Learning Journal'
  - 'Road map'
# updated:
---

# The Goal
Out of all the passions I have in life, programming is the one that has the deepest rabbit hole when it comes to learning.  Not only can you apply programming to many different fields, not only are there countless different languages to write in, but there are also many different paradigms that you can use to solve the same problem!  Looking for solutions from different angles is one of the skills I feel that sets me apart from others in this field.  To me, there is no better feeling that coming up with a novel solution to a problem.  This is the reason I try to think about every problem from every angle I can think of.

That is why it has been a goal of mine for too many years to learn as many different programming paradigms as I can.  Everyone knows about procedural programming, since that is just a list of instructions in order.  Most people know about object oriented programming, since the world seems to be mostly coded in that style.  Many others at least know of functional programming, even if they can't explain what a monad is.  But how many people know of and are well versed in agent-oriented, array-oriented, automata-based, logic-based, or flow-based programming paradigms?  Maybe using these less popular methods of programming can yield valuable insights on how to fix the problems out there.

In short: my goal is to learn as many different paradigms in languages that are designed for them in order to see problems in as many different lights as possible.

# Learning Journal Technique

As someone who has kept a journal since I was 19 years of age, the practice of keeping records of your thought process in chronological order is a very useful for me.  It let's me see how my mind was forming the ideas that are now crystallized, shows me what I might have gotten wrong (and when/why I thought that), and gives me something to reference later when I inevitably forget details.  Applying this technique to projects that require a lot of hard topics has always been the best way for me to learn new things.  

By making this process public, I hope to help the internet strangers who stumble upon my site solidify their own knowledge about these topics.  Who knows, maybe this website will one day become a resource that's linked to if I do a good job of explaining these topics.  Developer logs on Youtube are already a popular genre with the programming nerds.  Considering how [Handmade Hero](https://handmadehero.org/), a developer log about creating a video game from scratch in C, inspired people to make an entire community called [The Handmade Network](https://handmade.network/) about other similar projects exists shows the power of putting out your learning process into the world.  

# The Road Map

Below is the table of paradigms and languages that I will be working on during this learning process.  None of this is currently set in stone, and like all good projects, is subject to change if better information becomes available later.

| Paradigm         | Language(s)    |
| :--------------- | :------------- |
| Procedural       | C              |
| Object Oriented  | Smalltalk      |
| Functional       | Haskell        |
| Meta Programming | Lisp (Clojure) |
| Event Driven     | Elm            |
| Logic Based      | Prolog         |
| Concurrent       | Go             |
| Array Based      | Odin           |
| Agent Based      | Erlang/Elixir  |
| Role Based       | ???            |
| Automata Based   | ???            |
| Flow Based       | ???            |
| Data Driven      | ???            |

# First Project: Cross Platform GUI in C

When it comes to doing a project with C, there are way too many options out there.  C is a language that can compile down to pretty much any machine large or small, is the bases for operating systems and hardware drivers, and is the closest thing to machine language without dipping into the assembly world.  Really, any program can be written in C if I really wanted to try.  With that in mind, I chose to produce a cross platform GUI application that will satisfy the following requirements: 

- Work on any machine running Linux, Windows, MacOS, or Android.
- Access the file system to load/save data.
- Request data from a server using HTTP.

I'm under the impression that building a cross platform system in pure C is not that easy, which is one of the reasons older Microsoft Products do not work on Linux/Mac and most newer products built these days are using a web framework like ElectronJS.  I want to understand why that is, and see if it's still possible to build a performant program with a small memory footprint without hating life afterwards.  The reason for the HTTP request requirement due to my guess of running into security concerns when asking the OS to retrieve files from an unknown source.  How different OS's deal with that, and how I can make sure that happens appropriately from scratch is another challenge I wish to encounter.  

# Follow Along Shortly

I'll be posting my progress in the [Learning Journal page](https://www.6pakal.com/learning-journal) of this website.  Currently it's not built yet since I still have to create the sidebar and layout to properly organize notes so users don't have to tear their hair out searching for relevant information, but I do hope to have it up by the end of next week.  If you're interested please follow along and enjoy!