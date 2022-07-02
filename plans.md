# Plans

This document contains what Axa project plans to do. It is not a strict
roadmap, but serve to give the North to the project and collect interesting
wider to-do's.



## Libraries


### Eos

While scripting, most of time we need wide basic functions to handle from
strings to files, from math to communication. In this context Eos should
fit well.

Characteristics:

* A single Lua rock with a bunch of modules
* Extends the standard Lua library

Focus:

* System paths handling (parse, listing, changing)
* System users handling (get information from system users)
* Lua data handling (serialization and prettyfication)
* Tests (assertion and comparison tooling to improve tdd)
* Cryptography
* utf-8 (Lua string counterpart functions like `mb_*` of PHP)
* Basic paralelism
* Basic http communication
* Basic data format handling (CSV, JSON, XML/HTML, conf)
* Templating
- Functional programming helpers;
* FFI
* ...


### Aster

For tasks that go beyond basics. While Eos can be used in these scenarios, a
specialized library might be needed.

Example: a frontend representation of filesystem. While Eos and Lua standard
library can list files, get contents and properties etc. A specialized library
for UI can be used. This library could be developed following Eos patterns. It
would then be an Aster library.

Characteristics:

* Multiple Lua rocks.
* Each rock specialized in a theme containting multiple modules.

Some ideas:

* Specific format parsing (Jmespath, Yaml, Toml)
* Color math (RGB, RBGa, CYMK, HSL, HSV, LSB etc.)
* ...


### Echo

External library specific. Focus here is in most used libraries for diversified
tasks. It must follow Eos principles but are not "format of task" targeted, but
"tooling of task" targeted. I.e. while Eos and Aster focus on kind of task, Echo
focus on the tools. Here could have an `aster-curl` module, and an `aster-wget`
to do similar things but accordingly to the library-dependent capabilities.

Characteristics:

* External library dependent
* Must follow Eos interfaces.

Some ideas:

* LibVips for image processing;
* Curl for general purpose url handling;
* Nuklear for agnostic graphical interfaces;


## Tools

* `auge` - document generation from Markdown annotated Lua files containing
tests. Eos, Aster and Echo should have tests written in this format. The `auge`
tool will extract the documentation from these tests and generate markdown files
and possibly other files. At start, markdown is prefered due to ready usage on
project readme files.

* `luax` - basically a C header containing abstraction for most used Lua C API
tasks. While making C shorter, allows interchangeability between Lua versions,
good pratices folling Eos patterns.


