***
1. [Compiler options](#Compiler%20options)
	1. [GNU and Clang](#GNU%20and%20Clang)
		1. [`-O3 or -Ofast`](#%60-O3%20or%20-Ofast%60)
		1. [`--combine-fwhole-program`](#%60--combine-fwhole-program%60)
		1. [`-fno-rtti`](#%60-fno-rtti%60)
	1. [MSVC](#MSVC)
***

# Inlining
One of the most important compiler optimizations!!
If the symbol is not visible for the compiler, such as qsort() as an example the function cannot be inlined !!!

# Compiler options
## GNU and Clang

### `-O3 or -Ofast`
This compiler option optimize the code for speed.

### `--combine-fwhole-program`
TODO

### `-fno-rtti`
==Enabled by default==
(RTTI) stands for **Runtime type identification**. This is a feature of some languages such as C++ in order to provide information about an object's data type at runtime.
This can add overhead if we are not relying on RTTI.

> Note this option will disable the possibility to perform `dynamic_cast<>` and you will obtain a compilation error
 
## MSVC

### `/GR-`
Same as [[#`-fno-rtti`]]
