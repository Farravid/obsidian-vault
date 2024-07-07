
nasm (assembler) for generating object files

===

objdump for dissasembly an object

===

set a register to 0 is faster with xor instrucciontion, just two (bytes?)

====

esp (extended stack pointer) points the end of the stack. Every time we make a push the esp register is esp - 4 in case we push a 4 bytes (32 bits)

====
the call instruction pushes (push) the previous direction (which is the next instruction) and jumps into the given direction, in this case the name of the function or section

====
(not 100% sure how to explain but) 
if we don't need to use esp we can avoid the add in order to restore the position of esp
![[Pasted image 20240704233856.png]]

but we would need it if we do more stuff here