This file contains information about the specification of different CPU architectures, comparations...
This page will also contain relevant information for understanding CPU architectures, how they are built and so on.

---
1. [Architectures](#Architectures)
	1. [Clock cycle](#Clock%20cycle)
1. [64 bits vs 32 bits](#64%20bits%20vs%2032%20bits)
1. [CPU Dispatching](#CPU%20Dispatching)

---

# Architectures

## Clock cycle

The speed of a computer processor, or CPU, is determined by the **Clock Cycle**, which is the amount of time between two pulses of an oscillator. Generally speaking, the higher number of pulses per second, the faster the computer processor will be able to process information. The clock speed is measured in Hz.

> [!NOTE]
> Modern CPUs can execute more than on instruction per clock cycle.

# 64 bits vs 32 bits

These are some of the advantages that 64 bits systems have over 32 bits ones
-  Functions parameters are transferred in registers rather tan on the stack
-  The allocation and deallocation of big memory blocks is more efficient.
-  The SSE2 instruction set is supported on all 64-bit CPUs and operating systems.

# CPU Dispatching

CPU dispatch is **a technique when there are multiple compiled versions of your code for different CPU features**, and in runtime, your program detects which CPU features your machine has and uses the most performant version in runtime.

This can be useful, when some machines don't support certain set of vector instructions such as AVX512 or similar and you want to use different code for different CPUs, based on the support of these vector instructions. 


