***
1. [How much is a clock cycle and why should we use it for measuring speed?](#How%20much%20is%20a%20clock%20cycle%20and%20why%20should%20we%20use%20it%20for%20measuring%20speed?)
***
# How much is a clock cycle and why should we use it for measuring speed?

[[💟 CPU Architectures#Clock cycle | What is a clock cycle? ]]

Computers have different speeds. The speed of a program can vary based on the machine where it is executed. Nevertheless, the clock cycles a program takes is independently from the CPU.
If we write that something takes 10 clock cycles then it will still take 10 clock cycles even if the CPU clock frequency is doubled.

The length of a clock cycle is the reciprocal of the clock frequency. For example, if the clock
frequency is 4 GHz then the length of a clock cycle is
$$
\frac{1}{4 GHz} = 0.25ns
$$

![[Pasted image 20240718165916.png]]