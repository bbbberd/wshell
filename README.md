# wshell

WSH is simple implementation of linux shell written in c inspired by LSH that is the subject of a
tutorial on [Brennan blog][1].  It demonstrates the basics of how a shell works. That is: read, 
parse, fork, exec, and wait.  Since its purpose is just for me learning (not feature completeness 
or even fitness for casual use), it has many limitations, including:

* Commands must be on a single line.
* Arguments must be separated by whitespace.
* No quoting arguments or escaping whitespace.
* No piping or redirection.
* Only builtins are: `cd`, `help`, `exit`.

Running
-------

You can use basic `cc src/main.c` to compile, and then `./a.out` to run, or use gcc with `-o <file_name>`, 
or other c compiler. If you would like to use the standard-library based implementation of 
`lsh_read_line()`, then you can do: `gcc -DWSH_USE_STD_GETLINE -o lsh src/main.c`.

License
-------

This code is in the public domain (see [UNLICENSE](UNLICENSE) for more details).
This means you can use, modify, and distribute it without any restriction.  I
appreciate, but don't require, acknowledgement in derivative works.

[1]: http://brennan.io/2015/01/16/write-a-shell-in-c/
