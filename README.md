# projects

## [hewg](https://github.com/corvid3/hewg)
*C/CXX build system infrastructure*
Build system and package manager for C/CXX projects. Projects are defined solely though configuration files, instead of a messy tangle of scripts prone to breaking.
Compiled projects may be installed to the users `$HOME/.hewg` cache directory, where executables may be added to the path or libraries may be referenced by other hewg projects.
Dependencies are resolved via a simple dependency-tree graph managed by a datalog implementation which sorts out collision errors in dependency includes.
Written in desperation due to the current status of modern build systems.  
**NOTE** : most projects listed use hewg as their build infrastructure.

## [tenc32]()
*Emulator for a fake CPU architecture*
TODO

## [tenc32 toolchain]()
*tenc32 development environment*
With a CPU emulator comes with the need to have the ability to write software for it. 
An assembler and linker targeting POFF[^1] is provided for basic low level software development.
A work-in-progress C compiler aiming for C23 compliance is provided for hosted environment software development.

## [tenc32 software]()
*Things to run on the emulator*
TODO

## [brbt](https://github.com/corvid3/brbt)
*Bounded red black tree library*  
Left-leaning red black tree implementation in C. Implementation based off of Robert Sedgwick's seminal paper. API is designed to be simplistic to use, whilst also providing deep control over how memory is allocated. 
A cache replacement policy hook is also provided, so that fixed-capacity caches can be implemented using the library.

# parser libraries
*Serialization and Deserialization libraries*

### [libscl]()
*Simple Configuration Language*
`libscl` is a CXX library that implements the SCL specification[^2] for serialization and deserialization. Configuration file structure is defined through the use of CXX template metaprogramming techniques.
Defined file structure allows the SCL parser to automatically serialize and deserialize data into and out-of CXX data structures.
Written out of desperation trying to find a configuration standard that wasn't miserable to implement.

## [jayson]()
*JSON (de)serialization*
`jayson` is a CXX library that implements a non-strictly conforming implementation of a JSON serializer/deserializer. 

## [terse]()
*Terminal argument parser with compile-time defined options*
`terse` is a CXX library that provides basic 'subcommand' style argument and option parsing. Options and subcommands are defined through the use of CXX template metaprogramming techniques.

## [lexible]()
*Backtracking recursive descent compile-time parser generator for CXX*
`lexible` is a CXX library that provides tools to create a lexer and parser in CXX. 
Interfacing with lexbile happens mostly through the type system, using templated data structures to generate a backtracking recursive descent parser at runtime.

[^1]: "Passerine Object File Format"
[^2]: Specification can be found in the root directory of the SCL repository
