# COMP-2404

📘 My notes for my Intro into Software Eng. (CS) course – written in markdown

# Polymorphism

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