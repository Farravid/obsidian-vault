GNU
The 64-bit version is better than the 32-bit version. The Gnu
compiler often inserts built-in code instead of the most common memory and string
instructions. The built-in code is not always optimal. Use option `-fno-builtin` to get
library versions instead.


In order to track integer overflow:
 get a compiler warning for such optimizations with
option `-Wstrict-overflow=2`, or (5) make the overflow behavior well-defined with
option `-fwrapv` or `-fno-strict-overflow` 