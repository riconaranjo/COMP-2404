# COMP 2404 Midterm Review | Fall 2018

## Section 1 | Basics of C++ Development

### Linux Platform

- types of shells
- basic unix commands / io redirection
- types of unix platforms
- program building
  - **compiling / linking**
    - what are they?
    - what commands are used?
  - **source files / object files / executables**
  - **makefiles**
    - what are they?
    - what are they used for?

### Basic Language Features

- terminology
  - expressions / statements / blocks / scope
  - operators / operands / arity / precedence / associativity
- functions
  - global / member functions
  - declaration / implementation
  - function design
- parameter types
  - input / output / inout (input-output)
- parameter passing
  - by-value, by-reference, by-reference-by-pointer
- references
  - what are they?
  - what are they not?
  - how are they used?

### Programming Conventions

- naming / indentation / comments

## Section 2 | Basics of C++ Classes

### Class Definitions

- binary scope resolution operator ::
- access specifiers
  - public / private / protected
- code organization
  - header / source
- class interface
  - how you interact with a class
  - shows the set of public members

### Constructors / Destructors

- default arguements
- contructors
  - copy / conversion / default
- destructors
  - order of execution
    - child destructors are executed before parent
- copy contructors
  - what are they?
  - what do they do?
  - when are they called?

### Memory Management

- stack / heap
- **pointers**
  - what are they?
  - why are they used?
  - how are they used?
  - operators:
    - arrow (->) / dereferencing (*) / address-of (&)
  - differences references / pointers
  - parameter passing with pointers
  - static / dynamic memory allocation
    - dynamic: new / delete
  - memory leaks
  - 4 types of arrays
    - **statically** allocated array of **object pointers**
    - **statically** allocated array of **objects**
    - **dynamically** allocated array of **object pointers**
    - **dynamically** allocated array of **objects**

## Section 3 | Basics of Object-Oriented Design

### Software Eng. Overview

- software development life cycle
  - requirements analysis
  - design
  - implementation
  - testing

### Information Hiding

- data abstraction
  - seperating class interface from implementation
- encapsulation
  - group data that belongs together
- principle of least privilege
  - protect your data

### Object Design Categories

- types of objects
  - control / view / entity / collection
    - what are they?
    - what do they do?
    - what are they responsible for?
    - why use them?
- maintainability
- collection classes

### Documenting Design

- uml class diagrams
  - no collection classes
  - no getters / setters / ctor / dtor
  - classes
    - attributes / operations
  - associations
    - composition / inheritance
  - composition
    - directionality / multiplicity

## Section 4 | Essential Object-Oriented Techniques

### Encapsulation

- composition
  - member initializer syntax
  - order of ctor / dtor
- constants
  - objects / data members / member functions
- friendship
- static class members
- linked lists
  - insertion / deletion / clean-up
  - singly / doubly / tail / no-tail

### Inheritance

- base / derived
- member access
- base class initializer syntax
- order of execution
  - ctor / dtor