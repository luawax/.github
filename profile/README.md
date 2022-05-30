Axa Project
===========

Axa is a ecosystem development project that aims to create
libraries and tools to ease programming with Lua.


Why Lua?
--------
Lua has one of the simplest programming syntaxes, at the
same time that can emulate almost all programming paradigms. Also
is the scripting languages with lowest memory footprints.

Lua is only the core of language, with some very very basic standard
library. It has seriously good effects in how the Lua evolved:

* It is not the tail that shakes the dog - many languages with blurred
line between core language developers and standard library developers
has breaking changes in short cycle of years. These languages grows in
complexity and soon become heavy, complex and bloated. Lua is well
designed since its was first targeted to non programmers.

* It has long cycles of breaking releases - if you see the Lua timeline
of versions, you will see nearly haft to a decade in the great release
cycle. Even then, the differences are not so breaking ones. You have
confidence to work with Lua and even the version 5.1 (from 16 years ago)
are still being heavily used.


Why Axa?
--------
Lua community is great and grows each day, but lacks a referential point, that
means: 

* 5 or more modules about the same task, some of them:
  - or not well documented;
  - or not well designed (strange api, forced paradigms);
  - or not well maintained;

> It is frustrating start to use a library and feel insecure about how it
> will be maintained.

* the argument of do _it yourself_ kind:
  - copy and paste this snipped;
  - rewrite everywhere the same pile of boilerplate code;
  - the good practice is that makes you feel better;

> Also it is frustrating walk in circles without confidence about the next step.

Here emerge Axa, an attempt of:

* have the best implementation;
* have the simplest and intuitive usage;
* improve expressiveness;
* have good test coverage;
* be well documented;
* be previsible as the Lua core;


Philosophical Flame
-------------------

... or survival manual.

> 1. If you know where are you going, you will have more chances to find the
> path. If you know from where you came, you know how not to return.

* Where you want to go? Write a test to know if you arrived;
* What gone wrong? Write a test to not repeat the same mistake again;
* Why you came by that way? Well written tests are also documentation;


> 2. The traveller that doesn't map its progress needs to rediscover it again
> everyday.

Write good documentation, not outside code but _inside it_:

* Point the traps;
* Explain how to use and when not to use;
* Golden rule 1: Avoid to be so silent;
* Golden rule 2: Avoid to be merely a chatter;


> 3. Reforming is good, rebuild is not. If a house is built on good ground,
> with good foundations, you can reform it, improve it everyday. Otherwise
> anything will be breaking changes or lead to improvisation of crumbling roof
> and walls.

* Think before start (plan tests);
* Choose the right place (library, naming etc.);
* Chose the right material (smaller and robust dependencies);
* Do each thing at its time (write code to be time resistant);


> 4. You can do things with ten different tools... but if you choose to carry
> them all with you, you will soon be tired. Even if you choose one tool for
> each task you will still have all of them in your head, and perhaps
> familiarity with none of them.

* You can pay with life and pain if you want to carry it all;
* You can loose moment if you choose the wrong tool;
* Prefer the simpler, compact and multipurpose;


> 5. The hurry is the enemy of the advance. You may need to come back when you
> will be at the middle of the way or just break the bones and tumble in there;

Well... nothing should speak louder than advance. Even too much money should'nt
make the road shorter. Remember that you'll not the only one that will use
your software. Do it well, do it for the present and the future.


Roadmap
-------

#### Eos library

Characteristics:

* A single Luarock;
* Extends the Lua standard library;
* Have minimal dependencies (almost the same C libraries of Lua itself);
* Serve to support the most common development tasks;

Example of targetet tasks:

- TDD;
- File System;
- Shell facilities;
- Advanced string handling alternatives;
- Specific table handling (for lists and records);
- Functional programming helpers;
- Json parsing;
- Multithread and or paralelism;

The restriction to be on Eos library is have minimal dependences, i.e, use the
same C libraries that Lua uses itself and be target to the more core and common
tasks.


#### Comet libraries

Follows the Eos philophy of simplicity, but rather than be a single module
can be multiple ones.

Characteristics:

* Each module target one matter;
* Uses own naming for actions not being restricted to the dependencies names;
* Can implement diferent dependencies on different platforms but should always
yield the same consistent result;
* Can be refactored to well maintained dependency C libraries, but always
maintaining the same api (function names, arguments and values);


#### Exo libraries

Very peculiar to be standardized... basically the members of Exo class will be
external robust libraries but that have very peculiar properties and that cannot
be fully functional for all platforms.

Characteristcs:

* Specific domain tasks - not so common;
* Depencency targeted - it should be like a binding to use the library specific
abilities;
* 3rd part intuitive - the library upon the module works should be well;
documented, and the user should be capable of programming in Lua understanding
the 3rd party documentation (as well as module tests);
* Minimalism oriented - should be prioritized the libraries with some
similarity of the Axa project i.e. be simple, small, concise etc;

Examples:

* LibVips for image processing;
* Curl for general purpose url handling;
* Nuklear for agnostic graphical interfaces;

