





# MIPS ISA
We built a cpu using logisim evolution. this cpu will execute most of MIPS instructions. first phase was a single cycle cpu because it takes just a rising edge to access the memory.
in the second phase we implemented cache and accessing to memory would take 5 clocks. Our cache was 2 way set-assosiative. Third phase was about pipline and we implemented MIPS  5 stage
pipline. In the last Phase we implemented branch prediction a saturate counter. 

In addition to all above works, we handled RAW hazard so if you read from a register too soon, the real value will be fast forwarded to output of register file.
Only hazard that may happen is when you load something to a register from memory and immidiately use the value of that register in the next instruction.
This won't work because when you are loading the value from memory, you need that value in the alu at the same time.

