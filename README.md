# COMP-2404

📘 My notes for my Intro into Software Eng. (CS) course – written in markdown

# 1 | Basics of C++ Development

## Shells
A shell is program that allows direct access to OS, and allows users to run programs.
- command line interpreter
- main shells
  - ksh (korn shell)
  - sh (bourn shell)
  - bash (bourne-again shell)
  - csh (c-shell)
- differences include
  - commandline shortcuts
  - environment variables

## Redirection
pipelining is used for io redirection
- \< redirects from
- \> redirects to

## Program Building

**Compiling:** generate object code from source files<>
- gcc -c to compile.

**Linking:** generate execuatable from object code
- gcc -o to generate executable.

**Makefiles:** easy way to compile and link multiple source files.
- text file
- organizes compiling and linking commands
- defines source file dependencies

## 1.2 | Basic Language Features

**Expressions:** sequence of operation that evaluates to a single variable.

**Statements:** expression terminated by a semicolon that resolves to a single variable.

**Blocks:** sequence of statements within pair of braces.

**Scope:** part of program where a variable can be used.

### Operators
- **operands**
  - variables on which operator acts on
- **arity**
  - number of operands
- **precedence**
  - order in which operators execute
- **associativity**
  - order in which operators of same precedence execute
    - right-to-left / left-to-right

### Variables
- contains: name / value / data-type / memory address
- can be primative / user-defined / pointer

### Functions
- **global / member functions**
  - static member functions are like 'global' within class
- **declaration / implementation**
  - declaration in header
  - implementation in source
- **function design**
  - reusable
  - single purpose
  - encapsulation (hidden functionality)

## 1.3 | Programming Conventions

### Naming / Indentation / Comments
- promotes readability
- comments block in main
  - specifying purpose of program
  - usage (command line arguments)
  - author
  - revisions
- comments before class
  - specifying purpose of class
  - descriptions of complex / critical members

# 2.1 | Classes

## Binary Scope Resolution Operator ::
1. To access a global variable when there is a local variable with same name.
2. To define a function in source file.
3. To access a class's static variables.
4. Multiple inheritance.

## Access Specifiers
- public
  - visible to all
- private
  - visible only to same class
- protected
  - only visable to sub-classes

## Code Organization
**header Files:**
- class defintion
- data members
- member function prototypes

**Source Files:**
- member function implementations
- static data member intialization

## Class Interface
- how you interact with a class
- shows the set of public members
  - what users need to know:
    - class name
    - public members

# 2.2 | Constructors + Destructors

## Default Arguements
- default parameter value
- specified in function prototype
- must be right-most in parameter list

### Contructors
- explicitly called
- three types

**1. Copy Constructor:**
- takes a reference of the same class
- called when you initialize a variable to another object
  - but not already intialized variable
- implicitly called when you pass by reference

**2. Conversion Constructor:**
- takes any reference of other than same class

**3. Default Constructor:**
- called when memory is allocated statically / dynamically
- initializes data members

### Destructors
- implicitly called
- order of execution
  - child destructors are executed before parent

# 2.3 | Memory Management

## Pointers

- small, fixed-size variable
  - allows changes to memory outside current scope
  - avoids copying data
  - the only way of using dynamically allocated memory

- **operators:**
  - arrow (->) / dereferencing (*) / address-of (&)
  - dot operator (.) accesses object members
  - arrow operator (->) dereferences object and then accesses object member

## Dynamic Memory Allocation
- use `new` / `delete` commands

## 4 types of arrays
- **statically** allocated array of **object pointers**
- **statically** allocated array of **objects**
- **dynamically** allocated array of **object pointers**
- **dynamically** allocated array of **objects**

# 3.1 | Basics of Object-Oriented Design

- **Software Development Life Cycle**
  - requirements analysis
  - design
  - implementation
  - testing

# 3.2 | Information Hiding

**Single Responsibility:** objects should have only one purpose.

**Data Abstraction:** seperating class defintion from implementation.
  - seperate the **what** from the **how**

**Encapsulation:** group data that belongs together.
- protect data from bad code
- reuse code when possible
- give data memebers only private or protected access

**Principle of Least Privilege:**
- protect your data
- access to runtime objects should limited

# 3.3 | Object Design Categories

## Types of Objects

- **control**
  - control program flow
  - manages how classes interact
- **view (boundary)**
  - communication /interaction with user
- **entity**
  - persistent information
  - information that survives termination
- **collection**
  - *collection:* data structure to store multiple data objects of same type
  - collection class stores multiple collection objects

# 3.4 | Documenting Design

**UML Class Diagrams:**
- no collection classes
  - implied with multiplicity
- no getters / setters / ctor / dtor
- include **classes:**
  - attributes / operations
- include **associations:**
  - composition / inheritance
- include **composition:**
  - directionality / multiplicity
- include access specifiers
  - `+` public
  - `#` protected
  - `-` private

# 4.1 | Essential Techniques

## Composition
- member initializer syntax
- order of ctor / dtor

## Constants
- objects / data members / member functions
  - object / data member: constant keyword before data type
  - member function : constant keyword after protoype
- constant functions
  - cannot modify data members
  - the only type of functions allowed on a constant object
- constant data members must be initialized before constructor body
- must use member initializer syntax

## Friendship
- grants access to all private / protected members
  - cannot be taken
  - does not apply to derived classes of friend class
- friend function can access all members of a class

## Static Class Members
- exists even without class instances
- global to class
- only one instance allows
- intialized in constructor
- static member functions can only access static data members

## Linked Lists
- insertion / deletion / clean-up
- singly / doubly / tail / no-tail

# 4.2 | Inheritance

## base / derived
- all base class members are inherited
  - but access modifiers change
  - private become invisible
  - protected / public remain the same

## base class initializer syntax
- call base constructor as with class initializer syntax

# 4.3 | Design Patterns

## order of execution
  - ctor / dtor
  - ctor: parent to child
  - dtor: child to parent

# 4.4 | Polymorphism

- enables generalized use of a class hierarchy
  - interface at base class
  - derived classes override interface functions with specialized behaviour
- use base class pointers to manipulate derived classes
  - this is called **dynamic binding**

## Function Bindings

Linking a function call to a specific function

- decide between derived and base class member functions

### Static Binding

- selection made at compile time
- _always used_ when called using **object varibable** name
- _can be used_ when called using **object pointer**

### Dyanamic Binding

- selection made at runtime
- _never used_ with **object variable**
- _can be used_ with **object pointer**