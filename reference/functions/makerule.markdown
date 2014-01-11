
function makerule(source, targets)

Evaluates whether a target file needs to be built or rebuilt from one
or more source files.  The function is provided to emulate the
semantics of the Unix make program.

In a traditional Makefile, rules take the form

 target: source1 source2 ..
 (tab) commands

The top line evaluates to a predicate for building executing a number of commands,
 which is true if the target file does not exist, or if any of the source dependencies
in the list has been changed since the target was last built. 

The makerule function emulates the same semantics and sets a class if
the target needs to be built or rebuit, i.e. if the top line of an
equivalent makefile is true.

The source argument may be either a scalar or a list reference.  If
the source argument is the name of a list variable, then the entire
list of sources is used in the determination of whether the target needs
rebuilding.

Example

classes:

 "build_me" expressions => makerule("/tmp/target", "/tmp/source.c");

commands:

   build_me::

      "/usr/bin/gcc -o /tmp/target /tmp/source.c";




 
