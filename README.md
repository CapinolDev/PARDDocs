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

# Compiler Architecture
