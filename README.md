# Introduction & Philosophy

PARD is a programming language designed around game design and
development. It leverages FORTRAN's fast math and C interoperability.
The name PARD is an abbreviation of Punching Card, which is an homage to
the early days of FORTRAN.

# Lexical Grammar

## Variables and their types

Variables, just like most other programming languages, are a significant
part of PARD.\
There's 4 basic variable types:

-   **int**: A standard integer type for counts, loop counters, and IDs.

-   **float**: A floating-point number for positions, physics
    calculations, and deltatime.

-   **bool**: A boolean value (`true` or `false`) for state flags.

-   **string\[N\]**: A fixed-length, ultra-fast character array of size
    $N$.

As you can see, strings are not dynamically sized - this is not only for
easy operation in fortran, but it also introduces a good performance
boost.

## Variable definition

You can easily define a variable in the following way:\
`int myInt = 10`\
`float myFloat = 10.5`\
`bool myBool = true`\
`string[6] myString = ’Hello!’`

## Simple usage of variables

You can easily use a variable in multiple ways, here are some:\
`int x = 2`\
`int y = 3`\
`int z = x + y`\
`float f = 2.5`\
`float g = 0.5`\
`float h = f / g`\
You cannot mix types: by this I mean you can't do the following:\
`int x = 2`\
`float y = 10.5`\
`float z = x + y`\
This will raise an error, as not all types used together are of the same
type.

## Converting variables to other types

In the previous example, we had this:\
`int x = 2`\
`float y = 10.5`\
`float z = x + y`\
But what if we want to combine different types? Well, you can use simple
parsing functions: `float z = x + y.tofloat`\
There exists tofloat, toint and tostring.

## Array definition

Okay, how do we define arrays?\
Before the type, put (n) where n is the lenght of said array.\
`(2)int myInt = [10, 5]`\
`(3)float myFloat = [10.5, 3.14, 5.5]`\
`(3)bool myBool = (true,false,false)`\
`(2)string[6] myString = (’Hello ’, ’World!’)`

## Accessing values in an array

To get a part of an array, use an index. PARD is 1-index based, e.g. the
first item is index 1, the second is index 2 etc.\
`(2)int myIntArray = [10, 5]`\
`int myInt = myIntArray[2]`\
In this exaple, myInt will be 5.

# Compiler Architecture
