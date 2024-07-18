This file contains information about the specification of different OS, comparations...
This page will also contain relevant information for understanding OS architectures, how they are built and so on.
***
1. [Function parameters](#Function%20parameters)
***
# Function parameters

We have seen that ==64 bits== architectures can pass the function parameters into a registers instead of using the stack. [[💟 CPU Architectures#64 bits vs 32 bits | See differences between 64 vs 32 bits]]
Well not all the OS handle this in the same way.
## Linux, BSD, and Mac
These 3 OS allow up to **14** parameters to be transferred in registers (6 integer and 8 floating point).
## Windows
Windows allows only **4** function parameters to be transferred in registers. 

> Even though Windows has less registers for function parameters, this may be mitigated by making critical functions inline or static or by using a compiler that can do whole program optimization

# Resources

* Pedagogy basic OS written in C: https://github.com/mit-pdos/xv6-public
* 



