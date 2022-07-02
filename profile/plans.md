Roadmap
-------

#### Eos library

Characteristics:

* A single Luarock;
* Extends the Lua standard library;
* Has minimal dependencies, basically present in any POSIX compliant system;
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

