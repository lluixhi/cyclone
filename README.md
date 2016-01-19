[<img src="docs/images/cyclone-logo-04-header.png" alt="cyclone-scheme">](http://github.com/justinethier/cyclone)

Cyclone is an experimental Scheme-to-C compiler that uses a variant of the [Cheney on the MTA](http://www.pipeline.com/~hbaker1/CheneyMTA.html) technique to implement full tail recursion, continuations, generational garbage collection, and native threads. Unlike previous Cheney on the MTA compilers, Cyclone allows execution of multiple native threads. A tracing garbage collector is used to manage the second-generation heap and perform major collections without "stopping the world".

Getting Started
---------------

1. To install Cyclone on your machine for the first time use [**cyclone-bootstrap**](https://github.com/justinethier/cyclone-bootstrap) to build a set of binaries. 

2. After installing you can run the `cyclone` command to compile a single Scheme file:

        $ cyclone examples/fac.scm
        $ examples/fac
        3628800
    
    And the `icyc` command to start an interactive interpreter:
    
        $ icyc
        
                      :@
                    @@@
                  @@@@:
                `@@@@@+
               .@@@+@@@      Cyclone
               @@     @@     An experimental Scheme compiler
              ,@             https://github.com/justinethier/cyclone
              '@
              .@
               @@     #@     (c) 2014 Justin Ethier
               `@@@#@@@.     Version 0.0.1 (Pre-release)
                #@@@@@
                +@@@+
                @@#
              `@.
        
        cyclone> (write 'hello-world)
        hello-world

   You can use [`rlwrap`](http://linux.die.net/man/1/rlwrap) to make the interpreter more friendly, EG: `rlwrap icyc`.

3. Read the documentation below for detailed information on how to use Cyclone.

Documentation
-------------

The [User Manual](docs/User-Manual.md) covers in detail how to use Cyclone, and provides information and API documentation on the Scheme language features implemented by Cyclone.

The [Development Guide](docs/Development.md) contains instructions for hacking on Cyclone.

[Writing the Cyclone Scheme Compiler](docs/Writing-the-Cyclone-Scheme-Compiler.md) provides high-level details on how the compiler was written and how it works.

Finally, if you need a place to start learning the Scheme language try a classic textbook such as [Structure and Interpretation of Computer Programs](https://mitpress.mit.edu/sicp/full-text/book/book.html).

License
-------
Copyright (C) 2014 [Justin Ethier](http://github.com/justinethier).

Cyclone is available under the [MIT license](http://www.opensource.org/licenses/mit-license.php).
