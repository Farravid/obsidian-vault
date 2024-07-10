
===
RISC vs CISC
https://cs.stanford.edu/people/eroberts/courses/soco/projects/risc/risccisc/

===
AVX-512
**AVX-512** are 512-bit extensions to the 256-bit [Advanced Vector Extensions](https://en.wikipedia.org/wiki/Advanced_Vector_Extensions "Advanced Vector Extensions") [SIMD](https://en.wikipedia.org/wiki/SIMD "SIMD") instructions for [x86](https://en.wikipedia.org/wiki/X86 "X86") [instruction set architecture](https://en.wikipedia.org/wiki/Instruction_set_architecture "Instruction set architecture") (ISA)

===
More info from intel, use cases, even though getting started
https://www.intel.com/content/www/us/en/products/docs/accelerator-engines/what-is-intel-avx-512.html

===
Asmlib (Memory and string functions optimized in assembly)
http://www.agner.org/optimize/asmlib.zip 
 ===
 
Avoid the function scanf

===

Store string in a memory pool to avoid memory fragmentation and more
http://www.agner.org/optimize/cppexamples.zip

===

Unsigned vs signed for performance

`// Example 7.4. Signed and unsigned integers`
`int a, b;`
`double c;`
`b = (unsigned int)a / 10;`
 `// Convert to unsigned for fast division`
`c = a * 2.5;`
 `// Use signed when converting to double`

===
**Branch prediction**

The target of branches and function calls are saved in a special cache called the branch
target buffer.

===
Negate a number
`// Example 7.43`
`union {`
`float f;`
`int i;`
`} x;`
`x.f = 2.0f;`
`x.i |= 0x80000000;`
 `// set sign bit of f`
`cout << x.f;`
 `// will give -2.0`
===

TODO: Do something with the matrices and the cache?
TODO: Can I print a simd instruction with fmt?

# What is up

```c++

<compile>
{
	 "language": "c++"
}
</compile>

int main()
{
	 int x = 5;
	 return x;
}
```