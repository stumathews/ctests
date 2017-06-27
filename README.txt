The fundamental data types
==========================
declarations, expressions and assignment
the fundamental data types
characters and data type char
the data type int
the intergral types hosrt, long and unsigned
the floatiing types
the use of the typedef 
the sizeof operator
getchar and putchar
mathematical functions
hex and oct constants

Flow of control
===============
relational, equality and logical operators
relational operators and expressions
equality operators and expressions
logical operators and expressions
the counpound statments 
the empty statement
the if and else statmenet
the while statemente 
the for statement
the comma operator
the do statement
the goto statement
the break and continue statemnet
the conditional operator

functions
========
function definition
the return statement
function prototypes
function declarations from the compilers point of view
an alternative style for function definition order
function invocations and call by value
using assertions
scope rules
storage classes
static external variables
default initialization

Array, pointers and strings
===========================
one dimensional arrays
pointers
call by reference
the relationship between arrays and pointers
pointer arithmetic and pointer size
arrays and function arguments
dynamic memory allocation
strings
string handling functions
multidimensional arrays
arrays of pointers
arguments to main
ragged arrays
functions as arguments
arrays of pointers to function
the type qualifiers const and volatile

Bitwise operators and enumerations types
========================================
bitwise operators and expressions
masks
packing and unpacking
enumeration types

The preprocessor
===============

#include
#define
macros with arguments
type definitions and macros
conditional compilation
the operators # and ##
the assert macro
use of error and #pragma
line numbers
corresponding functions

Structures and Unions
====================

structures
accessing members of a structure
operator precedence and associativity
using structures and functions
initialisation of structures

# build packages,issue these commands for binary and source redistributables
cpack --config CPackConfig.cmake
cpack --config CPackSourceConfig.cmake
