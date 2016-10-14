# Joy website backup
A copy of Kevin Albrecht's mirror at http://www.kevinalbrecht.com/code/joy-mirror/joy.html
## Notes
* The code base is not clean in my view, thus I do not maintain this implementation. I just learn from the design of the language

* If you care about the continuation of Joy and you consider the code base hackable, feel free to fork and maintain it

* I also play with a Joy-like language in Javascript here: [sad coffee](https://github.com/xieyuheng/sad-coffee)
## Dependencies
  Joy uses the [Boehm-Demers-Weiser Garbage Collector](https://github.com/ivmai/bdwgc). Since the repository is so big, I opted to use commit `7aba59b5853330c9368bc16dd606e1617c704334` located in the `src` directory here.
## Building
To build the Joy interpreter, use `make`.
## Lib structure
* joy library
  * usrlib.joy -- personal user library, loaded by default
  * inilib.joy -- the initial library of the joy system
  * the basic libraries
    * agglib.joy -- aggregates: sets, lists, strings
    * seqlib.joy -- sequences: lists, strings with ordering
    * numlib.joy -- numeric: integers, floats
    * symlib.joy -- symbolic manipulation (only translations)
      * symtst.joy -- test file
      * symtst.out -- output
  * the special libraries
    * mtrlib.joy -- matrices and vectors
      * mtrtst.joy -- test file
      * mtrtst.out -- output
    * tutlib.joy -- interactive tutorials
      * joytut.joy -- an application
      * joytut.com -- a (pseudo) input
      * joytut.out -- output
    * lazlib.joy -- "lazy" infinite and finite lists
      * laztst.joy -- test file
      * laztst.out -- output
    * lsplib.joy -- a small (eval-apply) lisp interpreter
      * lsplib.lsp -- a small library for this version of lisp
      * lsptst.joy
      * lsptst.lsp -- input
      * lsptst.out -- output
    * plglib.joy -- propositional logic semantic tableaux
      * plgtst.joy -- test file
      * plgtst.out -- output
    * grmlib.joy -- grammar library (generating and parsing)
      * grmtst.joy -- test file
      * grmtst.out -- output
