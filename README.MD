> THIS PROJECT IS NOT MINE.  
SOURCE: [http://www.source-code.biz/snippets/java/RawConsoleInput/](http://www.source-code.biz/snippets/java/RawConsoleInput/)

RawConsoleInput - Read single characters from the console
---

The current Java JDK API does not allow reading single key strokes from the console. Console input is only supported in line mode. [JLine](https://github.com/jline/jline2) supports reading single keys, but not without blocking, and it's a large and complex package.

The RawConsoleInput class uses [JNA](http://en.wikipedia.org/wiki/Java_Native_Access) to call operating system functions of Windows and Unix/Linux.

Features:

* Allows reading single key strokes from the console.
* No automatic echoing of characters to the console output.
* Supports blocking and non-blocking input.
* Ctrl-C is received as a character code.
* Raw console input through RawConsoleInput and normal line-mode console input (e.g. using System.console().readLine()) can be mixed. But on Unix, resetConsoleMode() has to be called to switch the console back to normal input mode. 


Author: [Christian d'Heureuse](mailto:chdh@source-code.biz) ([www.source-code.biz](http://www.source-code.biz/), [www.inventec.ch/chdh](http://www.inventec.ch/chdh))
